---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: "Overview"
layout: single
classes: wide
---

## Class Description

Welcome to CSE 113: Parallel and Concurrent Programming! In this class, we will explore many aspects of parallel computing, from instruction-level parallelism in seemingly sequential programs to thread-level parallel programs that can efficiently execute across the many cores of today's multiprocessors and accelerators (e.g., GPUs). We will learn how to write programs that execute efficiently and correctly in concurrent environments. This class will give you the necessary foundation to solve problems using concurrency: a powerful skillset given that today's computers are becoming more and more parallel.

## Teaching Staff

We have a great teaching staff this quarter! All of them are passionate about parallel programming. Please get to know them and take advantage of the office hours and mentoring sessions they provide

* *Grad TAs*: 
  * Jessica Dagostini
  * Gurpreet Dhillon


* *Undergrad Graders/Tutors*
  * Jacob Dickerman
  * Ryan Nelson

## Necessary Background

The prerequisites for this class are CSE 12 (systems), CSE 101 (data-structures and algorithms), and recommended CSE 120 (architecture). You will need some foundation in all of those topics to succeed in this class. For example: you will need to know data-structures and algorithms, as we will extend some of these sequential concepts to their natural parallel counterparts. You will need some systems background, as we will discussing many aspects of the hardware/software interface. Parallel programming is most efficiently executed on parallel hardware: Thus, it is helpful to understand shared  hardware resources (e.g. the memory hierarchy) of the underlying architectures. 

Because this is an upper division class, I do expect a general CS foundation. For the homeworks, I will assume that you are:

- comfortable using a linux command-line
- programming in a high-level language (e.g. Python)
- programming in a low-level language (e.g. C)
- a high-level understanding of computer architecture
- a basic ability to use Github
- a basic ability to use Docker

## Class Modules

This class will be split into 5 modules, each of which are roughly two weeks:

* **Module 1: Introduction, Background and ILP** This module will introduce the class and provide a programming, compiler, and architectural refresher. We will discuss how modern hardware exploits parallelism within a sequential thread (ILP) and how to write parallel code in C++.

* **Module 2: Mutual Exclusion** This module will discuss the fundamental problem of mutual exclusion. We will discuss the theory behind mutual exclusion, how it is implemented in practice, and specialized mutual exclusion implementations. 

* **Module 3: Concurrent Data Structures** This module will discuss concurrent objects and how to reason about them. We will discuss several implementations and show how they can be used in load balancing and software pipelining.

* **Module 4: Parallel Programming on GPGPUs** This module will discuss general purpose (GP) GPU programming. We will discuss the SIMT programming model, hierarchical execution, and different architectural considerations when optimizing programs.

* **Module 5: Advanced topics** This module will discuss advanced topics, including memory consistency and fairness. 
 
## Class Format

Each class is 95 minutes. I will plan to be available 10 minutes before class starts and 10 minutes afterwards. 

_Non-protected materials_ will be hosted on this website. This includes the schedule, lecture slides, and references, etc.

_Protected materials_ will be hosted on a Canvas website that you will need your university credentials to access. These materials include homeworks, zoom links, lecture recordings, tests, grades, etc.

_A Class forum_ will be provided in Piazza. If you organize other forums outside of the class Piazza (e.g. discord), you must adhere to academic integrity and be kind and respectful. 

## Quiz/Attendance

Live discussions and synchronous class attendance are a valuable part of the learning experience. I expect you to make an effort to synchronously attend this class, whether on Zoom on in-person.

I plan to upload recordings of the class to canvas, but this is not a substitute for attendance. This will be graded using a small quiz given at the end of the class. Please do not submit the quiz unless you either attended or watched the lecture. 

You can have up to 3 absences that will not affect your grade. 

_If synchronous attendance drops significantly then I will stop recording lectures and make attendance a part of the grade_

## Accessibility

UC Santa Cruz is committed to creating an academic environment that supports its diverse student body. If you are a student with a disability who requires accommodations to achieve equal access in this course, please submit your Accommodation Authorization Letter from the Disability Resource Center (DRC) to me by email, preferably within the first two weeks of the quarter. I would also like us to discuss ways we can ensure your full participation in the course. I encourage all students who may benefit from learning more about DRC services to contact DRC by phone at 831-459-2089 or by email at drc@ucsc.edu.

## Office Hours:

### Instructor Office Hours:

I will provide 2 office hours per week: Thursdays from 3 - 5 PM. 

My office hours can be remote or in-person. My physical office is E2-233. I will provide a Zoom link on canvas. I manage the office hours through a Google doc sign-up sheet. I will reset the list sometime on Thursday and notify with a canvas announcement. Any name on the list before then will be erased.

Please sign up for only 1 slot at a time. If there is no other student waiting at the end of your slot, you are welcome to stay. If you want to discuss an issue that you think others might also be interested in, please add the issue to the spreadsheet. If you see your issue listed, please add your name and we add more people to the discussion. 

The sign-up sheet is meant to provide fairness; as such I will be strict about keeping to the schedule. Please forgive any abruptness.

### TA and Tutor Office Hours:

#### Jessica Dagostini
To reserve a spot - https://calendly.com/jessicadagostini/office-hours-cse113-24

- **Wednesdays** - 1 pm to 2 pm - In-person at room BE-151
- **Thursdays** - 10 am to 11 am - Remote via Zoom

#### Gurpreet Dhillon
To reserve a spot - https://docs.google.com/spreadsheets/d/1D_Z7ABTYHt5sTkUaRpSM7-748l-P8LA-hbYdGugKk-I/edit?usp=sharing

- **Mondays** - 12 pm to 1 pm - Remote or in-person at BE 312 C/D
- **Fridays** - 1 pm to 3 pm - Remote or in-person at BE 151

#### Jacob Dickerman
To reserve a spot - https://docs.google.com/spreadsheets/d/1SNNFZ92bLRSw7IDEsAi6OVoyPvUdGzugjLLgtpDq5HQ/edit?usp=sharing

- **Thursdays** - 1:30 pm to 3 pm - Remote or in-person (locations updated in sheet)
- **Fridays** - 11:30 am to 1 pm - Remote via Zoom

#### Ryan Nelson
To reserve a spot - https://docs.google.com/spreadsheets/d/1sT2Ho_4ed6I6_ikUm0jvZJabPzqk1o8CRM9PGedhQ5Y/edit?usp=sharing

- **Wednesdays** - 10:30 am to 12:00 pm - Remote via Zoom
- **Thursdays** - 10:00 to 11:30 am - in-person (locations updated in sheet)

## Asynchronous Communication

For any questions outside of office hours: Please post to the class Piazza. If it is a sensitive topic, you can post only to the teaching staff. Please do not message me directly unless it is an emergency. I may not respond. 

Link for Piazza is https://piazza.com/ucsc/winter2024/cse113

If your question is more general, make it visible to the rest of class. If it isn't clear if it is a sensitive question or not, please start out by making the question to the teaching staff and we can advise on making it public or not. Feel free to answer questions that your classmates post or freely participate in discussions there.

Please do not email us individually. Those emails get buried, or they might not be seen by the right member of the teaching staff. This especially applies to grading questions; if you have questions about your grade do *not* email a grader directly. Write a private post on Piazza to the teaching staff. Typically grades are a collaborative effort between several TAs, and it helps if we can all see the issue.

We will strive to reply to homework questions and discussions within 24 hours. Do not plan on, or expect help, outside of regular business hours (after 5 pm, weekends, or holidays)

## Homework:

There will be one assignment per module, for a total of 5 homeworks.

We will use github classroom with automatic feedback for 4 of the assignments. Because this is a relatively new setup, there may be some friction getting started. We appreciate your patience and understanding. I will update the class as we make progress.

We will provide a docker for you to develop in. We plan to enable a git-based workflow where you push your current solution to a repo and receive feedback from a server. You will be graded on the server feedback rather than the results from your own machine. This is to help provide fair (and scalable) grading across the increasing diversity of devices that everyone has these days. Someone with an Apple M-series processor will get very different results than someone with an Intel X86 processor.

_Architectural differences are very interesting to discuss and I hope we can have detailed discussions about how your machine's results differ from the server on Piazza_

Homeworks are due at midnight on their due date, but do not plan on help after 5 pm. You will have 10 days for each assignment. You have an additional 3 days to turn homework in late without penalty. After that, late work will not be accepted. The due date for the last homework may need to be adjusted to account for the end of the quarter.

## Tests:

There will be tests in this course: a midterm and a final. The midterm will be worth as much as a single homework assignment (10%). The final will be worth 30%.

The midterm will be given halfway through the class: assigned on Monday, Feb. 12 during class time.
The final will be given on Monday, March. 18.

You will be allowed 3 pages (front and back) of notes in any format (printed, hand-written, colored, etc). Feel free to print slides to use as your notes.

## Grade Breakdown

- Attendance/Quiz: 10%
- Homeworks: 50% (10% each)
- Midterm: 10%
- Final Exam: 30%

If you want to discuss a grade, please contact the teaching staff no later than 1 week after the grades are posted.

## Academic Integrity

One of the joys of university life is socializing and working with your classmates. I want you to make friends with each other and discuss the material. 

**That said, I expect all assignments (code, write-ups, and tests) to be your own original work.**

If you work together with a classmate on an assignment, please mention this, e.g. in the comments of your code. If you use a figure you didn't create in a write-up, then it needs a citation. Please review the [universities policy on plagiarism](https://guides.library.ucsc.edu/citesources/plagiarism)

This class has a zero-tolerance policy on cheating. Please don't do it. I would much rather get a hundred emails asking for help than have to refer anyone for academic misconduct.

As a final note on cheating: the economic condition facing computer science graduates is volatile in the near future. It is crucial that you spend your time at University learning the material deeply. If you cheat, you will not be able to stand out from your colleagues who put in the effort when it comes time to find a job. Cheating will have a devastating and unforgiving impact on your immediate career opportunities. Don't do it.  

## Privacy

I plan to record lectures in class. Please be aware that:

- Things you do or say will be recorded. I doubt that this will be an issue, but if you want me to remove any part of the recording, please just let me know.
- Many forums (e.g. zoom chats, Piazza posts, etc.) chats are not private. Please be respectful and kind and assume everyone can see what you are typing.

## Using AI Tools

We are in an exciting time for AI, especially for tools like Github co-pilot and LLMs (e.g., ChatGPT). These tools have incredible potential and they are improving every day. 

However, the educational community has not had sufficient time to understand the impact they will have on learning objectives. This class has been designed to be taken *without* the use of AI tools. For this class, they are not allowed to be used. If we suspect abuse, then we may implement random audits of assignments, where you will be asked to explain your implementation in detail. 

If you are interested in seeing how these tools can help with parallel programming, please feel free to use them *after* you have submitted a non-AI version of the homework. We would be very interested in hearing about your experience, e.g., as a piazza post.

## Acknowledgements

This page is based off of Professor [Lindsey Kuper](https://users.soe.ucsc.edu/~lkuper/)'s CSE232, Fall 2020 website
