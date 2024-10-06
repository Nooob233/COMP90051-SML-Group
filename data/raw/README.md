# COMP90051-SML-Group

## Tables Description
Data Source: https://foreverdata.org/1015/
Each data set is comprised of several tables detailed as follows:

### a. Members Table
- **MemberID**: A unique member ID.
- **AgeAtFirstClaim**: Member's age when first claim was made during the data set period.
- **Sex**

### b. Claims Table
- **MemberID**
- **ProviderID**: The ID of the doctor or specialist providing the service.
- **Vendor**: The company that issues the bill.
- **PCP**: Member's primary care physician.
- **Year**: The year of the claim (Y1, Y2, Y3).
- **Specialty**
- **PlaceSvc**: Place where the member was treated.
- **PayDelay**: The delay between the claim and the day the claim was paid for.
- **LengthOfStay**
- **DSFS**: Days since first service that year.
- **PrimaryConditionGroup**: A generalization of the primary diagnosis codes.
- **CharlsonIndex**: A generalization of the diagnosis codes in the form of a categorized comorbidity score.
- **ProcedureGroup**: A generalization of the CPT code or treatment code.
- **SupLOS**: A flag that indicates if LengthOfStay is null because it has been suppressed.

### c. Labs Table
Contains certain details of lab tests provided to members.

### d. RX Table
Contains certain details of prescriptions filled by members.

### e. DaysInHospital Tables - Y2 and Y3
Contains the number of days of hospitalization for each eligible member during Y2 and Y3 and includes:
- **MemberID**
- **ClaimsTruncated**: A flag for members who have had claims suppressed. If the flag is 1 for member xxx in DaysInHospital_Y2, some claims for member xxx will have been suppressed in Y1.
- **DaysInHospital**: The number of days in hospital Y2 or Y3, as applicable.
These tables are intended for use by entrants to train and validate their algorithms. DaysInHospital Tables are based on the Claims Table with admissions in Y2 or Y3, as applicable. As a privacy measure, any member who spent more than two weeks in hospital is grouped; they are treated as though they spent 15 days in hospital.

### f. Target - DaysInHospital_Y4
Does not include DaysInHospital. DaysInHospital data for Y4 are to be filled in by entrants to produce entries. See SampleEntry.csv as an example.
