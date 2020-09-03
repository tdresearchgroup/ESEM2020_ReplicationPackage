# ESEM2020_ReplicationPackage

The replication package for the paper "Profiling Developers Through the Lens of Technical Debt" (ESEM '20) contains

(i) The updated Technical Debt Dataset with executable views for all tables (in the .db format)

We construct views of each major table (GIT_COMMITS, REFACTORING_MINER, SONAR_ISSUES, and SONAR_MEASURES) in the Technical Debt dataset by restricting the projectID = ‘beam’, and label them with a_BEAM prefix:


|       TABLE       |           VIEW          |
|:-----------------:|:-----------------------:|
|    GIT_COMMITS    |    _BEAM_GIT_COMMITS    |
|    JIRA_ISSUES    |    _BEAM_JIRA_ISSUES    |
| REFACTORING_MINER | _BEAM_REFACTORING_MINER |
|    SONAR_ISSUES   |    _BEAM_SONAR_ISSUES   |
|   SONAR_MEASURES  |   _BEAM_SONAR_MEASURES  |


To extract data for different projects, the "projectID" part of the query needs to be updated to reflect the name of the project under study.


(ii) The Excel spreadsheets (in a compressed folder called graphs) contain the exported data (via comma-separated-values) and the charts for the paper.  Here, anonymizing becomes transparent--each data set is includes (side-by-side) the actual "handle" and the anonymized "...Dev#" (e.g. "CDev1") name used in the paper.  Anyone can easily figure out the name of CDev1: the developer with most commits to project `beam' in the Technical Debt dataset, etc.), given the view in the augmented Technical Debt database.

            cross.xlsx -- the cross-table of SonarQube rule violations
            handles_summary.xlsx -- the long-tail distribution of authors and committers
            refactor.xlsx -- the cross-table of refactoring actions as classified by JIRA
            sonarcnt.xlsx -- the long-tail distribution of SonarQube rule violators



(iii) Codified.csv (in the .csv format) gives our mapping of the SonarQube rule violations to the code smells by Martin Fowler [1] and bad practices.



Artifacts:
1. [Technical Debt Dataset](https://github.com/tdresearchgroup/ESEM2020_ReplicationPackage/releases/tag/1.0)
2. [Graphs](https://github.com/tdresearchgroup/ESEM2020_ReplicationPackage/blob/master/Graphs.rar)
3. [codified.csv](https://github.com/tdresearchgroup/ESEM2020_ReplicationPackage/blob/master/codified.csv)



References:

[1] Martin Fowler. 2018.Refactoring: improving the design of existing code. Addison-Wesley Professional.
