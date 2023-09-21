# First_project 
Product Manager Vasiliy has asked you to analyze completed lessons and answer the following questions:

How many students successfully completed only one course? (Successful completion means passing the course in the exam).

Identify the most challenging and the easiest exams: find courses and exams within the course that have the lowest and highest completion rates*. 

Determine the average time to complete exams for each subject (considering the student's last successful exam completion). 

Identify the most popular subjects (TOP-3) based on the number of registrations. Also, find subjects with the highest attrition rates (TOP-3). 

Using pandas, during the period from the beginning of 2013 to the end of 2014, identify the semester with the lowest course completion rates and the longest average course completion times. 

Often, for quality audience analysis, segmentation-based approaches are used. Using Python, create adapted RFM clusters of students to qualitatively assess your audience. In adapted clustering, you can choose the following metrics: R - average time to complete one exam, F - course completion rates, M - average score obtained on exams. Describe in detail how you created the clusters. For each RFM segment, establish boundaries for recency, frequency, and monetary metrics for cluster interpretation. You can find the approach description here.

To solve the task, conduct preliminary data analysis and formulate what should be considered a course. You can justify your choice with facts of exam completion, student distribution, and a unique course identifier.

*Completion rate = number of successful exams / number of all attempts to pass the exam

Files:

assessments.csv — This file contains information about test scores. Typically, each subject in a semester includes a series of tests with scores, followed by a final exam test (exam).
code_module — subject identification code.
code_presentation — semester (Identification code).
id_assessment — test (Identification number of the assessment).
assessment_type — test type. There are three types of assessment: teacher assessment (TMA), computer assessment (СМА), course exam (Exam).
date — information about the final test submission date. Calculated as the number of days from the start of the semester. The start date of the semester is number 0 (zero).
weight — test weight in % of the course grade. Usually, exams are considered separately and have a weight of 100%; the sum of all other scores is 100%.

courses.csv — the file contains a list of subjects by semester.
code_module — subject (identification code).
code_presentation — semester (identification code).
module_presentation_length — semester duration in days.

studentAssessment.csv — this file contains student test results. If a student does not submit work for assessment, the result is not recorded in the table.
id_assessment — test (identification number).
id_student — student identification number.
date_submitted — date of test submission by the student, measured as the number of days from the start of the semester.
is_banked — fact of test transfer from the previous semester (sometimes courses are retaken by students returning from academic leave).
score — student's score on this test. The range is from 0 to 100. A score below 40 is a failing grade.

studentRegistration.csv — this file contains information about when a student registered for a course in the semester.
code_module — subject (identification code).
code_presentation — semester (identification code).
id_student — student identification number.
date_registration — student registration date. This is the number of days measured from the start of the semester (e.g., a negative value of -30 means that the student registered for the course 30 days before it started).
date_unregistration — date of student course unregistration. For students who have completed the course, this field remains empty.
