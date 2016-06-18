# GA_Summary
Graduate Attributes Summary

This spreadsheet is intended to be used in conjunction with the ICDT to summarize graduate attributes collection across an entire program each year.

Currently, it requires manual manipulation of the data as follows:

* Copy the ICDT summary page for each course where graduate attributes collection occurred in the "Course-x" worksheets.
  + copy the ICDT file to the same directory as GA_Summary and save as "Gradesheet.xlsm" and click "Populate"
  + ensure that the "Instruction Level" fields have been entered.
  + currently, the graduate attributes are reported as an average of the individual assessments
* Once all of the individual course summaries have been entered, they are automatically summarized in the "Summary" and the "Data" worksheets.
  + Summary - please do not change this worksheet; it lists all graduate attributes results from the course summaries
  + Data - this worksheet is a duplicate of the "Summary" that is used to sort the data for presentation
* The "Data" worksheet can be used to prepare the data for presentation in a graphical format
  + Sort entire table on "Instruction List" (column E) Z-A
  + Sort populated table on "R" (column B) smallest-to-largest
  + Plot as column chart (potentially more than one)
  + Selected the data for plotting ("column" appears to work well for this)

The longer term plan is to automate this process.

#Gradesheet-GA-CI
Integrated Course Design Tool (ICDT)

This tool is intended to assist instructors with course planning by linking together course learning outcomes, teaching & learning activities, and assessments. The rationale is to report on student achievement in the context of the Engineers Canada Accreditation Board’s graduate attributes and use this information for continual improvement.

The tool is based on the principle of "constructive alignment": i.e., the link between intended learning outcomes, teaching and learning activities, and classroom assessment. The spreadsheet (Gradesheet-GA-CI.xlsm) is implemented using four main worksheets:

* LO (Learning Outcomes)
  + This worksheet is used to specify the course learning outcomes and their links to the CEAB graduate attributes and instruction levels.
  + The macro "Macro_frmOutcomes" (accessed by clicking the "New Learning Outcome" button) implements a Userform that assists the instructor with the setup of this worksheet.
* Grades (Class Gradesheet)
  + This worksheet is used as the grade collection spreadsheet for the course.
  + The macro "Macro_frmGrades" (accessed by clicking the "New Grade Component" button) implements a Userform that assists the instructor with the setup of this worksheet.
* One (First Detailed Grade Component)
  + This worksheet is used to collect detailed grade assessments for a single grade component.
  + The grade component is specified in the "Grades" worksheet using the "Link to -->" field (i.e., by specifying "One", worksheet "One" is used to enter the grade elements for this assessment).
  + The macro "Macro_frmOne" (accessed by clicking the "New Grade Component" button) implements a Userform that assists the instructor with the setup of this worksheet.
* Summary (Graduate Attributes Summary)
  + This worksheet provides a summary of the classroom assessments in the context of the 12 CEAB graduate attributes.
  + This is the worksheet that is read by GA_Summary.xlsm

  #ICDT_Test
  Integrated Course Design Tool

  This is a "macro-free" version of the IDCT.

  * LO (Learning Outcomes)
    + learning outcomes entered directly
    + drop-down boxes used to select graduate attributes and instruction levels
  * Grades (Class Gradesheet)
    + similar functionality to Gradesheet-GA-CI for the classlist and aggregate Grades
  * One (First Detailed Grade Component)
    + similar functionality to Gradesheet-GA-CI
    + learning outcomes are selected from a drop-down rather than a Userform
  * LO Summary (Learning Outcomes Summary)
    + class performance summarized by learning outcomes
    + capability added to easily hide learning outcome fields that are not used
  * GA Summary (Graduate Attributes Summary)
    + class performance by graduate attributes
    + capability added to easily hide graduate attributes that are not used
