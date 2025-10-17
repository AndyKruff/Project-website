---
layout: default
title: Interactive Search Dataset & Resources
---

# Interactive Search Dataset & Resources

Explore the user study dataset, the loggable interactive search platform, and user profile data.  
**GitHub Repository:** [PLACEHOLDER_LINK](https://github.com/your-repo-link)

---

## Dataset and System

We used the [Conversational Argument Retrieval dataset](https://github.com/Touché-2020/args.me) from Touché 2020, based on the args.me corpus of Debate.org threads. The dataset contains 387,606 arguments across 50 TREC-style topics. For this study, we selected 26 topics that were relevant and controversial to elicit varying levels of interest per participant. Arguments that were too short (<150 characters) or excessively long (>3,000 characters) were removed.

Our search platform allows:
- Query submission and reformulation
- Display of top-10 arguments per page (title + snippet, expandable to full text)
- Saving documents as supporting or opposing a stance
- Reviewing saved documents

> Note: Argument titles were automatically generated using Llama3.

---

## Data Collection

### Participant Recruitment

Participants were students of Information Science at a German university. Participation was voluntary, anonymous (pseudonyms), and compensated with course credits.

### Questionnaires

- **Pre-study questionnaire:** demographics, socioeconomic background, online activity, search experience, interest rating for 26 topics.
- **Post-study questionnaire:** stance change, task difficulty rating.

### Perceptual Speed Test

Participants completed a modified *Finding A’s Test*, classifying character strings for **ε** and **¥** (press `j` = both present, `n` = not present). Time limit: 2 minutes, with a 30-second practice phase.

---

## Study Procedure

- Each participant worked on two topics: one of high interest and one with no interest.
- Task time limit: 10 minutes
- Topic order pseudo-randomized
- Interactions logged: queries, document views, saving, navigation
- Optional comments collected (original + machine translation)

---

## Resources

### Interaction Log Dataset

- 122 sessions evenly distributed between high- and no-interest topics
- Each interaction contains type, timestamp, session ID, document rank, score, and length
- Stop decisions and reasons were recorded

### lisp – Loggable Interactive Search Platform

![Search Interface](./images/interface_clicked.png)

- Enter queries, view results, navigate pages
- Save documents with stance color coding
- Summary popup at the end of each session
- Customizable: labels, logging, dataset
- [Demo Perceptual Speed Test](https://andykruff.github.io/demo-ps-test/)

### User Profile Data

- Demographics, search experience, perceptual speed
- Average perceptual speed: 101.66 (median: 103, SD: 28.51)

![Demographics](./images/demographics_notitle.png)
![Perceptual Speed Scores](./images/ps_scores_new_bold.png)

---

## Potential Applications

This dataset and platform can be applied in a variety of research and development areas:

- **Interactive Information Retrieval:** studying user behavior in argument retrieval and exploratory search  
- **Personalization and Recommendation:** investigating the influence of topic interest and perceptual speed on search strategies  
- **User Modeling:** training models to predict search actions, stopping behavior, or stance selection  
- **Human-Computer Interaction:** evaluating interface designs for search platforms  
- **Educational Technologies:** assessing learning and information acquisition strategies  

![Markov Model of User Interactions](./images/MM_withnumbers.png)

*Figure: Markov model of user interactions. Transitions from states marked with * to **REVIEW** and from **REVIEW** back to those states were omitted for clarity. Transition probabilities indicated at the arrows and mean interaction times per state are averaged across all sessions. As **MARK** and **PAGE** have no actual duration, they are assigned a nominal value of 1 second for completeness.*
