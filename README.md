# School Districts and Supervisory Unions Annual Update

Updated June 25, 2024

- [Contact](#contact)
- [Timing](#timing)
- [Population Density Calculation](#population-density-calculation)
- [FY2025 Update](#fy2025-update)
- [FY2026 Update](#fy2026-update)
- [FY2027 Update](#fy2027-update)
- [FY2028 Update](#fy2028-update)


## Contact
Current contact at AOE is Julie Robinson (julie.robinson@vermont.gov). Nicole Lee (nicole.lee@vermont.gov) is Julie's supervisor and another potential contact.

## Timing
[School district](https://geodata.vermont.gov/datasets/03147644b3db427e8117d9f7bf895a0b_56/explore) and [supervisory union](https://geodata.vermont.gov/datasets/08c21e8c8c094771b8308ddd7bb1db1e_55/explore) layers are updated annually for the FY starting on July 1 (e.g., FY2025 begins July 1, 2024).

Contact Julie in late May/early June to inquire about any changes to SD or SU boundaries or names. Make edits in time to be published to portal by end of June/July 1 (Ivan will do this part).

## Population Density Calculation
In addition to boundary/name changes, the population density estimates in the SD layer should be updated based on the previous year's [population estimates by town](https://www2.census.gov/programs-surveys/popest/tables/) - navigate to folder containing appropriate year, /MCDs, /totals, file for "POP-50". See legislative requirements [here](https://legislature.vermont.gov/statutes/section/16/133/04010).

Most SDs follow town boundaries for either one or multiple towns. As of FY2025, there are two exceptions:

1. North Bennington ID is comprised of a small portion of both Shaftsbury and Bennington. Southwest Vermont UESD is comprised of Pownal, Woodford, Bennington, and Shaftsbury **excluding the portions of Bennington and Shaftsbury belonging to North Bennington ID**. Mt. Anthony UHSD is the same as Southwest Vermont UESD but *does NOT exclude* the North Bennington ID area (or population). 
![alt text](image-1.png)

2. Blue Mountain USD covers all of Ryegate and Groton, but also a small portion of northeast Newbury (Wells River). Oxbow UUSD is Bradford and Newbury, minus Wells River. ![alt text](image.png)

Population density is calculated by: 
1. Using the ALAND (land area) field from Census geography [county subdivisions](https://github.com/VCGI/vt-school-districts/blob/main/data/CensusGeo2023_countysub.csv) and ["sub towns"](https://github.com/VCGI/vt-school-districts/blob/main/data/SubTownGeography.csv) described above. 

2. Using total [population estimates by town](https://www2.census.gov/programs-surveys/popest/tables/) from Census. For sub town geographies, a ratio is applied to the latest population estimate for a town to make the adjustment. The ratio is based on the same percentage of the population falling in each sub town in the 2020 Census. It is assumed that the ratio remains relatively constant.

3. Summing ALAND and population totals from towns by school districts. For the school districts that deviate from town boundaries (i.e., sub town geographies), use the population ratio to calculate the adjusted population. 

4. Population density is calculated by SD using [population / (ALAND / 2,589,988)]. (denominator converts sq meters to sq miles.) Page 100 of the [2020 Census Demoraphic and Housing Characteristics File (DHC)](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www2.census.gov/programs-surveys/decennial/2020/technical-documentation/complete-tech-docs/demographic-and-housing-characteristics-file-and-demographic-profile/2020census-demographic-and-housing-characteristics-file-and-demographic-profile-techdoc.pdf) contains technical documentation.
For reference: [This file](https://vermontgov-my.sharepoint.com/:x:/g/personal/john_e_adams_vermont_gov/EbmeHZ1AxO1GmLAkWxtGUb8BlGN7iGxSxSWAL2TspYjo4Q?e=rPGzGQ) queries the 2023 population, area, and subtown geography files in github to calculate the densities. 



## FY2025 Update

* **School district** updates:
    * Name change for Orleans Southwest UESD to *Mountain View UESD*
    * Change Ferdinand's SU to *Essex North* (SU019)
    * Change Fletcher's SU to *Franklin West* (SU022)
    * Populate SUNAME field for Winhall (T248) with *Bennington Rutland SU* (formerly was blank)

* **Supervisory union** updates:
    * No changes or updates

* **Density calculations** (in school district layer):
    * Using 2023 population estimates by town, update population density following procedure above.
    

## FY2026 Update

## FY2027 Update

## FY2028 Update
