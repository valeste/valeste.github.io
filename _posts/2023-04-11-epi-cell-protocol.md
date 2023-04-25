---
layout: post
title: Epithelial Cell Isolation from Lab Reared Botryllus schlosseri
date: '2023-04-11'
categories: protocol
tags: protocol
---

This draft is version 0.23.04.12.

# *Materials*

### Equipment

-   Biosaftey cabinet
-   Nikon SMZ745T Stereoscopic Microscope with Excelis camera
-   15 cm diameter glass culture dish
-   Aspirator
-   Forceps
-   Osmo1 Osmometer
-   Evos XL Core inverted microscope
-   Spray bottle
-   Pipette wand
-   Conical holder

### Consumables

-   BH Supplies Insulin Syringes U-100 28G 1ml/cc 5/16” (8mm)
-   15 mL centrifuge tubes (number dependent on how many samples)
-   30 ppt (~850-900 mOsm/kg H2O) filtered seawater (FSW)
    -   This can be pre-formulated (but autoclaved) Red Sea Salt or an
        in-house solution
-   70% ethanol
-   Corning 6 well plates
-   0.22 um filter units
-   50 mL, 10 mL, and 5 mL serological pipettes
-   100 um cell strainers
-   10,000 U/ml penicillin
-   10 mg/ml streptomycin
-   25 μg/ml amphotericin-B

### Required solutions

For all solutions below you will need about 1 L of filtered seawater.
Note you will need an additional n x 300 mL of FSW where n = number of
wells you intend to seed.

#### Filtered Seawater - 0.05% Gentamicin (FSW-G) 

This solution is essential for the isolation of tunicate individuals 24
hrs prior to dissection.

In the biosaftey cabinet add together the following:

-   500 mL of filtered seawater (~30 ppt / 850-900 mOsmo/kg)
-   238.8 uL 50 mg/mL stock gentamicin
    -   Gentamicin (477.596 g/mol); 50uM/mL = 23.88ug/mL

#### Filtered Seawater - 1% Pen/Strep & 0.01% Amp B (FSW-PSA)

This solution is used for transferring the excised buds to the biosaftey
cabinet in TPS as well as washing prior to dissection.

In the biosafety cabinet add together the following:

-   248 mL filtered seawater (~30 ppt / 850-900 mOsmo/kg)
-   250 uL Amphotericin B (250ug/mL stock solution)
-   2.5 mL of 100x Penicillin-Streptomycin

#### Tunicate Culture Medium (TCM)

This solution is the base media for all cell cultures. It may be
modified to incorporate other nutrient or organic osmolyte requirements.

According to [Rabinowitz and Rinkevich
2011](https://link.springer.com/article/10.1007/s11626-010-9357-4) for
each 35mM well you will need 2mL of TCM at the initiation of the
cultures. Thereafter, you will replace 10% of media every two week
according to [Rabinowitz and Rinkevich
2004](https://pubmed.ncbi.nlm.nih.gov/15801159/)

As such upscale or downscale the below list as needed. In biosaftey
cabinet add the following solutions:

-   47 mL sterile L-15 media
-   1 mL of 1 M HEPES (20mMol/L)
-   1.5 mL heat inactivated fetal bovine serum (HI-FBS) (3%)
-   1% mixed antibiotic solution containing penicillin (10 000 U ml–1),
    streptomycin (10 mg ml–1) and amphotericin B (25 μg ml–1) (PSA)
    -   50uL of Amphotericin B (250ug/mL stock solution)
    -   0.5mL of 100x Penicillin-Streptomycin (1% PSA)
-   Adjust media to correct osmolarity using concentrated salt water to
    achieve 850-900 mOsmo/kg.

<!-- -->

    n <-6 # change n as needed where n = the number of wells you intend to seed
    FSW_G_mL <- 50*n + ((50*n)*0.1)
    FSW_PSA_mL <- (20*n) + (5*n) + (((20*n) + (5*n))*0.1)
    FSW_mL <- FSW_PSA_mL + FSW_G_mL + (n*300) + ((FSW_PSA_mL + FSW_G_mL + (n*300))*0.1) 
    # last portion of each equation adds 10% volume calculating for loss during water transfer

    ## [1] "2524.5 mL of FSW needed for 6 wells"

    ## [1] "330 mL of FSW-G needed for 6 wells"

    ## [1] "165 mL of FSW-PSA needed for 6 wells"

# *Epithelial Cell Isolation*

Be sure to have sufficent stocks of the above three solutions prior to
following the below procedures.

#### 1. The day prior to bud isolation

1.1. Using [this staging
method](https://valeste.github.io/2023-04-07-Devo-Bsc/), identify
individuals with zooids at stage C2, average zooid size of 300 μm,
colonies that are large (~200 zooids embedded in tunic), and appear
health according to health scoring metric.

1.2. Remove individuals from recirculating seawater system and place
each individual separate containers filled with 50 mL of FSW-G solution
for 24 hours, starving them for that time period.

1.3. Prepare coated plates as needed for the next day.

#### 2. Bud excsion

2.1. Remove colonies from FSW-G

2.2. Wash colonies and glass slide for 30 sec with 70% ethanol

2.3. Immerse glass slide in 15 cm diameter, sterile glass dish filled
with fresh 20mL FSW-PSA. For each new colony microdissection, rinse the
15 mL glass plate with 70% ethanol in triplicate, followed by triplicate
rinse of FSW-PSA prior to refilling plate with more FSW-PSA.

2.4. Under stereomicroscope on lab bench take picture of colony with
Excelis camera

2.5. Using a pair of 28G syringe needles, open the tunic and dissect
buds and transfer groups of 10 buds to 15 mL conical tubes containing 5
mL of FSW-PSA.

2.6. Transfer all conical tubes containing bud tissue to the biosaftey
cabinet in TPS for cell seeding

#### 3. Seeding tissue

3.1. In the biosaftey cabinet, pour out contents of one conical tube
into a sterile 100-μm pore-size nylon cell strainer and rinse tissue
with 200-300 mL of FSW.

3.2. Transfer buds to pre-coated wells and remove any excess FSW.

3.3. To each well add 2 mL of TCM

3.4. Incubate cells at 20 C
