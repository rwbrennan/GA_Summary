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

  This is a "macro-free" version of the IDCT. Although Gradesheet-GA-CI is relatively straight-forward, some instructors may be uncomfortable using a macro-enabled spreadsheet for grade collection. This macro-free version has all of the same functionality as Gradesheet-GA-CI, with the addition of a learning outcomes summary.

  * LO (Learning Outcomes)
    + Learning outcomes are entered directly into the spreadsheet.
    + Drop-down boxes are used to select graduate attributes and instruction levels.
    + The learning outcome number is populated automatically: currently, a maximum of 24 learning outcomes can be entered.
  * Grades (Class Gradesheet)
    + This worksheet has similar functionality to Gradesheet-GA-CI for the class list and aggregate grades.
    + Unlike Gradesheet-GA-CI, the worksheet is protected so that the automatic calculations cannot be accidentally altered.
    + The instructor enters the name of the grade component (row 6), and the percentage weight (row 7). If the assessment is not being used for graduate attributes collection, the number of points for the assessment is entered directly in the left column ("Grade") along with the total (aggregate) score for each student on the assessment. The "Grade" column is automatically highlighted in green when this choice is made. If the assessment is chosen for graduate attributes collection, the instructor chooses the worksheet for the detailed assessment from the drop-down ("One-Four"). The "One-Four" column is automatically highlighted in green and is used for the grade calculation; the individual student grades for this assessment are now entered in the detailed grade component worksheet (e.g., worksheet "One").
  * One (First Detailed Grade Component)
    + This worksheet has similar functionality to Gradesheet-GA-CI for the detailed grade component assessments.
    + Unlike Gradesheet-GA-CI, the worksheet is protected so that the automatic calculations cannot be accidentally altered.
    + The instructor enters the grade elements (row 6), and number of points for the grade elements (row 7). The link between grade elements and learning outcomes are made using a drop-down (row 8) rather than a Userform.
    + The learning outcomes drop-down is automatically populated from the list of learning outcomes in the "LO" worksheet, and once selected, is automatically linked to the graduate attribute and the instruction level specified in "LO".
  * LO Summary (Learning Outcomes Summary)
    + This worksheet summarizes the overall class performance by course learning outcome.
    + The capability has been added to easily hide learning outcome fields that are not used (the "groups" on the left column).
  * GA Summary (Graduate Attributes Summary)
    + This worksheet summarizes the overall class performance by graduate attribute.
    + The capability has been added to easily hide graduate attribute fields that are not used (the "groups" on the left column).
