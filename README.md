User Stories to Application launch without humans
===
Xingyu Chen
---
Problem Statement
---
	With advances in Internet and technology, thousands of software applications are being designed every day, which also raise the demands for software engineers. It usually takes several years of professional practice to cultivate a experienced SDE. One of the most important part of programming skills is coding standard and conventions, which is gradually being replaced by computer’s work with the help of Natural Language Processing(NLP).
	Engineers are trying to simplify the process of programmers writing professional coding language. Instead, computer can analyze users’ main purposes and build simple but efficient software projects. The interesting part of this technique is how to recognize users’ requirements, where NLP do most of the work. Technology of NLP helps computer separate input natural language into several isolated logic parts. The judging rule sometimes varies depending on the kinds of language or even the users’ habits of using words. This also makes it the most complicated part of the whole process. Machine learning is also being applied in some research. Based on the separated logic parts, computer aggregate these parts together in coding-friendly sequence. The final step of translating logic into operators and functions is relatively a easier part.
Current Research
---
	Most of the current established work focus on the field of generating SQL queries automatically. Translating user questions into SQL queries involves solving problems more than just answering questions and translation. When users are interacting with computers, they usually put forward questions that require complex processing liking reference to combined information of several disparate schemas, which requires heavy analyzing workload on computers. Several attempts have been made on different benchmark datasets to address such problems in the Text-to-SQL task, especially in semantic parsing. Below is an example of well-performed converter based on semantic parsing.
	
![image](https://user-images.githubusercontent.com/84394630/191374117-79b65145-706e-45ca-8654-b435844ef022.png)
Fig 1 SParC dataset

	However, it is true that the presented model perform pretty well on it respective datasets, the generated codes don’t provide the option to test the model on a custom database. Actually, a slight change to the existing database will cause great adjustment to the converting rules. Out of these given models, we can make some changes to EditSQL and manage to run the SParC experiment on a custom SQLite database. These moderations are minor but prove to be an easy workaround to test the performance on customized dataset.
	EditSQL attempts to solve a context-dependent text to SQL query generation task and incorporates interaction histories as well as an utterance-table encoder-decoder unit to robustly understand the context of a user’s utterance (or question). To do this, they use an encoder based on BERT which avails in capturing complex database structures and relate them to the utterances. Thus, given an arbitrary question, the model will most certainly identify correctly the database schema to which the question corresponds.
	Another challenge in generating SQL queries is to fit end-user needs. Most of the users are not technically skilled and don’t know the basic structure of database. For example, many existing libraries require to use column names inside the input requests. But the assumption is actually wrong because most users don’t care about database structure at all. We can’t expect column names or other sorting index to be included in their input natural language queries. 
Conclusion
---
	In conclusion, using NLP as a bridge to connect users’ natural language and computer-side SQL queries is a very promising field of research. Based on these existing well-trained converting models and developing techniques of recognizing users stories, NL-to-SQL technology is expected to be perfected in the near future. This will bring much more energy to the development of software applications.
References
---
[1]https://support.docparser.com/article/1266-what-is-a-parsing-rule-and-how-do-i-create-one
[2]https://towardsdatascience.com/natural-language-to-sql-use-it-on-your-own-database-d4cd5784d081
[3]https://www.indellient.com/blog/transforming-natural-language-text-to-sql/
[4] https://www.geeksforgeeks.org/introduction-to-nosql/
[5]https://stackoverflow.com/questions/54819075/what-are-some-of-the-ways-to-convert-nlp-to-sql

