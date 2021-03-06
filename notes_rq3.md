# About the first 35 papers

## Programming Languages

For the 35 papers, we have:

Algol 68
C
C
C
C, C++, and Java
C/C++
C++
Two studies: (i) Java, Python, CUDA; and (ii) Java
Cobol
Does not specify.
Fortran
Fortran
J#
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java
Java, C
Java. The pilot was in Python, but it was just a pilot.
Pascal
Pascal
Pascal
Pascal
Pascal and C
PL/I

Not one language per paper. One of them used three, for example. One paper had to studies, both focusing on Java. Another one had a single study involving three languages. This is the reason why the numbers below do not add up tot 35. Out of the 35 papers, we have:

- 18 focused on Java, one in J#. 
- 7 on C
- 1 on Cobol
- 1 on Algol 68
- 1 on PL/i
- 3 on C++
- 1 on Python (the pilot for another one also used Python)
- 2 on Fortran
- 1 on CUDA
- 5 on Pascal 

Lots of work on Java and C/C++. Not a single one targeting languages in the iOS ecosystem, even though the Apple store had a revenue of 26.5 billion in 2017 [1] and Swift and Objective-C are popular programming languages [2], not a single one focusing on JavaScript (or TypeScript), arguably one of the most popular programming languages [2], just one targeting Python, one of the most popular languages to teach programming [3]. More generally, the readability of the constructs of a number of programming languages that are popular has not been studied. This suggests that guides indicating better implementation approaches and preferred idioms are defined based on gut feeling and personal experience more than on empirical evidence.  

- [1] https://www.forbes.com/sites/chuckjones/2018/01/06/apples-app-store-generated-over-11-billion-in-revenue-for-the-company-last-year/#31ff67e06613
- [2] https://redmonk.com/sogrady/2019/07/18/language-rankings-6-19/
- [3] https://cacm.acm.org/blogs/blog-cacm/176450-python-is-now-the-most-popular-introductory-teaching-language-at-top-u-s-universities/fulltext

All of this is relevant because results do not transfer from one language to the other. As previous work has shown in the context of program construction (see the papers below and work by Leif Singer and colleagues), the choice of programming language does affect programmer performance even for basic programming tasks. 


Should we separate these results per study, instead of per paper, considering that some papers have more than one study?


This compares Python and C++ for novices:
I am assume the typical exercises focus on construction. Need to check this.  
https://dl.acm.org/doi/10.1145/3159450.3160586

This one Python vs. C: 
Entire course. Exercises usually focus on construction
https://www.semanticscholar.org/paper/A-Controlled-Experiment-on-Python-vs-C-for-an-Wainer-Xavier/ba21f056208d67a6bfe039cb5cd0ae51a34546d2



## Measures of readability (dependent variables) for experiments:

There is a considerable repertoire of approaches to assess program readability. They represent the dependent variables of the kind of comparative study we are studying. Unveiling these readability measures can help in the design of new comparative empirical studies analyzing program readability. It is useful to briefly describe the task that was performed. 

Personal opinion: which one is "better", which one is more difficult to understand? Comparing different approaches. Personal opinions may be rated/graded or ranked. Subjects may also be asked simply whether they understand or not (in this case, the opinion is about their understanding, not directly about the code or whatever is being compared). 

Findbugs warnings: rate per class, rate per line of code, accounting for categories of warnings or not. Absolute number does not make much sense unless the comparison involves different versions of the same program/system that have similar numbers of LoC and do the same thing.

Experiments vs. quasi-experiments. The atoms of confusion study fits into the latter. 

Quite a few studies analyze time and also correctness. Few measure the **rate of correct answers per time unit**. This makes sense because less time might stem from code being easier to read but also due to the subject simply paying less attention. 

Correct answers vs. incorrect answers. Correctness can also be measured in terms of the error based on the expected value of an aggregate measure. 


- **Number of lines of code that were recalled correctly and in the correct order**. The subjects had 4 minutes to recall programs they had just spent 3 minutes studying.  Compare simple vs. complex control flow and the use (or not) of paragrahing in the source code. 

- **Fully correct answers to a test**. The questions were placed in five categories based on difficulty (where the easiest category had the most fully correct answers). The questions either involved explaining the purpose of a code snippet or tracing the execution of a program, i.e., how its state change as each instruction was executed. Compares metrics: Number of statements, Number of operands (including all identifiers that are not key words), Cyclomatic complexity, Average nested block depth, Average number of parameters, Number of methods (for EiPE questions only). Two *dynamic metrics*: Sum of all operands in the executed statements, Number of executed program statements. **Very interesting**. We read code in an attempt to understand what it will do at runtime, but most work on metrics focuses on **static metrics**, not dynamic ones. 

- **Time to answer the questions, correctness of the answers, visual effort**, measured "indirectly using observable variables related to fixations", such as pupil dilations, time spent looking at specific sections of code, and examined area of the code. This study compared regular vs. non-regular code snippets.  

- **Task completion time, correctness of the answers**. The participants had to study 2 out of four small J# programs and later were presented with 3-option sheets where they had to pick the one that best described (they were not really questions) the function of the application. Each sheet was only presented after the previous one was complete. Naming style again.

- **Findbugs warnings**. In this case study, 8 open-source Java systems were analyzed to check conformance of their identifiers against 10 identifier style guidelines (collected by the authors). Implicit assumption: identifier naming impacts readability. # of classes with flawed/not flawed identifier names vs. # of classes with Findbugs warnings.

The following two pertain to the same study:

- **Correctness of answers**. Experiment 1, Java. The subjects were asked to fix a bug in versions of a Java program using different styles of identifier (although always single-letter vs. more complex). Experiment 2, C. The subjects had to explain the function of a program and then extend its functionality. Are single-letter variable names really harmful for program comprehension?
- **Personal opinion**. Which version of the same code snippet is better?  

- **Personal opinion**. The subjects had to rate on a 1-3 scale their preferred style of code organization for Pascal programs. 

- **Correctness of answers**. Different types of true/false questions pertaining to "operations", "control flow", "state", "function". Nonsensical vs. meaningful identifier names. Also places subjects into three groups based on their experience. 

- **Correctness of answers, personal opinion about difficulty, eye tracking, time to complete the task**. Correctness: exact, partial, wrong. Personal opinion about difficulty in terms of rate and rank. Eye tracking: fixations (duration and rate) and saccades (amplitude). Measured four different levels of indentation (0,2,4,8).

- **Findbugs warnings**. Number of warnings per KLoC. Also examined the 8 different types of warnings (for RQ2). Case study targeting 14 open source projects. Measured WCMR, a measure of the quality of variable names aiming to account for concreteness and retention. 

- **Personal opinion**. Subjects had to chose the version of a code snippet they considered more readable. Each one had to do that for 10 pairs of code snippets where, for each pair, one snippet adhered to a certain stylistic guideline and the other one did not, some related to readability, some to legibility. 

- **Correctness of answers, time to complete the task**. Correctness classified in terms of Correct, Partially Correct, Incorrect. Compares 5 different orderings for the elements of a class (original, random, and three more discussed in the paper). Also considered subject experience as an independent variable. Subjects had to answer three multiple choice comprehension question pertaining to 5 classes, where each one employed a different method ordering scheme.

- **Correctness of answers, time to complete the task, personal opinion**. Compared styles of nested if statements. Subjects were randomly assigned into three treatment groups of 12 students; each group receiving one version of the nested IF statements. 5 short questions to answer about the code and 2 subjective ones. Personal opinion on a 5-point scale. There was also a second experiment with three styles of if nesting, one of them also appearing in the first experiment. 

- **Correctness of answers, time to complete the task, correct answer/minute rate, personal opinion**. Score in a 14  multi-choice question test (Pascal). 1-5 scale, worst to best. These questions asked about the programs the subjects had to study. Another study with 10 questions (C). Compares programs that use and do not use the "micro-typographic" elements of Book Format style: "identification and/or creation of code segments, code paragraphs, sentence structures, and intramodule comments. To do this, micro-typographic factors such as blank lines, embedded spaces, type styles, and in-line comments are used"

- **Correctness of answers, personal opinion, time to determine whether they understood or not**. Each subject studied 8 methods extracted from a group of 50 . They had to study the methods. For each method, participants were asked to first answer whether they understood the method or not (personal opinion). If they stated that they did understand, they were then asked three verification questions about the method (correctness). Measures a number of different metrics to assess whether any of them is a good predictor for "code understandability". Time was measured only until the subject clicked that shee understood the code or not. Also assigned a binary judgement to subject understanding (if 2 of the 3 verification questions were answered correctly) and compared that with whether they believe they understand the code or not .  

- **One-line summary of the program, percentage of recalled lines, percentage of recalled lines following one presented by the experiments and order of the lines**. Experiments aiming to verify the existence of beacons. Participants studied printed copies of a short program. Asked to understand it and memorize it. Then asked to summarize and recall. Second experiment: copy of a program, subjects were given 7 cards with one line of code each. Asked to write the following two lines. 

- **Time to complete the task, visual focus**. How long developers inspected the code to find a defect. Time spent looking at different parts of the code and the direction of reading of the subjects. Participants were asked to find a defect in a code snippet, which was repeated four times. Two snippets had semantic defects and two had syntactic defects. In our study we compared short, mostly single-word identifier names (“short” condition) with longer compound identifier names. Used the type of defect as a control. 
 
- **Brain activity**. In terms of average magnitude in alpha and theta frequency bands. Compared how the brain is activated when reading code with and without potentially confusing constructs and coding idioms (atoms of confusion). 

- **Findbugs warnings**. Only used method-level warnings (not LoC-level). Compared the readability scores of all methods from 20 systems, using the warnings as ground truth. These models were used as predictors and AUC was the evaluation metric, together with the number of correctly or incorrectly classified methods.  

- **Time to complete the task, correctness of answers**. Correctness in terms of both number of errors (because the program outputs multiple values) and magnitude of the error (considering that one of the outputs is an aggregate measure). Participants had to trace the execution of the program based on two different inputs. Compares positive vs. negative conditions; (ii) true/false conditions; (iii) loop styles, more specifically, process/read vs. read/process, and (iv) memory effect (whether the performance is better in the second trial).


- **Personal opinion**. Developers were asked to judge multiple methods considering two different versions, one with developer-inserted blank lines and another one with the blank lines inserted by a tool. Evaluates the impact of developer-inserted vs. tool-inserted vertical spacing (blank lines) on readability. 

- **Correctness of answers**. Students had to read one version of the program and answer 12 short-answer questions about said program. The grade in this test was the score. Compares procedure format (none, internal, external). Also looked at comments, but accounted for all treatments separately. 

- **Correctness of answers, time to complete the task**. Number of correct answers to two sets of questions and time to answer them. Compares presence vs. absence of side effects. Each subject was subjected to the two treatments and had to answer questions pertaning to each one. The questions exhibit small snippets that may or may not have side effects. 

- **Findbugs warnings**. Priority 1 and 2 warnings. Analyzed 8 open source Java projects. Tries to define a readability index based on a number of guidelines for identifier naming and on existing metrics such as McCabe's cyclomatic complexity.  

- **Personal opinion and correctness of answers**. 



Readability (based on opinions of the subjects about how readable code is), when comparing expert and novice implementations, and code comprehension (objectively measured), more specifically, whether there is a difference in comprehension when novices examine expert- vs novice-style code examples. More abstractly, the authors want to gauge whether novices who prefer a "novice style" of writing code have deep misunderstandings about the programming language. 
The score of the participants in the 20 questions (measured on a 1-100 scale). According to the paper, "the questions were scored objectively". 
"Time
Success rate
Self-reported difficult rate
fNIRS: Oxy values
Eye Tracker: Fixation duration"
response time and correctness (correct (2), almost correct (1), or wrong (0))
"""The statistical analysis begins with an initial simple comparison of means for each variant for each of the three response variables: description ratings, confidence, and PCIS. Subsequently, mixed effects regression models are considered"". ""Second, the complete model is generated to assess the effects of four general categories of explanatory variables on the given response variable"".

About four general categories: The first category includes demographic information such as the gender, (language) comfort, and years-worked. The second category includes question characteristics, which includes code type (snippet or algorithm), lines of code, number of identifiers in the code (identifiers), and number of identifiers squared (identifiers2) – included after a graphical inspection of the data revealed a quadratic shape. The third category includes the time spent analyzing the code, writing the descriptions, and for memory, the time spent recalling identifiers. The fourth category includes answer characteristics, which, for example in the case of description rating, include the variables confidence and length of description.

About any variables:
Description rating - is the evaluation of correctness of each response (description in free-form) on a 0 (omitted an answer or reported a problem with viewing the code) to 5 (correct) scale.
Confidence - the subject are confidence that understanding the code in scale of 1 (low) to 5 (high).
PCIS (percent correct in source) - the percent of correct answers for identifiers that appeared in the code (list of identifiers).


For each variable was created models statistical (regression) types different: first a simple model and then a complete model.

Simple Model: ""is first constructed to gain an initial impression as to the influence of question, variant, and their interaction, hereafter denoted question*variant, on one of the three response variables: description rating, confidence, and PCIS"".

Complete Model:  includes the variable variant and its interactions with the other variables. Because each model contains significant interactions, variant is always discussed in conjunction with other variables."
"Variables:
TOTVAR - number of different variables in the program
LENGTH - average length of variables
WIDTH - average number of lines between the first and last use of variable.
VAR - average normalized length of variables.

Comments:
NCOM - number of comments
NC - volume of comments in characters
NBLOC - number of blocks of contiguous comments

Structural Complexity:
NSTRUCT - number of structures
DTOT - DEPTH(S) summed over all structures S.
DAVE - DTOT/NSTRUCT - average depth of nesting
DMAX - maximum depth of nesting
CYCLO - sum of program branches plus one.

Software Science Parameters:
N1 - total number of operators in a program
N2 - total number of operands in a program
NU2 - number of unique operators
NU2 - number of unique operands
N = N1+N2 - measured length of the program
NP = NU1 log2 NU1+NU2 log2 NU2 - predicted length
L = 2*NU2/NU1 * N2 - estimated implementation level
V = N log2 (NU1+NU2) - volume of the program
ERR = |(N-NP)/NP| - absolute error in predicted length
LEVEL = L² * V - level of the language used
EFFORT = V/L - mental effort required to understand the program.

Program Length:
NL - total number of lines in the program
NSL - number of lines containing statements"
"RQ2 - Grades in 5 options (totally positive, positive, neither positive or negative, negative, or totally negative)
RQ4 - Pull request response (accepted, rejeicted)"
Time required to correctly comprehend the program. The other dependent variable was the subjective opinion of each subject about whether parameter or local variables were more important to understand a method. 
Four dependent variables, 1) whether a task was completed successfully, 2) Time on task to complete programming tasks, 3) the number of compiler errors received by the developer, and 4) the percentage of time developers spend with the program not compiling.
Which areas of the brain are activated and the intensity with which activation happens. For RQ1, the measure was the contrast between the images obtained during bottom-up comprehension and detection of syntax errors (the baseline). For RQ2, they measured the "balanced contrast between the bottom-up condition and the 4 semantic-cues conditions". It is not clear to me how the non-beacon version differs from the bottom-up snippets. Maybe in the bottom-up snippets every identifier was obfuscated whereas for the non-beacon versions of the semantic cues snippets only some of the identifiers, the beacons, were obfuscated. This is suggested by Listing 2, where some of the identifiers are not obfuscated. It is important to stress that time is NOT a dependent variable. The snippets were designed to take approximately the same time to comprehend.
Perceived understandability.




## Stuff we did not see

Studies analyzing the impact of optional typing in languages such as TypeScript, Hack, Dart, and Python (with MyPy). 

Very little work focusing on functional programming constructs and their positive or negative impacts, when compared to alternatives.

Readability of concurrent code. Concurrency is hard, but there are probably ways to make concurrent code harder to understand and, conversely, easier. There is work on program construction and on performing evolution in a prexisting program, but we could not find a single study focusing on readability. 

Studies comparing writeability and readability of specific constructs, idioms, and stylistic choices. 

