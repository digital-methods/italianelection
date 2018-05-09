# Methodology & Research Design

In our study on the Italian elections, we decided to turn to the electorate, in order to understand answer a crucial question: what were Italian voters talking about in the run up to the national ballot? We thought it would be interesting not to focus on the speeches or the interviews of the candidate, considering the themes that each party brought forward are easily identifiable through a quick look at their program, and therefore a digital analysis might have brought little added value. Instead, by focusing on what the voters were saying, we wanted to look at whether and how citizens pick up the rhetoric of politicians, and which topics they considered most important and valuable to be discussed on a social media platform like Facebook. Therefore, we proceeded with the selection of our sample.

In terms of time, we chose to focus on the one month before the date of the election, so from February 2nd, 2018 to March 4th 2018. This choice is justified by the fact that under Italian law, this is the official period of campagna elettorale (electoral campaigning). However, we still needed to decide which comment section(s) we wanted to analyze. In the beginning we considered to take into consideration the comment section of the Facebook pages of the biggest Italian newspapers. This turned out to be rather impractical for a number of reasons. First, the news are not only about domestic politics. More and more newspapers share topics related to much more trivial news that would have represented a great amount of noise in our sample. Second, and more importantly, with the breakout of the “Cambridge Analytica” scandal, Facebook proceeded to change his API policy, making scraping a large amount of posts impossible for us.

## Research question

Hence, we opted instead to look at the comments of the personalities which led (formally or informally) the current three biggest parties in the Italian Parliament: **Matteo Renzi, Luigi di Maio, and Matteo Salvini**. Considering that politicians post in a smaller amount than newspapers, the scraping turned out to me easier and the interest for the analysis remained. By looking at what supporters or detractors were talking about under their Facebook statuses or shared links, we thought we could get an idea about

1. **what issues were brought up the most by them, and in particular** 

2. **whether they reflected the themes offered by the platforms of the politicians**. 

3. **what emotions were related to these issues, and did they differ between politicians**

## Hypothesis 

Finally, we formulated the hypothesis we wanted to test through our study, that is the following: 

> **“The comments to the posts of political leaders mirror the themes and the rhetoric present by each of their political platforms".**

When looking at the specific cases, this hypothesis eventually turns into **three different hypotheses** to test for each candidate. By looking at the different party programs, we expected the following. 

1. With regards to Renzi (Partito Democratico), we expected to see a discourse revolving around the _economic activity_ and _jobs_ with a special focus on _schooling_, _lower taxes_ and some hints of more _European cooperation_. 
2. As for Di Maio (Movimento 5 Stelle), we expected discussions on what seemed to be most important – and controversial – point of his party’s campaign, that of the _basic universal income_. Since that, together with _lower taxes_, this was one of the few prominent topics we could identify, we were interested in exploring what 5 Stars voters also discussed about. 
3. Finally, for Salvini (Lega Nord) our main hypothesis was related to a strong focus on _anti-immigration rhetoric_, which is one of the major stances of the right-wing candidate. In addition, his platform promoted _anti-European stances_, proposals for _lower taxes_ and _pension reforms_: all topics we predicted that would lead the public discourse of his party’s voters.

## Methods 

In order to test these hypothesis, we decided to run topic models using Latent Dirichlet Allocation (LDA) on a corpus of Facebook comments to the posts published by the politicians. Topic modeling algorithms are a tool of machine learning which analyze a textual corpus to identify coherent ‘topics’ and the strength to which they appear in each document. LDA, popularized by Blei, Ng, and Jordan, is a simple topic model. Put simply, it groups terms that appear more frequently than expected by chance to create topics. With the CorText platform, our tool for analysis, the researcher can set a specific number of topics or ask the algorithm to find the optimal number. Due to the size of our database and our interest in the most prominent themes in the comments, topic modelling is an ideal tool.

We compiled the database for each of the politicians individually, and subsequently merged them together to create a separate database of all of the comments. The merged database would serve as a baseline to which the individual politicians could be compared. In other words, by examining the most salient topics in the comments overall, we could compare the topics for each of the politicians and see where they converged and where they differed. After uploading and parsing each of the databases, we created a number of topic models. 

Though we used the built-in “text cleaning” functions to clean the database of stop-words, we still found a considerable portion of meaningless words (e.g., slang, misspellings, etc.) throughout the topics. We decided to refine each of the politician databases to only include words that appear in at least ten percent of the comments. We refined the overall database further, focusing specifically on comments that were themselves commented on. We then created topic models of ten topics for each of these reduced databases. After identifying the coherent topics in the overall database, we ran a contingency matrix between the politicians and the topics. This illustrated the degree to which each of the topics were correlated to comments on each politician’s page.

To examine the sentiments expressed towards each politician, we conducted a sentiment analysis of each of the posts. Unfortunately, the algorithm was completely inaccurate. In order to capture another kind of emotional response, we decided to look at posts that received at least one “reaction”: like, love, angry, ‘haha’, ‘wow’, and sad. After extracting comments with each reaction and forming smaller databases, we created models of ten topics (the optimal number) and corresponding contingency matrices. Please refer to the “Data and Discussion” tab for our results. 

Source: DiMaggio, Nag, and Blei, 2013; Blei, 2012; Blei, Ng, Jordan, 2003

