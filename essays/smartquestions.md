---
layout: essay
type: essay
title: "There is no such thing as a stupid question, or is there?"
# All dates must be YYYY-MM-DD format!
date: 2023-01-26
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

Everyone has questions, and in general, everyone is looking for answers to those questions. When learning a new skill, questions are especially important for understanding the skill. In fact, asking questions is more than encouraged for new learners in the classroom and jobs. However, it is also up to the new learner to ask smart questions.

"There is no such thing as a stupid question." This is a common quote used by many, and most abide by this statement as well. So what do I mean by asking a smart question? I am specifically referring to how the question is structured and presented. There is truly no such thing as a stupid question, but how that question is phrased can be incredibly stupid. In the space of software engineering (and basically everywhere, actually), how a question is asked is very important because you will only get your answer from somewhere else. Experts are people who can readily answer questions about their field, but experts are people and people are busy. 

As a side note, when people say "There is no such thing as a stupid question", they are usually referring to the content of a question. There is no shame in asking about a topic you don't know much about, but there is shame in demanding free answers from others when the user's guide is right there.

## Smart Questions Get Smart Answers

A question of "How do I fix this???" followed by a screenshot of 200 lines of code is maybe received or most likely dismissed with disdain. Best case you'll get a response heavily dusted with salt and a manual thrown in your direction. 

On the other hand, a question of "I'm encountering an error with a section of my code, I've looked up the error message but none of the fixes I've found are working here. I've singled out the problem in this snippet here." followed by the code that causes the error and the offending error, both of which are text and not screenshots. 

Though both questions are essentially asking for help in the asker's code, the second question gives more information in a more accessible manner. If your question is easier to understand, it is more liable to get an answer. Nobody wants to look through 200 lines of code, and what does "How do I fix this???" even mean?

Asking smart questions is important especially so in software engineering because there are many people learning and the learning process varies. The experts can't answer everyone's questions immediately, much less if they're answering entirely for free. On forums or mailing lists such as StackOverflow, this is usually the case. Plus, as problems become more advanced, surpassing just code and perhaps into hosting a server, there are more variables that come into play. It's difficult enough to diagnose a problem over the internet, through text, and differing timezones. Thus, having information as clear as possible and being specific in a question is more likely to grab an expert's attention.

## StackOverflow Questions

This question asks ["Why is processing a sorted array faster than processing an unsorted array?"](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) While not a question about an error they have received, it was a behavior that the asker observed to be peculiar and they wanted to know more about it. The behavior showed that a sorted array was processed much faster in a loop than an unsorted one. First off, a very clear and concise question! The asker then describes the behavior and includes the code in C++ that shows it. They also discuss the steps they have taken to try and figure it out themselves: They assumed the behavior was a result of a language or compiler anomaly, but testing a similar case in Java yielded a similar result. Thus they have taken to the forum boards, awaiting for an expert to enlighten them on their curiosity. 

(Note: Asking this question now may not be well received because it is very easy to find the answer through Google. However, this question was asked in *2012* and was probably one of the first on a forum such as this)

Answered not a day later, an expert comes sweeping in with an incredibly detailed explanation and even a helpful analogy. They explain that this behavior is caused by branch prediction failure. In (very) short, branch predictors try to predict where a branch will go at a fork. If the array is sorted, it's easier to predict the correct path and the processor chugs along. If the array is unsorted, the processor has to slow down, wait for previous instructions to be completed, find the correct path, and continue on its merry way.

As an added bonus, since this question was asked and answered on a public forum, everyone has access to this answer without the need to bother someone else about it. Even better, the explanation has been continually updated with how various compilers react to this problem. The last update was in August 2022!

That was a fantastic example! What about another?

This next question's title states "Do while" loop should be stopped, by entering a char variable, if it is 'y' or 'Y'. When string is entered it goes to infinite loop'." The asker's code is looping infinitely when they key in an incorrect input for the program. A valid question, I'm pretty sure this is a buffer input issue and those were nervewracking when I first learned about them. However, the asker attaches the entire *178* lines of code. The title isn't even a question, it's a declaration of the problem. While having a problem with the title is fine, the asker's question must also be easy to locate, preferably the first thing anyone sees when they click on the issue. How else would anyone know what answer you want?

The day this question was asked, it had already received 2 downvotes. Ouch. Someone else has also commented suggesting that the problem probably does not need all 178 lines of code for demonstration. They then very kindly linked the asker to a guide for creating a minimal reproducible example. The issue is certainly salvageable, it's really the 178 lines of code no one wants to look through that is the problem with the problem. 

Oh man, never mind actually. The question was straight up removed after a couple of hours. My condolences to the asker.

## Ask the smart questions!

Questions are important, but smart questions are even more so. A smart question is always a question an expert is happy to answer. Those questions demonstrate that you the asker are actually willing to learn and try to understand their field of expertise. The reason why these experts answer questions on forums such as StackOverflow anyways is not only that they emjoy helping others, they enjoy hard and thought-provoking questions to solve. I know it's not everyone's cup of tea, but a hard homework question can be fun to solve sometimes. In the end, both you and the expert will learn something new!