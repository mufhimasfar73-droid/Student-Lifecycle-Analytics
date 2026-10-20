🎗️📊# Student-Lifecycle-Analytics:                                                                                             
Excel and power bi project analyzing performance of students and university database(2025-2026).                                                                                                                                                         
🎗️📌*) PROJECT OVERVIEW:                                                                                                                                                                                                                                                                                                                                                           This project analyzes the student lifecycle in university, it includes student admission , departments and grades.This project also focusing on faculty's department and library loans.                                            Using EXCEL , i did removing duplicates,handling missing values , standardizing formats , creating calculated fields , filtering and sorting the data and also creating a pivot table.                                                  Using POWER BI, the data was visualized with a proper cleaning data.                                                                                                                                                                     
🎗️💡*) PROJECT OBJECTIVES:                                                                                                                                                                                                                                 The core objectives can be broken down into the following key pillars:

🔗1. Financial Monitoring & Revenue Tracking
Objective: Track and reconcile student fee collections across multiple payment channels (Bank Transfer, Online Gateway, Demand Draft, Credit Card, etc.).

Key Metrics: Monitoring total fee collections (over ₹120.3M across 1,201 recorded payments) to evaluate cash flow and payment channel efficiency.

🔗2. Operational Efficiency & Resource Management
Objective: Audit campus resource utilization—specifically tracking library book loans, return rates, and overdue inventories.

Key Metrics: Monitoring active vs. overdue library loans (e.g., tracking the ~18.5% outstanding loan rate) to optimize resource availability and implement automated reminder workflows.

🔗3. Student Demographics & Academic Tracking
Objective: Analyze student distribution, gender ratios, city-wise concentrations, and academic performance (enrollments, assignment submissions, grade points).

Key Metrics: Evaluating student geographic spread across major metropolitan hubs (such as Mumbai, Chennai, and Bengaluru) to guide targeted recruitment and institutional outreach.

🔗4. Strategic Decision-Making & Institutional Reporting
Objective: Provide an integrated "Academic & Operational Performance Dashboard" and pivot analyses to assist administrators in data-driven planning, process automation (e.g., automated fee and library reminders), and operational risk mitigation.                                                                                                                                                                                                                           
🎗️🎯*) DATA SOURCES:                                                                                                                                                                                                                                       👩‍🎓Excel practice data generators(2025-2026)                                                                                                                                                                                                📈Education & Academia(2025-2026)                                                                                                                                                                                    Domain: Student performance.                                                                                                                                                                                                                                                                                                         
🎗️⚠️*) PROBLEM STATEMENT:                                                                                                                                                                                                                                 "Educational institutions often struggle with fragmented tracking across student demographics, multi-channel fee collections, course enrollments, academic performance, and physical resource allocation (such as library inventories). Without an integrated data-driven system, administrators face blind spots in identifying revenue bottlenecks, high volumes of unreturned library assets (e.g., an 18.5% overdue loan rate), reliance on manual/legacy payment methods (such as Demand Drafts accounting for 31% of collections), and a lack of centralized operational visibility for strategic decision-making."                                                                                                                                                                                                           
🎗️📋*) ATTRIBUTE DETAILS:                                                                                                                                                                                                                                   "students:StudentID, Name, Date Of Birth, Gender, City.Faculty:FacultyID, Faculty Name, DepartmentID, Rank, Email.Courses:CourseID, Course Name, DepartmentID, Credits.Enrollments:StudentID, CourseID, Semester, Year.AssignmentSubmissions:StudentID, Submission Date, Grade Points, Grades.LibraryLoans:StudentID, Book Title, Loan Date, Return Date.Pivot Analysis:Pre-built cross-tabulations and summaries.FeePayments:StudentID, Amount, Payment Date, Semester, Year, Method.Dashboar:Academic & Operational Performance Dashboard."                                                                                                                                                         
🎗️🧪*) DATA PREPROCESSING STEPS:                                                                                                                                                                                                                                                                                                                                 🔗1. Handling Missing & Null Values
Drop Blank Rows & Padding: Remove completely empty trailing rows in large tables (such as the Students sheet, which contains over 1 million rows due to blank trailing space, but only 500 actual student records).

Impute or Filter Incomplete Records: Clean missing values in relational tables like Courses (missing course IDs or credits) and AssignmentSubmissions (missing submission dates or grade points) by either dropping null rows or imputing defaults based on course metadata.

🔗2. Data Cleaning & Formatting
Date Parsing & Standardization: Convert date attributes (Date Of Birth, Submission Date, Loan Date, Return Date, Payment Date) from text/object types into standardized datetime formats to enable chronological and cohort analysis.

Text & Categorical Cleaning: Trim whitespace, standardize casing for categorical text fields (e.g., City names, Gender, Semester, and payment Method), and ensure consistent ID formats (e.g., StudentID and CourseID).

🔗3. Removing Unnamed/Auxiliary Summary Columns
Isolate Raw Data from Summary Blocks: Strip out auxiliary inline summary blocks and placeholder columns (such as Unnamed: 4 to Unnamed: 11 found in AssignmentSubmissions, LibraryLoans, and FeePayments) which contain embedded statistics, notes, or empty cells, and recalculate them dynamically during analysis.

🔗4. Relational Integration & Merging
Key-Based Joins: Establish primary-foreign key relationships across sheets using unique identifiers:

Link Enrollments and FeePayments to Students using StudentID.

Link Enrollments and AssignmentSubmissions to Courses using CourseID.

Link Faculty to Courses and departments using DepartmentID.

🔗5. Feature Engineering & Validation
Derived Metrics: Compute derived features such as student age from Date Of Birth, total tuition paid per student, loan duration days from loan and return dates, and assignment grade point averages.

Duplicate Check: Audit datasets for duplicate records (e.g., duplicate fee transactions or multi-logged course enrollments) and drop redundancies to maintain data integrity.                                                                                                                                                                                               
🎗️🧩ANALISIS & visualizations:                                                                                                                                                                                                                                                                                                                                   Analytical Domain	Key Metric / Segment	Total Volume / Value	Percentage / Share:
Fee Revenue	Bank Transfer =	₹43,260,404.51	~35.9%
Online Gateway	          = ₹39,725,466.13	~33.0%
Demand Draft	            = ₹37,332,252.91	~31.0%
Student Demographics	Female Students	267	53.4%,Male Students	233	46.6%
Library Operations,Returned Books =	2,062	-81.5%
Overdue Books	=467	-18.5%.                                                                                                             The analysis has been compiled into an integrated multi-panel visualization dashboard , covering fee collection channels, city distributions, gender ratios, and library loan return rates                                                                                                                                                                 
🎗️🗝️*) KEY INSIGHTS:                                                                                                                                                                                                                                                                                                                                             🔗Fee Collections & Revenue:

Total collections amount to ₹120,318,123.55 across 1,201 total payment transactions.

Bank Transfer leads as the top collection channel with ₹43.26M (431 transactions), followed closely by Online Gateways at ₹39.73M (400 transactions) and Demand Drafts at ₹37.33M (370 transactions).

🔗Student Demographics:

Comprises 500 unique active students distributed across 7 major metropolitan hubs.

Gender Split: 267 Female students (53.4%) and 233 Male students (46.6%).

Top Cities: Led by Mumbai (77 students), Chennai (76 students), Bengaluru (74 students), and Delhi (74 students).

🔗Library Resource Utilization:

Tracks 2,529 total book loans across academic titles.

Return Status: 2,062 loans (81.5%) have been successfully returned, while 467 loans (18.5%) remain outstanding and overdue across 274 unique students.                                                                                                
🎗️🏁conclusion:                                                                                                                                                                                                                         🔗Balanced & Diversified Revenue Streams:

Fee collections totaling ₹120,318,123.55 are well-distributed across payment channels, led by Bank Transfers (₹43.26M / ~35.9%), Online Gateways (₹39.73M / ~33.0%), and Demand Drafts (₹37.33M / ~31.0%). While digital gateways and bank transfers dominate, the continued ~31% share of manual Demand Drafts highlights an opportunity for further digital adoption.

🔗Strong Metropolitan Reach & Balanced Demographics:

The institution serves a diverse body of 500 unique students with a balanced gender ratio (53.4% Female and 46.6% Male) spread evenly across major metropolitan hubs (Mumbai, Chennai, Bengaluru, Delhi, Hyderabad, Pune, and Kolkata), providing a strong foundation for targeted outreach and alumni networking.

🔗Operational Vulnerability in Resource Management:

While library resource utilization is high across 2,529 total loans, an 18.5% overdue rate (467 unreturned books held by 274 unique students) points to a clear operational bottleneck. Implementing automated reminder systems will be critical to safeguarding institutional assets.
