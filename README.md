# External Credit Assessment and the Mapping Process
## Background Information
The **Office of the Superintendent of Financial Institutions (OSFI)** has raised a new set of requirements to direct the usage of external credit assessments by big banks. After a review process of the major international rating agencies, OSFI has permitted banks to recognize credit ratings from the following rating agencies for capital adequacy purposes.
- **DBRS**
- **Moody’s Investors Service**
- **Standard and Poor’s (S&P)**
- **Fitch Rating Services**

Each bank will be responsible for assigning eligible **External Credit Assessment Institutions (ECAIs)**’ assessments to the risk weights available under the standardized risk weighting framework, i.e. deciding which assessment categories correspond to which risk weights.

The mapping process should be objective and should result in a risk weight assignment consistent with that of the level of credit risk reflected in the tables above. It should cover the full spectrum of risk weights. The following table provides guidance as to how such a mapping process may be conducted:

![image](https://user-images.githubusercontent.com/83738852/214069190-e6bf404a-ee69-4f8f-a644-961da180b81e.png "Credit assessment systems used by different organizations") 

*Figure 1: Credit assessment systems used by different organizations*

## Rules
* **Internal Grade (IG)** is usually assigned by analysts themselves, which are designed to reasonably matching with external credit ratings
* **Higher the IG** (Internal Grade), **lower** the **risk weight**
* If there is only **one assessment** by an ECAI chosen by a bank for a particular claim, that assessment should be used to determine the risk weight of the claim.
* If there are **two assessments** by ECAIs chosen by a bank which map into different risk weights, the **higher risk weight will be applied**.
* If there are **three or more assessments** with different risk weights, the assessments corresponding to the **two lowest risk weights should be referred to** and the **higher of those two risk weights will be applied**. 

* For the instrument issued by **US or Canadian government**, if there is **no external rating available**, default the grade to 'AAA'. 

* For the instrument issued by other **foreign government**, if there is **no external rating available**, default the grade to ‘A'.

## Objective 
For each security issuer, derive the "**Standardized Risk Weighting**" from the ratings provided by ECAIs, based on OSFI's specific rules

## Tools
SQLite Studio, MS Excel

## Inputs
* All the fixed income securities that the bank is holding as of Jan 2020. ("bond_jan_2020.csv")
![image](https://user-images.githubusercontent.com/83738852/214077042-4d7110c8-0c95-4e20-ae7d-1e5960d709b0.png "Fig. II: Partial view of securities holding by bank as of Jan 2020")

*Fig. II: Partial view of securities holding by bank as of Jan 2020*

* Mapping table from external rating to internal rating. (“lt_rating_to_ig.csv”) **NOTE**: **Higher the IG, lower the risk weight.** 
    
![image](https://user-images.githubusercontent.com/83738852/214077400-e5c44fb6-068e-4efc-a8bd-81e5f62860a4.png "Fig. III: Corresponding Investment Grade(IG) matching with credit assessments from other organizations") 

*Fig. III: Corresponding Investment Grade(IG) matching with credit assessments from other organizations*

* Mapping table from **internal grade (IG)** to internal rating (desired **Standardized Risk Weighting**). (“ig_to_rating.csv”) 
![image](https://user-images.githubusercontent.com/83738852/214078275-2ef6fa91-f294-41e3-a3ed-311bedb851e1.png "Fig. III: Conversion from Investment Grade(IG) to our own Standardized Risk Weighting (RTG_FINAL)") 

*Fig. III: Conversion from Investment Grade(IG) to our own Standardized Risk Weighting (RTG_FINAL)*

**Note**: “*lt_rating_to_ig.csv*” and “*ig_to_rating.csv*” are **derived** from the above-mentioned OSFI's guidance.

