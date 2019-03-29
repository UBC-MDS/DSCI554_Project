# Proposal

### Identify the question that your team in interested in answering with the survey. The aim of the survey should be to try to answer one specific and testable question. Examples of specific and testable questions include (you can use one of these if you really like them):

DSCI 512 is a programming and algorithms course in the MDS program at UBC which introduces fundamental algorithms such as sorting and searching, as well as data structures. According to a poll done during the course, some students reported that they have been experiencing a hard time with course materials and lab assignments. This leads to our survey question:

Does the level of programming experience prior to the MDS program influence a person's self-perceived difficulty of DSCI 512 (Algorithms and Data Structures)?

### Identify the other questions you plan to ask in your survey to identify confounding variables and justify/explain why you plan to include them.

#### 1.0 Confounding Variable: Sex (type: category)

**Explanation**: Sex is based on a biological classification system.  It has been included as a confounding variable because there is evidence to suggest that biological differences between males and female might affect a student's percieved difficuly of the couse.  For example, it is reported that on average, females are more prone to stress than males[1].  This is relevant to our question because, for example, difficulty may be more accutely percieved by an student who is more prone to stress.  

**Questions**: Sex?

**Options**: 1) Female, 2) Male

#### 2.0 Confounding Variable: Math Skills (type: category)


**Explanation**: Mathematics is an essential skill when it comes to learning algorithms. Algorithms are utilized everywhere to provide solutions to problems, but developing algorithms requires strong logical thinking abilities. Mathematics is the formal study of logical consequences, which is extremely important when understanding algorithms. Therefore, it is evident that students' mathematical abilities may affect their level of programming experience, as well as difficulty in learning DSCI 512.

**Questions**: Among all the math courses you have taken in the past, in general, how were your grades compared to others? For example, Calculus, Linear Algebra, Statistics.

**Options**: 1) Below average, 2) Average, 3) Above average


#### 3.0 Confounding Variable: Friends or family who have jobs associated with programming (type: category)

**Explanation**: Undoubtedly, friends are more likely to share common values and interests. Hence, if a MDS student has friends or family who work for IT companies, they are more likely to be affected and tend to have programming experience before the program. During the course, those friends can provide help so that students are less stressed when they have problems.

**Questions**: Do you have any friends or family who have jobs associated with programming?

**Options**: 1) No, 2) Yes


#### 4.0 Main Covariate: Previous programming experience (type: category)

**Explanation**: The level of the previous experience is the main independent variable that we are interested in, which is a potential reason for variation of the self-perceived difficulty in 512.

**Questions**: ???

**Options**:(scale from 1 to 5, entry to expert) ???

#### 5.0 Outcome: Self-perceived difficulty regarding DSCI 512 (type: category)

**Explanation**: Self-perceived difficulty regarding DSCI 512 is the outcome whose variation is being studied.

**Question**: How difficult did you find DSCI 512 relative to the other courses in the MDS program?

**Options**: 1) Easier than average,  2) Average, 3) More difficult than average.

<br>

| Variable | Name | Type |
|---|---|---|
| Confounder | Sex | category |
| Confounder | Math Skills | category |
| Confounder | Friends who have jobs associated with programming | category |
| Main Covariate | Previous programming experience | category |
| Outcome | Self-perceived difficulty | category |

_A summary table of variables in our analysis_

### Describe how you plan to analyze the survey results (e.g., what statistical test(s) do you plan to employ?).

**Null hypothesis**: The level of programming experience prior to the MDS program does not influence a person's self-perceived difficulty regarding DSCI 512.

**Alternative hypothesis**: The level of programming experience prior to the MDS program influences a person's self-perceived difficulty regarding DSCI 512.

We plane to analyze the survey results in the following ways: 1) exploratory data analysis (EDA)
and 2) Regression Test.???

### Discuss the aspects of the UBC Office of Research Ethics document on Using Online Surveys that are relevant to your proposed survey.

According to the Office of Research Ethics document, the collection of opinions and information are considered personal information if the information could be linked or associated with the individual. Such data, if collected through a survey, must not be stored outside of Canada and should be surveyed through tools hosted within Canada. Some of the variables that we thought about including in our survey were potentially considered "personal information", such as an individual's age or gender. However, due to the small population of our MDS program, it is definitely easy for this type of information to be identifying. As we are also taking a privacy and ethics course, we understand that these issues can bring many unnecessary problems. Ultimately, we decided to some variables, such as age, from our survey, regardless of whether they are confounding variables or not.

In order to comply to the UBC Office of Research Ethics, we would provide a cover letter (consent form) to all survey participants. The cover letter would include:

- the sentence:  “By completing the questionnaire, you are consenting to participate in this research.”
- the purpose of the survey
- a description of the topic of the survey
- contact information
- risks and benefits
- limits to confidentiality
-  a statement that participation is optional
- the UBC Research Participant Complaint Line text
- (if possible) the UBC letterhead

# References:

1: https://www.ncbi.nlm.nih.gov/pubmed/23239826
