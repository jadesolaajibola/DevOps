PRODUCT REQUIREMENTS DOCUMENT
STUDENT ATTENDANCE
MANAGEMENT SYSTEM
Course Code: COS-209
Group 11
1. Introduction
1.1 Background of the Project
Attendance monitoring is an important administrative activity in universities. It helps lecturers keep track of students' participation in lectures and provides information that may be used when reviewing students' academic engagement. In many learning environments, attendance is still recorded manually by calling names, passing around paper sheets or asking students to sign an attendance register. Although these methods are familiar, they can require considerable class time and may create difficulties when records need to be organised, checked or retrieved.
The Student Attendance Management System is proposed as a web-based application that uses QR code technology to make this process more efficient. Instead of relying on paper registers, a lecturer will create an attendance session for a selected course and display a QR code. Students will use their devices to scan the displayed code and submit their attendance through the system. The application will validate the code and record the attendance against the appropriate student, course and session.
1.2 Purpose of the Document
This Product Requirements Document (PRD) describes the purpose, users, scope, features and quality expectations of the proposed system. It provides a shared reference for the project group and anyone involved in planning, designing, implementing and evaluating the application. It explains what the system is expected to do without prescribing every detail of how the software must be programmed.
1.3 Product Overview
The application will provide separate experiences for lecturers and students. Lecturers will manage attendance sessions and review the records collected for their courses. Students will register attendance by scanning valid QR codes and will be able to review their attendance history and percentages. The system will use a database to store the information required for accounts, courses, sessions and attendance records.
1.4 Intended Benefits
The intended benefits include reducing the time spent taking attendance, making records easier to retrieve, limiting common manual recording errors and giving students clearer access to their attendance information. The system is intended to support the existing teaching and learning process rather than replace the academic responsibilities of lecturers.
 
2. Problem Statement and Project Justification
2.1 Description of the Problem
Traditional attendance-taking methods can be slow, particularly in courses with large numbers of students. A lecturer may need to call each student's name, wait for responses and manually mark a register. This activity can interrupt the lesson and reduce the time available for teaching. When paper records are used, the lecturer may also need to organise several sheets for different courses and dates.
Manual records can be affected by human error. A name may be missed, a mark may be placed in the wrong row, or information may be difficult to read. Paper registers can also be misplaced or damaged. In addition, checking a student's attendance over several weeks may require the lecturer to review many separate records and calculate the total manually.
Another challenge is that students may not have a convenient way to monitor their attendance throughout the semester. If attendance information is kept only in a paper register or separate lecturer records, students may have to ask for an update. This can make it difficult for them to identify attendance concerns early.
2.2 Proposed Solution
The proposed system addresses these challenges by providing a central digital platform for attendance registration and monitoring. Lecturers will create a session for a course, and the system will generate a QR code that changes automatically every 30 seconds. The attendance session will remain open for 15 minutes. Students must scan a valid code during the session to register their attendance. The system will validate submissions and prevent the same student from recording attendance more than once for a particular session.
2.3 Project Justification
A QR-based approach offers a practical way to connect a classroom attendance activity with a digital record. It reduces the need for lecturers to process paper registers and gives students a direct way to submit and review their records. Storing information in a database also makes it easier to organise attendance by student, course and session. These improvements support more consistent record keeping and can make attendance information more accessible to authorised users.
2.4 Limitations to Recognise
The system depends on access to a suitable device and a working connection to the application. A QR code scan alone does not prove a student's physical location or identity beyond the account and validation measures implemented by the system. The project will therefore focus on reliable account access, valid session codes and duplicate prevention, while recognising that additional verification may be considered in a future version.
 
3. Project Aim, Objectives and Success Measures
3.1 Project Aim
The main aim of the project is to develop a web-based Student Attendance Management System that uses changing QR codes to make the recording, storage and monitoring of university attendance faster, more organised and more reliable.
3.2 Specific Objectives
•	Automate the attendance-taking process by allowing students to register through QR code scanning.
•	Reduce errors associated with handwritten registers and manual transfer of attendance information.
•	Enable lecturers to create attendance sessions for courses and monitor submitted attendance records.
•	Allow students to view their attendance history and calculated attendance percentages.
•	Improve the organisation and reliability of attendance information through centralised digital storage.
•	Restrict access to system functions according to whether a user is a student or a lecturer.
•	Prevent duplicate attendance submissions for the same student and attendance session.
3.3 Measurable Success Criteria
The project will be considered successful when the main user activities can be completed as intended. A lecturer should be able to sign in, select an assigned course, start a session and display its QR code. The code should refresh automatically every 30 seconds, and the session should close after 15 minutes. A student should be able to sign in, scan a valid code and receive a clear indication that attendance has been recorded. A second submission for the same session should not create another attendance record.
The system should also calculate attendance percentages consistently from the stored records. Students and lecturers should be able to access their respective dashboards, and users should not be able to open functions that are not permitted for their roles. These criteria provide practical checks that can be used during system testing and project evaluation.
3.4 Relationship Between Objectives and Features
Each objective is supported by one or more system features. QR code generation and scanning support automation; validation and duplicate checks support record reliability; role-based dashboards support appropriate access; and attendance history and reports support monitoring. The objectives are therefore connected directly to the features described in the functional requirements.
 
4. Target Users and User Requirements
4.1 Primary User Groups
The system has two main categories of users: lecturers and students. Each category has different responsibilities and should be presented with the functions needed to carry out those responsibilities. The application must identify the user's role after login so that the correct dashboard and permissions can be applied.
4.2 Lecturer Requirements
Lecturers need a straightforward way to manage attendance for the courses assigned to them. After signing in, a lecturer should be able to view the relevant course list, select a course and create a new attendance session. The lecturer should then be able to display the generated QR code for students to scan. During the session, the lecturer should be able to see which students have successfully registered. After the session, the lecturer should be able to review attendance information and access reports for the course.
•	Securely access a lecturer account using registered credentials.
•	View courses assigned to the lecturer.
•	Start an attendance session for a selected course.
•	Display the automatically changing QR code during the session.
•	Monitor submitted attendance records.
•	View attendance reports for relevant courses and sessions.
4.3 Student Requirements
Students need a simple process for registering attendance and checking their records. After signing in, a student should be able to view registered courses and use a device camera or supported scanning function to scan the lecturer's QR code. The student should receive feedback showing whether the submission was successful or why it could not be accepted. The student dashboard should provide access to attendance history and percentages so that the student can monitor participation over time.
•	Securely access a student account using registered credentials.
•	View registered courses.
•	Scan a valid QR code during an active attendance session.
•	Receive confirmation or an understandable error message after scanning.
•	View attendance history and attendance percentages.
•	Review attendance statistics presented in a clear format.
4.4 Usability Expectations
Both user groups should be able to understand the main actions without extensive technical knowledge. Labels should be clear, navigation should be consistent, and important feedback should be easy to notice. The design should avoid unnecessary steps, especially during the short period in which an attendance session is active.
 
5. Functional Requirements: Accounts and Dashboards
5.1 Authentication and Account Access
The system must provide a login process for registered students and lecturers. Users will enter their registered credentials, and the application will verify them before granting access. Login information must be handled securely, and the system should not reveal sensitive account details in error messages. Where a login attempt fails, the application should display a clear message and allow the user to try again.
Authentication must be connected to role-based access. A student account should open the student dashboard, while a lecturer account should open the lecturer dashboard. A user should only be able to access functions permitted for their assigned role. For example, students may register attendance but must not be given the lecturer function for generating QR codes.
5.2 Lecturer Dashboard
The lecturer dashboard will serve as the main working area for attendance management. It should display the courses assigned to the lecturer and provide a clear way to select a course. From the selected course, the lecturer should be able to start an attendance session, view the active QR code and monitor students who have registered. The dashboard should also provide access to attendance reports so that records can be reviewed after a session has ended.
The dashboard should distinguish between an active session and a completed session. During an active session, the QR code and session status should be visible. Once the 15-minute session period has ended, the application should indicate that attendance registration is closed. This helps lecturers understand whether students can still submit attendance.
5.3 Student Dashboard
The student dashboard will provide an overview of the student's registered courses and attendance information. It should include access to attendance history, calculated percentages and visual statistics. The information should be organised so that a student can identify the course to which each attendance record belongs and understand how their percentage has been calculated.
5.4 Feedback and Notifications
The application should provide feedback after important actions. Examples include successful login, successful attendance registration, an invalid or expired QR code, a closed session and an attempted duplicate submission. Messages should be written in plain language and should help users understand what happened and what action, if any, they can take next.
 
6. Functional Requirements: QR Code Attendance
6.1 Creating an Attendance Session
Only an authenticated lecturer should be able to create an attendance session. The lecturer will select one of the courses assigned to them and start the session. The system should associate the session with the selected course and record the session's start time and status. This information provides the context needed to identify which class meeting a student's attendance belongs to.
6.2 QR Code Generation and Refresh
When a session begins, the system will generate a QR code for attendance registration. The QR code must automatically change every 30 seconds while the session is active. The changing code is intended to reduce the usefulness of an old screenshot or previously displayed code. The code should represent a valid attendance session and should be checked by the application before a record is accepted.
The QR code must be linked to the correct course and session. A code should not be accepted if it is invalid, has expired or belongs to a session that is no longer active. The application should make the current code easy for students to scan from the lecturer's display.
6.3 Session Duration
Each attendance session should last for 15 minutes. The system should track the time from the start of the session and stop accepting new attendance submissions when the allowed period ends. The lecturer dashboard should show the session status, and students who attempt to submit after the session has closed should receive an appropriate message.
6.4 Student Scanning and Validation
A student must be logged in before registering attendance. After scanning the displayed QR code, the application should check that the code is valid, that the related session is active and that the student is eligible to submit an attendance record for that session. If the checks are successful, the system should save the attendance record and display confirmation. If validation fails, the system should reject the submission and explain the reason in a clear way.
6.5 Duplicate Prevention
The system must prevent a student from registering attendance more than once for the same session. This check should be performed before a new record is saved. If a matching attendance record already exists, the application should retain the original record and inform the student that attendance has already been registered. The duplicate check should be based on the student and session, rather than only on the QR code currently displayed.
 
7. Non-Functional Requirements
7.1 Usability
The application should be easy to learn and navigate for users with different levels of technical experience. Common tasks, such as logging in, selecting a course and scanning a code, should be presented clearly. The interface should use consistent layouts, readable text and understandable labels. Error messages should explain the issue without relying on complicated technical language.
7.2 Performance and Responsiveness
The system should respond promptly to normal user actions, including login, opening dashboards, loading course information and submitting attendance. QR code updates should occur at the required 30-second interval without requiring the lecturer to refresh the page manually. The application should be designed to handle the expected classroom use in which several students may submit attendance within a short period.
7.3 Security and Access Control
The system must protect users' login information and restrict access to authorised users. Student and lecturer roles must be enforced consistently across the application. Students should not be able to generate QR codes or view another student's private attendance history. Lecturers should be able to view attendance information relevant to their assigned courses. The system should also validate submitted data rather than trusting information received from a user's device.
7.4 Reliability and Data Integrity
Attendance records should be stored reliably and remain associated with the correct student, course and session. The application should avoid creating incomplete or duplicate records when a user submits a request more than once. Attendance calculations should be based on the records stored in the database and should be consistent whenever the same data is reviewed.
7.5 Compatibility and Accessibility
The web application should work on computers and mobile devices so that lecturers can display QR codes and students can scan them using suitable devices. Pages should adjust to different screen sizes, and essential actions should remain accessible on smaller screens. The interface should use sufficient text contrast and clear visual indicators to make information easier to read.
7.6 Maintainability
The application should be organised in a way that allows the project team to identify and update individual features without unnecessarily affecting unrelated parts of the system. Clear naming, consistent code structure and appropriate documentation will support testing, correction of errors and future improvements.
 
8. Technology Stack and Data Requirements
8.1 HTML
HTML will be used to define the structure and content of the web pages. It will provide the elements used for forms, headings, navigation, buttons, tables and dashboard sections. A clear HTML structure will help ensure that the application content is organised and understandable.
8.2 CSS
CSS will be used to control the appearance and layout of the application. It will define colours, spacing, typography, alignment and responsive behaviour. The styling should remain consistent across the lecturer and student dashboards while allowing each page to present the functions relevant to its user.
8.3 JavaScript
JavaScript will provide interactive behaviour within the application. It can support actions such as responding to button clicks, updating dashboard content, managing the QR code display and handling user interactions. It will also help connect the user interface to the application's attendance registration process.
8.4 QR Code Technology
QR code technology will be used to provide a scannable representation of the active attendance session. The system will generate the code for lecturers and provide a scanning process for students. The code must change every 30 seconds, and the application must validate it before accepting attendance. QR code generation and scanning are therefore central parts of the attendance workflow.
8.5 Database Requirements
A database will store the information needed to operate the system. This includes student details, lecturer details, course information and attendance records. The system will also need to retain information about attendance sessions so that each record can be connected to the correct class meeting. Access to stored information should be controlled according to user roles.
8.6 Main Data Entities
•	Student: identifies a student account and the student's registered information.
•	Lecturer: identifies a lecturer account and the courses associated with that lecturer.
•	Course: stores the course information needed to organise attendance.
•	Attendance session: records the course, session timing and session status.
•	Attendance record: connects a student to a particular session and indicates that attendance was successfully registered.
The relationships between these data entities should support accurate retrieval and reporting. For example, a lecturer should be able to retrieve records for a course session, while a student should be able to retrieve their own attendance history across registered courses.
 
9. System Workflow and Project Scope
9.1 Lecturer Workflow
The process begins when the lecturer opens the web application and logs in using registered credentials. After authentication, the lecturer dashboard displays the courses assigned to that account. The lecturer selects the course for which attendance is required and starts a new attendance session. The system creates the session, generates a QR code and displays it for students. While the session remains active, the QR code changes automatically every 30 seconds. The lecturer can monitor the students whose attendance has been registered. At the end of the 15-minute period, the session closes and the lecturer can review the resulting attendance information.
9.2 Student Workflow
A student begins by logging in to the application. The student then attends the relevant class and scans the QR code displayed by the lecturer using a suitable device. The application receives the scanned information and checks whether the code is valid and the session is still open. It also checks whether the student has already registered attendance for that session. If all checks pass, the system stores the attendance record and displays a success message. If a check fails, the application rejects the submission and displays an appropriate explanation. The student can later open the dashboard to review attendance history and percentages.
9.3 Overall Workflow Summary
•	The lecturer logs in and selects an assigned course.
•	The lecturer starts an attendance session.
•	The system generates and displays a QR code.
•	The QR code refreshes automatically every 30 seconds.
•	Students log in and scan the displayed code.
•	The system validates the code and checks for an existing record.
•	Valid attendance is saved; invalid or duplicate submissions are rejected.
•	The session closes after 15 minutes.
•	Students review their attendance information, while lecturers review reports.
9.4 Project Scope
The project will focus on student and lecturer authentication, course management, QR-code attendance registration, attendance tracking, attendance percentage calculation, dashboards and attendance reports. These functions form the core of the proposed system and are necessary to support the main user activities described in this document.
9.5 Items Outside the Current Scope
The current project description does not specify features such as biometric identification, automatic integration with a university-wide student information system, payment processing, timetable creation or advanced location tracking. These features should not be treated as confirmed requirements for the present version. They may be considered separately if the project scope is expanded in the future.
 
10. Expected Outcome, Testing and Conclusion
10.1 Expected Outcome
At the end of development, the project is expected to provide a functional web-based attendance management application for students and lecturers. Lecturers should be able to create attendance sessions, display changing QR codes, monitor registrations and view reports. Students should be able to scan valid codes, register attendance and monitor their attendance history and percentages. The system should provide a more organised alternative to paper-based attendance recording.
10.2 Testing and Evaluation
Testing should confirm that the system performs the required tasks correctly. Authentication testing should verify that registered users can log in and that access is limited according to their roles. Dashboard testing should confirm that students and lecturers see the appropriate information and functions. QR code testing should confirm that codes refresh every 30 seconds and that invalid or expired codes are rejected. Session testing should confirm that attendance registration closes after 15 minutes.
Attendance registration testing should check that a valid scan creates a record linked to the correct student and session. Duplicate testing should confirm that a student cannot create multiple records for the same session. Calculation testing should compare displayed attendance percentages with the underlying attendance records. Compatibility testing should examine the application on computer and mobile screen sizes. These checks will help the group identify problems before presenting the completed project.
10.3 Success Criteria
•	Lecturers can successfully create attendance sessions for their courses.
•	QR codes change automatically every 30 seconds during an active session.
•	Each attendance session remains open for 15 minutes.
•	Students can register attendance by scanning a valid QR code.
•	Invalid, expired and duplicate submissions are not accepted.
•	Attendance percentages are calculated correctly from stored records.
•	Students and lecturers can access their respective dashboards and permitted information.
10.4 Conclusion
The Student Attendance Management System is designed to improve the way attendance is recorded and monitored in a university environment. By using changing QR codes, a defined 15-minute session period, account authentication and centralised attendance records, the application aims to reduce the difficulties associated with manual attendance-taking. Its lecturer and student dashboards will make attendance information easier to manage and review. The requirements in this document provide a foundation for the design, development and testing of the proposed system.
11. Future Considerations
After the core system has been completed and tested, the project team may review possible improvements based on user feedback. Such improvements could include more detailed report filters, downloadable attendance reports, additional accessibility refinements or integration with other university systems. These are future considerations only and do not change the requirements of the current project.
