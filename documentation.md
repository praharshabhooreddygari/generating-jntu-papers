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



  Section A Rules (2-mark questions)


• Each unit must contribute exactly 1 question

• Track which topics from each unit appear most frequently in past papers

• Topics appearing in 3+ past papers = high priority

   Section B Rules (10-mark questions)

• Each unit must contribute exactly 1 question

• Track whether a unit historically favors single 10-mark or split 5+5 format

• For split questions, track which topic combinations (a+b) repeat together

• Topics appearing as 10-mark in 3+ papers = high prediction weight

• If a topic appeared in Section A last exam, it's less likely to repeat there next time

  General Rules


• If a topic was asked last semester, lower its prediction score

• If a topic was skipped for 2+ consecutive semesters, raise its prediction score

• Weight recent papers more than older ones (e.g., last 3 years > older)




