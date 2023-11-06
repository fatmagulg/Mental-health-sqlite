# Mental-health-sqlite
SQL assignment done as part of a Level 4 Data Analytics Bootcamp.

This dataset is an Open Source Mental Illness (OSMI) data. 

It has been collected using surveys from 2014, 2016, 2017, 2018 and 2019. 

The surveys are a way of understanding the mental health situation and the frequency of mental health disorder in the tech industry. 

The dataset is available in sqlite format and can be downloaded from [here](https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry)

Some preprocessing was performed before making the dataset available: similar questions were merged together, values for answers were made consistent (for example  1 == 1.0), and spelling errors were fixed. 
The raw data was processed using Python, SQL and Excel for cleaning and manipulation (prior to this work).

The database contains three tables: `Survey`, `Question`, and `Answer`.

  1. **Survey**, containing columns:
    - `PRIMARY KEY INT SurveyID`
    - `TEXT Description`


  2. **Question**, containing columns: 
    - `PRIMARY KEY QuestionID`
    - `TEXT QuestionText`


  3. **Answer**, containing columns:
    - `PRIMARY/FOREIGN KEY SurveyID`
    - `PRIMARY KEY UserID`
    - `PRIMARY/FOREIGN KEY QuestionID`
    - `TEXT AnswerText`


`SuveyID` column contains the survey year i.e. 2014, 2016, 2017, 2018, 2019 and the same question can be used for multiple surveys. 

Answer table is composite, with multiple primary keys. Here, `SurveyID` and `QuestionID` are [`FOREIGN KEYS`](https://www.w3schools.com/sql/sql_foreignkey.asp)

Some questions can contain multiple answers, thus the same user can appear more than once for any given QuestionID.

You can find more information [here](https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry).
