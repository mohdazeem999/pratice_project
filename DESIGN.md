
# LearnIQ — Design Document

> **AI-Powered Classroom Learning Intelligence and Personalized Improvement Platform**

---

## 1. Document Information

| Field | Details |
|---|---|
| Project | LearnIQ |
| Document | `DESIGN.md` |
| Version | `1.0` |
---

# 2. Product Overview

LearnIQ is an AI-powered classroom learning intelligence platform for Classes 5–12.

The platform transforms assessment responses into actionable learning information by identifying learning gaps, supporting targeted practice, measuring improvement, and recognizing meaningful student progress.

### Core Learning Cycle

```text
Assess
   ↓
Analyze
   ↓
Identify Learning Gaps
   ↓
Personalize
   ↓
Practice
   ↓
Reassess
   ↓
Measure Improvement
   ↓
Recognize
   ↓
Reward
   ↓
Continue Learning


---

3. Design Goals

The design should:

Make student learning status easy to understand.

Make assessments simple to start, complete, and submit.

Clearly communicate learning gaps.

Help teachers move from assessment results to intervention.

Make improvement visible over time.

Recognize progress, not only high marks.

Keep primary actions clear.

Maintain consistent navigation.

Support relevant loading, empty, error, and success states.

Never present unimplemented functionality as functional.



---

4. Target Users

4.1 Student

Students can:

Sign up and log in.

Complete onboarding.

Attempt assessments.

View results.

Understand learning gaps.

Complete targeted practice.

Take reassessments.

Track improvement.

Earn points and achievements.

Complete challenges.

View eligible rewards.


4.2 Teacher

Teachers can:

Manage classes.

Create or select assessments.

Assign assessments.

Monitor student performance.

View individual learning gaps.

View class-level learning gaps.

Assign targeted practice.

Monitor improvement.

View recognition and progress.


4.3 School Administrator

Administrators can:

Manage teachers and students.

Manage classes and subjects.

Manage approved rewards.

Manage reward inventory.

Manage reward redemptions.

Monitor school-level trends.



---

5. MVP Scope

Student

The core student journey is:

Sign Up / Login
       ↓
Onboarding
       ↓
Student Dashboard
       ↓
Assessment
       ↓
Results / Learning Intelligence
       ↓
Targeted Practice
       ↓
Reassessment
       ↓
Improvement Tracking
       ↓
Recognition / Points
       ↓
Rewards

Teacher

Teacher Login
       ↓
Class Selection
       ↓
Assessment Creation / Selection
       ↓
Assign Assessment
       ↓
Monitor Results
       ↓
Class Learning Map
       ↓
Student Learning Profile
       ↓
Targeted Intervention
       ↓
Reassessment
       ↓
Improvement Monitoring

Administrator:

Administrator Login
       ↓
User Management
       ↓
Class / Subject Management
       ↓
Reward Management
       ↓
Redemption Management
       ↓
School-Level Monitoring


---

6. Scope Control

The design must remain within the agreed LearnIQ classroom-learning MVP.

Do not add features simply because they are visually attractive or technically possible.

Do not present these as functional unless they are implemented and approved:

Career-development features

Unimplemented AI recommendations

Unimplemented XP systems

Unimplemented rankings

Future-scope functionality

Features outside the approved MVP


> Important: A mockup is design evidence. It is not proof that the underlying feature works.




---

7. Information Architecture

LearnIQ
│
├── Authentication
│   ├── Login
│   └── Sign Up
│
├── Onboarding
│
├── Student
│   ├── Dashboard
│   ├── Assessments
│   ├── Assessment Attempt
│   ├── Results
│   ├── Learning Gaps
│   ├── Practice
│   ├── Reassessment
│   ├── Progress
│   ├── Achievements
│   ├── Points
│   ├── Challenges
│   └── Rewards
│
├── Teacher
│   ├── Dashboard
│   ├── Classes
│   ├── Assessments
│   ├── Create / Assign Assessment
│   ├── Class Learning Map
│   ├── Student Profiles
│   ├── Intervention
│   ├── Improvement Tracking
│   └── Recognition
│
└── Administrator
    ├── Dashboard
    ├── Users
    ├── Classes / Subjects
    ├── Rewards
    ├── Redemptions
    └── Monitoring

Only approved MVP sections should be implemented.


---

8. Screen List

#	Screen	Role	Purpose

1	Login	All	Access the platform
2	Sign Up	Student/Teacher	Create an account
3	Onboarding	Student	Establish learning context
4	Student Dashboard	Student	Show current learning status
5	Assessment	Student	Complete assessment
6	Results	Student	Show performance and learning intelligence
7	Learning Gaps	Student	Show areas requiring improvement
8	Practice	Student	Complete targeted practice
9	Reassessment	Student	Measure improvement
10	Progress	Student	Show improvement over time
11	Recognition	Student/Teacher	Show learning achievements
12	Rewards	Student/Admin	Manage approved educational rewards
13	Teacher Dashboard	Teacher	Classroom overview
14	Class Learning Map	Teacher	Identify class-wide gaps
15	Student Profile	Teacher	Inspect individual progress
16	Assessment Management	Teacher	Create/assign assessments
17	Admin Dashboard	Admin	School-level management
18	User Management	Admin	Manage users
19	Reward Management	Admin	Manage rewards and inventory


> Remove screens that are not part of the approved MVP.




---

9. Student Screen Requirements

9.1 Login

Purpose

Allow existing users to access LearnIQ.

Required Elements

Email / username

Password

Login button

Sign-up link

Error feedback


States

Default

Loading

Invalid credentials

Authentication error

Success



---

9.2 Sign Up

Purpose

Allow new users to create an account.

Required Elements

Registration fields

Create account button

Login link

Validation feedback


States

Default

Loading

Validation error

Registration error

Success



---

9.3 Onboarding

Purpose

Collect the minimum information required to establish the student's learning context.

Required Elements

Grade / class

Relevant subject information

Required preferences

Continue button

Progress indicator where necessary


States

Default

Loading

Validation error

Completion success



---

9.4 Student Dashboard

Purpose

Provide a concise overview of the student's current learning activity.

Possible Content

Current performance

Pending assessments

Recent assessment

Learning gaps

Next learning action

Improvement summary

Points / achievements where implemented


States

Loading

Populated

Empty

Error



---

9.5 Assessment

Required Elements

Assessment title

Question

Answer controls

Progress indicator

Navigation

Submit button


States

Loading

Active

Validation error

Submission error

Submission success



---

9.6 Results / Learning Intelligence

Possible Content

Score

Topic performance

Concept strengths

Learning gaps

Possible mistake patterns

Improvement information

Next learning action


AI-generated insights must be presented as system-generated analysis and must not be represented as certain diagnoses when evidence is insufficient.


---

9.7 Personalized Practice

Purpose

Provide targeted practice based on identified learning needs.

The screen may contain:

Target concept

Practice questions

Difficulty

Progress

Completion status



---

9.8 Reassessment

Purpose

Measure whether understanding has improved after practice.

The reassessment interface should remain consistent with the assessment experience.


---

9.9 Progress

Possible Content

Previous scores

Current score

Improvement

Concept progress

Assessment timeline


The design should emphasize growth rather than only ranking.


---

9.10 Recognition

Possible categories:

Overall Performance

Most Improved

Consistency

Concept Mastery

Challenge Achievement

Subject Progress



---

9.11 Rewards

Students can view:

Available points

Reward name

Required points

Availability

Redemption status


Possible states:

Available

Out of stock

Pending

Approved

Rejected

Error



---

10. Teacher Design

Teacher Dashboard

Possible sections:

Total students

Recent assessments

Average class performance

Difficult concepts

Students requiring support

Students showing improvement

Class learning map

Intervention suggestions


Class Learning Map

Example:

Fractions              82% mastery
Algebra                71% mastery
Linear Equations       54% mastery
Geometry               76% mastery
Data Handling          63% mastery

The visualization should make difficult concepts immediately visible.

Student Profile

Teachers should be able to inspect:

Assessment history

Learning gaps

Concept performance

Improvement

Practice activity

Recognition data



---

11. Administrator Design

Administrator screens should focus on school-level management:

User management

Class management

Subject management

Reward management

Reward inventory

Redemption management

Overall learning trends

Platform policies



---

12. Navigation

Navigation principles:

1. Keep primary navigation consistent.


2. Make the current location obvious.


3. Use clear labels.


4. Keep primary actions prominent.


5. Avoid unnecessary navigation.


6. Provide predictable Back / Continue behavior.


7. Avoid dead-end screens.


8. Prevent accidental loss of assessment progress.



Role-based navigation should show users only relevant areas.


---

13. Visual Design Direction

LearnIQ should feel:

Clean

Modern

Educational

Student-friendly

Professional

Trustworthy

Data-oriented


The design should prioritize clarity over excessive decoration.

Visual Message

Learning → Understanding → Progress → Improvement


---

14. Design System

Color Palette

Token	Value

Primary	#TODO
Secondary	#TODO
Background	#TODO
Surface	#TODO
Text	#TODO
Muted Text	#TODO
Success	#TODO
Warning	#TODO
Error	#TODO
Information	#TODO


Replace all #TODO values with the final approved design tokens.

Typography

Element	Font / Size / Weight

H1	TODO
H2	TODO
H3	TODO
Body	TODO
Caption	TODO
Button	TODO


Components

Reusable components include:

Buttons

Inputs

Select controls

Cards

Navigation

Tabs

Progress indicators

Question options

Tables

Charts

Badges

Alerts

Modals

Loading indicators

Empty states

Error states

Success messages



---

15. Responsive Design

Desktop

Use available screen space efficiently.

Maintain clear information hierarchy.

Use multiple columns where appropriate.

Keep dashboards readable.


Mobile

Avoid horizontal scrolling.

Prioritize essential information.

Use touch-friendly controls.

Maintain readable typography.

Keep primary actions visible.

Collapse secondary information when appropriate.



---

16. UI States

Important interactive screens should account for:

Loading

Communicate that information is being loaded or processed.

Empty

Explain why no information is currently available and provide a useful next action when appropriate.

Error

Explain the issue in simple language and provide a recovery action.

Success

Confirm important completed actions such as:

Account creation

Assessment submission

Practice completion

Reassessment completion

Reward request


Disabled

Controls should appear visibly disabled when an action cannot yet be performed.


---

17. AI Design Principles

AI may support:

1. Assessment response analysis


2. Learning-gap identification


3. Possible misconception detection


4. Personalized practice


5. Difficulty adjustment


6. Learning-path recommendations


7. Teacher intervention suggestions


8. Natural-language explanations


9. Question generation


10. Progress summarization



AI output must:

Be understandable.

Be based on available evidence.

Avoid presenting uncertain inferences as facts.

Distinguish recommendations from confirmed assessment data.

Never imply unimplemented functionality exists.



---

18. Data Visualization

Use visualizations only when they help answer meaningful questions.

Examples:

Progress charts

Concept mastery indicators

Assessment history

Class learning maps

Improvement trends


Each visualization should help answer questions such as:

What concept is difficult?

Has the student improved?

Which students need support?

Which topic needs intervention?



---

19. Gamification and Recognition

The PDR includes:

Points / XP

Badges

Challenges

Rankings

Recognition

Rewards


Gamification should encourage learning rather than competition alone.

Recognition should include multiple dimensions:

Performance
    +
Improvement
    +
Consistency
    +
Mastery


---

20. Reward System

The reward system is school-controlled.

Student Flow

Earn Points
    ↓
Browse Approved Rewards
    ↓
Check Required Points
    ↓
Request Redemption
    ↓
View Status

Admin Flow

Create / Approve Reward
    ↓
Manage Inventory
    ↓
Receive Redemption Request
    ↓
Approve / Reject
    ↓
Track Fulfilment


---

21. Accessibility

The interface should provide:

Adequate color contrast.

Clear form labels.

Readable typography.

Visible interactive states.

Logical hierarchy.

Keyboard accessibility where applicable.

Touch-friendly mobile controls.

Non-color-only status communication.

Recoverable error messages.



---

22. Technology Context:
Layer	Technology

Frontend:html,css,js
Backend	:node.js,express.js
Database:supabase
Authentication:supabaase
Design Tool	Google Stitch / ACTUAL TOOL

---

23. Design-to-Implementation Consistency

The project documentation should follow:

PDR.md
   ↓
DESIGN.md
   ↓
MOCKUPS.md
   ↓
Implemented UI

All four should describe the same approved product.

If a feature is removed from the MVP, it should also be removed from the relevant design and mockups.


---

24. Mockups

The complete visual evidence is maintained in MOCKUPS.md.

The mockup set should cover the agreed user journey rather than only a single dashboard.

Required mockup categories:

Authentication

Onboarding

Student dashboard

Assessment

Results

Learning gaps

Practice

Reassessment

Progress

Teacher workflows where applicable

Administrator workflows where applicable

Relevant UI states


Design Source

[PASTE GOOGLE STITCH / DESIGN TOOL LINK HERE]


---

25. Design Review Checklist

[ ] MVP scope finalized.

[ ] Career-development scope resolved.

[ ] Complete screen list approved.

[ ] Student journey documented.

[ ] Teacher journey documented if applicable.

[ ] Administrator journey documented if applicable.

[ ] Navigation reviewed.

[ ] Primary actions are clear.

[ ] Desktop layouts reviewed.

[ ] Mobile layouts reviewed.

[ ] Loading states reviewed.

[ ] Empty states reviewed.

[ ] Error states reviewed.

[ ] Success states reviewed.

[ ] No unimplemented feature is presented as functional.

[ ] AI claims are evidence-based.

[ ] Mockups match DESIGN.md.

[ ] MOCKUPS.md contains final mockups.

[ ] Design-source link added.

[ ] Technology stack matches the actual implementation.

[ ] File is saved as DESIGN.md.



---

26. Related Documentation

PDR.md

MOCKUPS.md




---

27. Design Status

Field	Value

Status	In Review
Version	1.0
Last Updated	YYYY-MM-DD
Design Source	[LINK]
Mockups	MOCKUPS.md



---

Core Design Principle

> Don't just show students their marks. Show them what they need to learn, help them improve, and make that improvement visible.



LearnIQ

Assess → Understand → Improve → Measure → Recognize → Reward → Learn Again
