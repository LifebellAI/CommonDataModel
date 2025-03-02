NOTE ABOUT CDM v6.0
====================

Please be aware that v6.0 of the OMOP CDM is **not** fully supported by the OHDSI suite of tools and methods. The major difference in CDM v5.3 and CDM v6.0 involves switching the \*_datetime fields to mandatory rather than optional. This switch radically changes the assumptions related to exposure and outcome timing. Rather than move forward with v6.0, CDM v5.4 is actively in production to address additions to the model that have been requested by the community while retaining the date structure of medical events in v5.3. Please see our [roadmap](https://github.com/OHDSI/CommonDataModel/projects/3) for more information on which proposals will be included in CDM v5.4. For new collaborators to OHDSI, please transform your data to [CDM v5.3](https://github.com/OHDSI/CommonDataModel/releases/tag/v5.3.1) until such time that CDM v5.4 is ready for release. 

Common Data Model v6.0
=================

 See full CDM specifications on our [website](https://lifebellai.github.io/CommonDataModel/index.html).


Release Notes for v6.0
=============

### This version address the following issues/pull requests:

#### CDM
* [#81](https://github.com/OHDSI/CommonDataModel/pull/81) Adds the COST table
* [#137](https://github.com/OHDSI/CommonDataModel/pull/137) Adds the SURVEY_CONDUCT table
* [#181](https://github.com/OHDSI/CommonDataModel/pull/181) Adds the LOCATION_HISTORY table
* [#91](https://github.com/OHDSI/CommonDataModel/issues/91) Latitude and longitude added to LOCATION table
* [#107](https://github.com/OHDSI/CommonDataModel/issues/107) Contract owner information added to PAYER_PLAN_PERIOD 
* [#120](https://github.com/OHDSI/CommonDataModel/pull/120) New fields added to PAYER_PLAN_PERIOD (PAYER_CONCEPT_ID, PLAN_CONCEPT_ID)
* [#166](https://github.com/OHDSI/CommonDataModel/issues/166) Record inserted into METADATA to document CDM version
* [#172](https://github.com/OHDSI/CommonDataModel/pull/172) NOTE_EVENT_ID and NOTE_DOMAIN_ID (NOTE_EVENT_TABLE_CONCEPT_ID) added to NOTE
* [#198](https://github.com/OHDSI/CommonDataModel/pull/198) Change IDs to BIGINT 
* [#153](https://github.com/OHDSI/CommonDataModel/issues/153) ADMISSION_SOURCE_CONCEPT_ID changed to ADMITTED_FROM_CONCEPT_ID 
* [#214](https://github.com/OHDSI/CommonDataModel/issues/214) All CONCEPT_IDs are mandatory except for UNIT_CONCEPT_ID, VALUE_AS_CONCEPT_ID, and OPERATOR_CONCEPT_ID 
* [#164](https://github.com/OHDSI/CommonDataModel/issues/164) Any reference to DOMAIN_ID was switched to EVENT_FIELD_CONCEPT_ID
* [#212](https://github.com/OHDSI/CommonDataModel/issues/212) CDM Results schema created with tables COHORT and COHORT_DEFINITION
* [#210](https://github.com/OHDSI/CommonDataModel/issues/210) DEATH table removed and cause of death now stored in CONDITION_OCCURRENCE
* [#166](https://github.com/OHDSI/CommonDataModel/issues/166) Record inserted into METADATA identifying the CDM version
* [#172](https://github.com/OHDSI/CommonDataModel/issues/172) Added NOTE_EVENT_ID and EVENT_FIELD_CONCEPT_ID to NOTE table

#### Vocabulary
* [#186](https://github.com/OHDSI/CommonDataModel/issues/186) Keep deprecated CPT concepts active and standard
* [#85](https://github.com/OHDSI/CommonDataModel/issues/85) NOTE_NLP concepts added

#### Wiki
* [#188](https://github.com/OHDSI/CommonDataModel/issues/188) Added foreign key description to wiki files
* All [THEMIS](https://github.com/OHDSI/THEMIS/issues) rules added to wiki

Additional Updates
==================

* DATE fields are now optional and DATETIME fields are mandatory

---------
  
This repo contains the definition of the OMOP Common Data Model. It supports the SQL technologies: BigQuery, Impala, Netezza, Oracle, Parallel Data Warehouse, Postgres, Redshift, and SQL Server. For each, the DDL, constraints and indexes (if appropriate) are defined. 


Versions are defined using tagging and versioning. Full versions (V6, 7 etc.) are usually released at most once a year and are not backwards compatible. Minor versions (V5.1, 5.2 etc.) are not guaranteed to be backwards compatible though an effort is made to make sure that current queries will not break. Micro versions (V5.1.1, V5.1.2 etc.) are released irregularly and often, and contain small hot fixes or backward compatible changes to the last minor version.
