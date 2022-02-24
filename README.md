# Covid-19 Reinfections in Bulgaria - 2020-2021 Period

 ### Repository for Reinfections in Bulgaria during the 2020-2021 period.

The current repospitory contains some datasets relating to the Covid-19 pandemic in Bulgaria during the 2020-2021 period.

`Disclaimer:`
````
Most datasets were provided directly by the Ministry of Health and contained sensitive infromation.
Datasets in current repository have been anonymized and/or aggreagated to protect the identities and medical history of people infected with Covid-19 in Bulgaria.
````
****

### For most files, the following periods are defined:

* **Period 1** - This is considered to be the alpha wave in Bulgaria and is defined as the period between: 15-01-2021 and 30-06-2021.

* **Period 2** - This is considered to be the delta wave in Bulgaria and is define as tje period between 01-07-2021 and 25-OCT-2021.

    The reason for this is that the file provided for General infections has a cut-off date of 05-11-2021

****

### The *input folder* contains infections, hospitalizations and deaths for the general population in Bulgaria and includes:
 

1. **breathing_reanimation_alpha_delta.csv** - File contains the counts of breathing assistance per breathing assistance type, per age group and period.
2. **deceased_alpha_delta_without_oc_cov.csv** - File contains the counts of deceased people aggregating across oc_cov status, per age group and period.

    The ``oc-cov`` status represents a binary between died due to Covid-19 (``cov``) and died with Covid-19 (``noncov``).

3. **deceased_alpha_delta.csv** - File contains the counts of deceased people separated between oc_cov groups, per age group and period.
The oc-cov status represents a binary between died due to Covid-19 (``cov``) and died with Covid-19 (``noncov``).
4. **hospitalized_alpha_delta.csv** - File contains the counts of hospitalized people separated between per age group and period.
5. **infections_alpha_delta.csv** - File contains the counts of infected people separated between per age group and period.

****
### The *output folder* contains datasets used for analysis and contain:

1. **BG_Vaccinated_Infections_Periods[3].csv** - file contains a combination between the following files:
   1. deceased_alpha_delta.csv
   2. hospitalized_alpha_delta.csv
   3. infections_alpha_delta.csv

2. **infected_hospitalized_deceased[cov-only]_combined.csv** - file contains counts for infections, hospitalizations and deaths per period per age group.

3. **Reinfections_blinded.csv** - contains a blinded list of reinfected individuals. Their personal information has been blinded by:
   1. Setting age at 10 year intervals
   2. Removing gender
   3. Obfuscating exact dates to month-year values
   4. Breathing re-animation has been reduced to a binary option (yes or no), instead of individual list of possible breathing re-animation techniques
   5. Existing listed comorbidities of hospitalized individuals has been ommitted