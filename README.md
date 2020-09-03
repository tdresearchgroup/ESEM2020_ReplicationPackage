# ESEM2020_ReplicationPackage

This replication package contains

(i) The updated Technical Debt Dataset with executable views for all tables (in the .db format)
We construct views of each major table (GIT_COMMITS,REFACTORING_MINER,SONAR_ISSUES, andSONAR_MEASURES) in the Technical Debt dataset by restricting theprojectID to ‘beam’, and label them with a_BEAM prefix (e.g._BEAM_GIT_COMMITS). To extract data for different projects, the "projectID" part of the query needs to be updated to reflect the name of the project under study.

(ii) Codified.csv (in the .csv format) which is the mapping of SonarQube coding violations to the most common code smells by Fowler [1] and the translation of the SonarQube rules violations to bad practices.



Artifacts:
1. [Technical Debt Dataset](https://github.com/tdresearchgroup/ESEM2020_ReplicationPackage/releases/tag/1.0)
2. [codified.csv](https://github.com/tdresearchgroup/ESEM2020_ReplicationPackage/blob/master/codified.csv)



References:
[1] Martin Fowler. 2018.Refactoring: improving the design of existing code. Addison-Wesley Professional.
