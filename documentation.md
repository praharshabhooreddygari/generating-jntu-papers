generating jntu papers by predicting from the last pages
1.Backend
2.Engine
3.data collection and cleaning
4.rule sets
5.User Interface


| Regulation |                                           CSE course entries |
| ---------- | -----------------------------------------------------------: |
| **R09**    |            **Needs separate counting from the archived PDF** |
| **R13**    | **Needs separate counting from the course-structure tables** |
| **R15**    |                                  **Needs separate counting** |
| **R16**    |                                              **~64 entries** |
| **R18**    |                                               **66 entries** |
| **R22**    |                                               **75 entries** |
| **R25**    |                                              **~75 entries** |



 --> Section A Rules (2-mark questions)


• Each unit must contribute exactly 1 question

• Track which topics from each unit appear most frequently in past papers

• Topics appearing in 3+ past papers = high priority

   -->Section B Rules (10-mark questions)

• Each unit must contribute exactly 1 question

• Track whether a unit historically favors single 10-mark or split 5+5 format

• For split questions, track which topic combinations (a+b) repeat together

• Topics appearing as 10-mark in 3+ papers = high prediction weight

• If a topic appeared in Section A last exam, it's less likely to repeat there next time

  -->General Rules


• If a topic was asked last semester, lower its prediction score

• If a topic was skipped for 2+ consecutive semesters, raise its prediction score

• Weight recent papers more than older ones (e.g., last 3 years > older)



-->Regulation-based Rules

• Each course has a regulation (e.g., R18, R20, R22) with its own syllabus

• Topics deleted in a regulation must be strictly excluded from predictions for that regulation

• Never predict a deleted topic even if it has high historical frequency

• When loading past papers, map them to their regulation — don't mix topics across regulations

So the rule priority becomes:

1. Is the topic in the current regulation's syllabus? → If NO, discard it completely

2. Then apply frequency/recency scoring

This means your system needs a syllabus input per regulation as a base filter before any prediction logic runs.

Do you have the syllabus data for the regulations you're targeting, or is that something your team still needs to gather




-->Deleted Topics

• Problem: Easy to miss deleted topics per regulation

• Solution: Maintain an explicit deleted_topics list per regulation in the syllabus JSON — act as a hard filter before any scoring





