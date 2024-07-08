# Change detection of demolished built area in Gaza Strip after 2023 
## Introduction
Since 7 October. 2023, Israel and Hamas-led Palestinian militant groups have been continously having an armed conflict especially in Gaza Strip. Israel–Hamas war. The United Nations Economic and Social Commission for Western Asia (ESCWA) updated on May 2024 that 360,000 buildings in the Gaza Strip have been partially damaged or destroyed during Israel’s war against Hamas. Based on the data dated April 28, 2024 from Palestinian Central Bureau of Statistics , over 50% of the buildings were destroyed.Here presents a change detection of demolished building in Gaza Strip, using Google Earth Engine (GEE). The data from Dynamic World allows detection of built area. A decrese of built area implies that the building is demolished. By crosschecking with the RGB satallite images, it is to confirm that this method of change detection can be used as demage assessment of demolished buildings.

![paste to excel](mapGaza.PNG)
Figure 1. The map of Gaza Strip (outlined with black line).

## Methodology
Dynamic World (DW) is a global land use land cover (LULC) dataset with near realtime 10m resolution. It produces probabilities per pixel for 9 land types, including built area. Built area is defined as low- and high-density buildings, roads, and urban open space. The probabilities of ‘built’ is selected from DW. Probabilities of built on 7 Oct 2023 and 7 Jun 2024 are compared in this task. The decreased probability of built area represents the demolishment of buildings, roads and open urban space. When the probability of built area before is greater than 0.5 and decreases to less than 0.25 after. It represents the demolishment of built area.

This change detection is to compare the data between 7 Oct 2023 and 7 Jun 2024 in Gaza Strip.

Harmonised Sentinel-2 MSI: MultiSpectral Instrument, Level-1C is an imaging mission with a global 5-day revisit frequency. The S2 Multispectral Instrument (MSI) samples 13 spectral bands, including visible at 10 meters spatial resolution. The natural color band combines the red (B4), green (B3), and blue (B2) channels was used in cross checking the accuracy of this change detection task, by comparison with real visible imagery. The RGB S2 harmonised image is to validate our analysis of the change in built area.

The full javascript code of this change detection task in GEE can be accessed in the following link:
https://code.earthengine.google.com/6e622c0a2454404094a83302d5530081

A map of damage assessment from UNOSAT and a map of fortified position from Planet Lab are for checking the coherence of data between different data sources.


## Decreased built area in Gaza Strip
As shown in Figure 2 and 3, the built area (red) decreased and the area of bare ground (grey) increased. Before the war, the built area continuously covered the land in Gaza Strip. However, the built area scattered and was separated by bare ground. 

![paste to excel](mapGaza.PNG)
