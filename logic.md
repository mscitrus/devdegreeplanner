1. Courses are assigned values based on entry in courselist. This gives them a score for how often they are offered and how many courses they serve as a prereq for. If used for an organization, this would be controlled by them.
2. The requirements for a degree are entered. This is where manual prioritization happens, and where students mark any courses they havea already completed. This would be controlled by a department/college.
3. Plan generation. Student generates a plan using the data from course list and catalog requirements.
    a. Student selects a starting term (fall, spring, summer, etc) and a year.
    b. Student selects full or part-time (for grads, 9 hours is full; part-time allows at most 2 classes)
    c. Begin sorting classes for plan. For each semester, the system will use the following process:
        1. Determine the number of spots to be filled on the schedule (how many classes to take).
        2. Select the highest ranking class.
        3. If the course is not offered that semester, move down the ranking to the highest scoring offered class.
        4. If the prerequisites for that course are not completed, move down the ranking.
        5. Go back to step 2. Repeat until semester is full.

Scoring system:
Manual priority                 +5
Odd/Even-numbered years only    +4
One semester only               +3
Two semesters only              +2
Offered every semester          +1
Dissertation/capstone           ALWAYS 0



Schema

CourseDB:
Prefix
CourseNum
Title
Fall
Spring
Summer
YrPattern
Prereqs


DegreeDB:
CoursesRequired
CoursesRanked
CoursesCompleted
CourseManualPriority

PlansDB:
StudentName
EnrollmentLvl
Semesters