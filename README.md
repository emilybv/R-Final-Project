# SISE2601 Project data description
================
Team no. 17

## Dataset: Social Media Mental Health Survey (SMMH)

### Columns Description

1. **row_id**: Unique identifier for each row (numerical).
2. **timestamp**: Timestamp indicating when the survey response was recorded (date-time).
3. **age**: Respondent's age (numerical).
4. **gender**: Respondent's gender (categorical).
5. **rel_status**: Respondent's relationship status (categorical).
6. **occ_status**: Respondent's occupation status (categorical).
7. **uses_social_media**: Whether the respondent uses social media (yes/no).
8. **avg_time_on_sm**: Average time the respondent spends on social media every day 
(categorical, in hours).
9. **sm_without_purpose_adhd**: How often the respondent uses social media without a specific purpose 
(ordinal, scale of 1 to 5).
10. **sm_distraction_adhd**: How often the respondent gets distracted by social media when busy 
(ordinal, scale of 1 to 5).
11. **restless_without_sm_anx**: Whether the respondent feels restless if they haven't used social
 media in a while (ordinal, scale of 1 to 5).
12. **easily_distracted_adhd**: Respondent's self-rated level of distraction (ordinal, scale 
of 1 to 5).
13. **worry_bother_anx**: Respondent's self-rated level of being bothered by worries (ordinal, scale 
of 1 to 5).
14. **difficult_concentration_adhd**: Whether the respondent finds it difficult to concentrate on 
things (ordinal, scale of 1 to 5).
15. **compare_to_others_se**: How often the respondent compares themselves to successful people
 through the use of social media (ordinal, scale of 1 to 5).
16. **feel_about_comparison_se**: How the respondent feels about the comparisons mentioned in the
 previous question (ordinal, scale of 1 to 5).
17. **seek_validation_se**: How often the respondent seeks validation from social media (ordinal,
 scale of 1 to 5).
18. **feel_depressed_depr**: How often the respondent feels depressed or down (ordinal, scale of 
1 to 5).
19. **interest_fluctuate_depr**: Frequency of fluctuations in the respondent's interest in daily 
activities (ordinal, scale of 1 to 5).
20. **sleep_issues_depr**: Frequency of sleep issues faced by the respondent (ordinal, scale of 
1 to 5).
21. **university_affiliated**: Whether the respondent is affiliated with a university (binary: 0 or 1).
22. **private_affiliated**: Whether the respondent is affiliated with a private 
organization (binary: 0 or 1).
23. **not_affiliated**: Whether the respondent is not affiliated with any specific organization
(binary: 0 or 1).
24. **school_affiliated**: Whether the respondent is affiliated with a school (binary: 0 or 1).
25. **company_affiliated**: Whether the respondent is affiliated with a company (binary: 0 or 1).
26. **government_affiliated**: Whether the respondent is affiliated with a government organization 
(binary: 0 or 1).
27. **uses_facebook**: Whether the respondent uses Facebook (binary: 0 or 1).
28. **uses_twitter**: Whether the respondent uses Twitter (binary: 0 or 1).
29. **uses_instagram**: Whether the respondent uses Instagram (binary: 0 or 1).
30. **uses_youtube**: Whether the respondent uses YouTube (binary: 0 or 1).
31. **uses_discord**: Whether the respondent uses Discord (binary: 0 or 1).
32. **uses_reddit**: Whether the respondent uses Reddit (binary: 0 or 1).
33. **uses_pinterest**: Whether the respondent uses Pinterest (binary: 0 or 1).
34. **uses_tiktok**: Whether the respondent uses TikTok (binary: 0 or 1).
35. **uses_snapchat**: Whether the respondent uses Snapchat (binary: 0 or 1).
36. **adhd_score**: Composite score indicative of ADHD tendencies (numerical).
37. **depression_score**: Composite score indicative of depression (numerical).
38. **self_esteem_score**: Composite score indicative of self-esteem issues (numerical).
39. **anxiety_score**: Composite score indicative of anxiety (numerical).
40. **overall_mental_health_score**: Composite score indicative of overall mental health status
 (numerical).

### Data Overview

The data consists of 12 Likert scale based questions columns giving us points that measure either 
frequency or intensity of various mental illnesses aspects. A low score of 1 generally indicates low
frequency or intensity, and a high score of 5 typically indicates high frequency or intensity. 
As mentioned, each column describes a question relating to a different mental illness and ends with
one of the following accordingly: `depr` - depression, `se` - self esteem, `adhd` - ADHD,
`anx` - anxiety. There are 4 questions relating to ADHD, 3 to depression, 3 to anxiety and 2 to
self-esteem.
The other variables describe information about the individuals and social media platforms usage.

The data was checked to contain missing values or null values but it have had none.
However, please note that the column `affiliation_type` contains "N/A" values and according to the 
provider of the data set, in the questionnaire individuals could leave it blank indicating they are
not affiliated with anyone. Thus, we referred to this as one of the types of the affiliations.

At our first glance, we noticed there were columns storing values as a list in the data set. 
Therefore, we identified these columns by searching for columns with multiple values separated by
commas (using R code). After finding these, we separated the values into different binary columns.
In addition, we added a column of identifier for each row so that we recognize each unique individual.

In our project we are interested in the severance of each mental illness of each particular group,
so we calculated the total score for each mental illness for each person as well as the total score
as a general mental well-being score.
