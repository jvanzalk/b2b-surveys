# b2b-surveys

Leading survey tools (e.g., Qualtrics, Survey Monkey) fit most **B2C companies** needs out of the box. However, **B2B companies** often need to aquire information from multiple people at a single company, and this is where built-in functionality can fall short.

Companies are diverse in terms of how they are structured (e.g., the departments they have, the job titles they use). For this reason, it's very tricky for B2B companies to know what person at a company will have the information that they need.

So there is a need for B2B companies to be able to send a survey out that can be forwarded to different individuals at a company. If one individual cannot answer something, they can forward it to their colleague.

This repository provides an example of how this can be accomplished using the Qualtrics API. 

This is not a perfect solution. Unfortunatley, people can't collaborate on a qualtrics survey like they would in a Google Doc. But, it's a nice work around for surveyors at B2B companies.

## Survey Design

The survey design implemented is made up of the 3 parts: (1) a screening section where respondents select the information that they can provide, (2) the survey questions, and (3) a referal section where respondents can refer a colleague to provide the information that they could not.

<img src= "https://github.com/jvanzalk/b2b-surveys/blob/master/images/survey_design.JPG" width="500">

The screening section contains display logic so that respondents can only select topics that their company as a whole hasn't completed:

<img src= "https://github.com/jvanzalk/b2b-surveys/blob/master/images/topic_question.JPG" width="500">

The survey flow calls out embedded data that comes from customized survey links which control what the respondent sees. For example, if a respondent completes topic 1 (or T1) and refers a colleague to complete topic 2, the colleague will be sent a survey link with T1_Completed=1. The display logic will then prevent them from answering the questions under topic 1 too. 

<img src= "https://github.com/jvanzalk/b2b-surveys/blob/master/images/survey_flow.JPG" width="500">



