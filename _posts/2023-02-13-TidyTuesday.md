Read in the data:
```
{r}
library(dplyr)
library(tidyverse)
############# accessing data ###########
# Option 1: Read in manually

feederwatch <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-01-10/PFW_2021_public.csv')
site_data <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-01-10/PFW_count_site_data_public_2021.csv')
```
Take a look at it:
```
{r}
head(feederwatch)
head(site_data)
```
I wanted to "reduce the clutter" since I just wanted to look at Blue Jay count over the months and snow depth.

```
{r}
#reducing the clutter in feederwatch data and site_data
feederwatchClean <- feederwatch[,c(1,12,13,8, 21)]

sitedataClean <- site_data[,c(1, 30,31)]
```
```
{r}
#joining the tables with dplyr (SQL based formatting)

birdObs <- merge(feederwatchClean, sitedataClean)

#removing NA's
birdObs2 <- na.omit(birdObs)
```
```
{r}
 ############# making a subset of the data ##########
blujayRows <- grep("blujay", birdObs2$species_code)
blueJayData <- birdObs2[blujayRows, ]
```

```
{r}
########### my plot ##############
par(mar = c (5, 4, 4, 4) + 0.3)
plot(type = "h", x = blueJayData$Month, y = blueJayData$how_many,
     xlab = "Month",
     ylab = "Blue Jay Count",
     main = "Change in  Blue Jay count over time and snow depth.",
     lwd = 10, col = "dark blue"
     )
par(new = TRUE) #allows us to add a new plot to overlay
plot(x = blueJayData$Month, y = blueJayData$snow_dep_atleast,
     pch = 13, col = "green",
     axes = FALSE, 
     xlab = "", ylab = "")
axis(side = 4, at = pretty(range(blueJayData$snow_dep_atleast)))
mtext("Pecieved snow depth (inches)", side = 4, line = 2)
```
![pdf](https://github.com/valeste/valeste.github.io/blob/master/assets/img/tidyTuesFeb13.pdf)