> **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group \#: 14   |                             |
| -------------- | --------------------------- |
| Student Names: | Robert Brown (10180520)     |
|                | Brooke Kindleman (30090660) |
|                | Risat Haque (30094174)      |
|                | Amnah Hussain (30095907)    |

**Table of Contents**

[1 Introduction 1](#_Toc439194677)

[2 High-level description of the exploratory testing plan 1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing 1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports 1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided 1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned 1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself 1](#_Toc439194683)

# Introduction

The following lab report provides exposure to exploratory, manual, and regression testing for a simple ATM machine simulator, provided in two unique versions. Version 1.0, the original program, is tested with exploratory and manual testing while Version 1.1, the mock refactoring of Version 1.0, is tested with regression testing to verify the success of previous testing methods locating and correcting faults. During the evaluation of both versions, it was discovered that the program had a multitude of errors, all of which will be documented in both the sections below and the provided excel sheet.

Prior to starting this lab, our knowledge of exploratory and manual functional testing was limited. We discussed that manual scripted testing is a “step-by-step outline of various tests to be performed by a secondary individual,” with a strict outline that has been created prior to the testing period taking place, while exploratory testing was a “free-for-all” testing, where individuals attempt to break the system without a clear outline of the program. Exploratory testing relies on the assumption that the tester will be curious and inquire enough into the functionality of the program that most existing faults are located. Manual scripted testing, by comparison, is founded on a rigid testing structure outlined previously to any testing actually taking place. Unlike exploratory testing, in manual scripted testing, the program’s requirements are clear and predefined; there is a heavy reliance on prior knowledge of the programs by those who wrote the tests and a trust that the tester will follow the script as closely as possible when testing.

# High-level description of the exploratory testing plan

Prior to conducting exploratory testing on Version 1.0 of the program, our group briefly familiarized ourselves with the requirements of the ATM system and which outputs indicated each functionality was, or was not, free of fault. Each team member independently tested the system for approximately 30 minutes and recorded relevant descriptions of each test. These descriptions included what the error was with the type of card used, as well as the conditions the error occurred under. After this, the team collaborated and compiled a main list of errors to be recorded in the project’s backlog, ensuring that if the same error was discovered by multiple team members it would not be recorded multiple times. The backlog consisted of bugs with the following: the function being tested, the state of the system, the steps to reproduce, the expected outcome, the actual outcome and a relevant screenshot of the current state of the program. Additional information, such as log readings or receipt print-outs, were entered in the main text area in code block formatting if an image of the system state was already attached to the report.

# Comparison of exploratory and manual functional testing

From both testing methods, our group discovered bugs in features that are essential to the proper functioning of the ATM system. The majority of the bugs our team discovered and reported were found during exploratory testing, in which 16 bugs were found. Manual Functional Testing (MFT), by comparison, revealed 11 bugs in the ATM system. Of the 11 errors discovered during MFT, 5 had already been found and documented in the Exploratory Stage. In total, 22 errors were located through the combination of exploratory and MFT. Through the team’s testing, MFT proved to have an efficiency of 27.5%, with 11 tests resulting in the location of an error, out of the total of 40 tests that were conducted. Of the 11 errors found during MFT, 6 of them were unique to MFT alone.

A quantitative comparison to the efficiency of the exploratory testing cannot be made, as a script with a numerical count of the tests performed and a record of how many tests resulted in an error being found. It should, however, be emphasized that the majority of unique errors located by our team in this lab were done so during exploratory testing, not MTF. A more general comparison of the two testing methods, comparing the approximate times spent doing each method and the rate at which they discovered errors, supports this. Our group spent around 45 minutes on MFT, in contrast to Exploratory testing, which was done for approximately 30 minutes. With this knowledge, it can be understood that MFT took approximately 50% more time than Exploratory testing, but only discovered 11 errors in this time, compared to Exploratory testing’s 16 found faults. These rough values allow for the calculation that errors were found in MFT with an approximate rate of 0.24 errors per minute. Exploratory testing had an error discovery rate of 0.53 errors per minute, a rate that is roughly 54% greater than that of MFT. This relationship suggests that Exploratory testing is more effective, efficient and takes less amount of time to complete when compared to MFT.

It must be noted, however, that although MFT proved to have a lower efficiency at locating errors than Exploratory testing, it was more consistent and easier to use as a reference for regression testing. Having a pre-written script to follow when testing, with requirements and expectations from each test, clearly outlined allowed for each requirement clearly be classified as either “failed” or “passed,” as well as providing a simple template to follow and compare to when our team began regression testing on Version 1.1 of the ATM program. Errors discovered during regression testing could easily be compared to the testing results from the MFT of Version 1.0 of the ATM program, and it could be quickly concluded as to whether a fault had previously existed in the system and had not been resolved in the new version, or if it was a new error entirely that required attention and documentation.

An unexpected discovery by our team during the lab was that 6 of the tests in MFT were not true “bugs,” as the script provided for MFT expected us to find, but were other issues that were not directly related to the test result and would not result in a failure of MFT testing, despite them causing issues with the functionality of the ATM program. Test 12, for example, successfully shows accounts, thus passing the corresponding MFT test, but does not consider that users may not have a savings or checking account. Although regression testing implements a way to correct this, MFT fails to catch cases that are outside the requirements of the system but can contribute poorly to the user experience. This rigidity in the testing process for MFT does not allow for the flexible recording of errors not otherwise in the provided script, thus allowing some errors to be ignored that would otherwise contribute to a less-than-optimal or non-functioning program, simply because there is not a reasonable way to record them in the premade testing infrastructure.

MFT can also fail to locate major issues with the system that Exploratory Testing can catch. For example, our team discovered an infinite money withdrawal bug where users can repeatedly access $20 bills from the account selection tool. This was discovered during Exploratory testing when a team member was picking one of the options in the transaction menu, and accidentally selected the incorrect option. The error was recorded as bug ATM_1-10 on the backlog. An event like this would not occur during scripted testing, due to the necessity of precisely following step-by-step instructions, provided before testing begins.

Exploratory testing, while having an improved ability to adapt to unexpected conditions and errors, still maintains the possibility of missing some errors during testing. This can be attributed to the unexpected actions of human testers during evaluation, who may not consider attempting a certain function or boundary, resulting in less-than-perfect error location and reporting. A bug that was discovered at the MFT stage was transferring amounts between checking and savings accounts on Card 2. This was recorded as ATM_1-17 on the backlog. From exploratory testing, we didn’t test this specific condition, but MFT allowed our group to check specific conditions using different variables (ie: card 2 instead of card 1). In conclusion, our group does believe that both stages are essential in testing and can contribute to the overall quality of the application. Exploratory testing is more effective, but without MFT, several bugs can still be missed.

# Notes and discussion of the peer reviews of defect reports

Prior to writing any defect reports our group discussed a standard for reporting and created a report template to standardize the format of information provided in the report. When completing regression testing, the more detailed reproduction steps and screenshots were helpful in identifying if defects were properly resolved.

# How the pair testing was managed and team work/effort was divided

Our team utilized an online group generator to divide the group into 2, thus 2 pairs. Team A was composed of Risat and Robert, and Team B was composed of Brooke and Amnah. Using this structure, each team worked independently to test a set of 20 of the total 40 tests during the manual scripted testing. Team A was responsible for Tests 1-20, and Team B was responsible for Test 21-40. Each pair ran the tests twice to verify that tests were done correctly and errors were not ignored. Tests were conducted synchronously in each pair with active discussion and bug reporting happening simultaneously. This was achieved by a Zoom call between each pair, in which each team member screen shared and narrated their actions while their partner watched and ensured the correct conditions and inputs were being used to evaluate program functionality. This format ensured that work was balanced evenly among teammates, with each individual contributing an equal amount for the testing. In addition to this method, each error that was located was checked twice by the team member who found it, followed by a collaborative discussion with the other 3 team members to allow any issues regarding it to be brought forward and resolved collectively.

# Difficulties encountered, challenges overcome, and lessons learned

Some of the difficulties we encountered were completing the testing remotely with partners while screen sharing. Since the program window couldn’t be resized it was difficult for the other group members to view the exact behaviour of the program due to the reduced visibility of the program’s interface. Additionally, we noticed some slight differences in the way that the system GUI elements were rendered based on the operating system (i.e. Mac OS vs Windows), which may contribute to additional bugs being reported or certain bugs being missed, depending on how flexible the program was at properly adapting different operating systems.

The scripted testing felt very repetitive and it was mildly frustrating having to repeat certain tasks multiple times for some consecutive tasks to evaluate each step of a specific function. For a longer-term project, our group felt it would be more time-efficient to implement automated testing to complete the scripted portion of the testing.

Through this experience, our group worked on improving our collaboration and communication skills that will inevitably help us in future labs, especially given current conditions requiring work to be completed remotely. Additionally, we also gained exposure to testing technologies, bug writing, excel tools, github/git, and ATM functionalities through group discussions.

# Comments/feedback on the lab and lab document itself

After reading through the document our group was able to understand the basic operation of the ATM system. Additional functionality such as the holding of balances wasn’t clearly identified until our group referred to the ATM system documentation website. This was available within the source listed at the bottom of the document. Without this, we would have caught additional bugs that were in fact not bugs, but simply a lack of understanding on our team’s behalf of how the program functioned.
