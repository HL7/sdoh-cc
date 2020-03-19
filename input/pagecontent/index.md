### Overview

| IG Characteristic  |     Value |
|------------------------------------------------------|--------------------------------------------|
|**FHIR Version:** |    FHIR R4 |
|**IG Realm:** |    US |
|**IG Type:** |    STU |
|**Exchange Methods:** |    RESTful Query, Messages, Transactions, Documents, Tasks |
|**IG Dependencies:** |    This IG utilizes and adopts guidance developed in several other FHIR&reg; Implementation Guides. |
{:.table-striped}




| Dependent IG Name         |  IG Code         | Version                      |
|----------------------------------|-------------------------|---------------|
| HL7 FHIR US Core               |  [US Core](http://hl7.org/fhir/us/core/STU3.1)                | Version 3.1.0     |
| Structured Data Capture                         |   [SDC](http://hl7.org/fhir/uv/sdc/2019May)        | Version 2.7.0                     |
| C-CDA on FHIR R4     |     [C-CDA on FHIR](http://hl7.org/fhir/us/ccda/STU1)           | Version 1.0.0              |
| DaVinci Clinical Data exchange            | [CDex](http://hl7.org/fhir/us/davinci-cdex/2019Jun) | Version 1.0.0              |
| Bidirectional Services eReferrals                      |  [BSer](http://hl7.org/fhir/us/bser/) | Version 1.0.0 |
{:.table-striped}

Additional information regarding guidance developed in these IGs is available in the chapters of this IG titled Overview of Data Sharing Methods and Overview of Capability Statements.  




###  Purpose

This HL7&reg; IG defines FHIR R4 profiles, extensions and value sets needed to exchange SDOH content defined by the Gravity Project. It defines how to represent coded content used to support the following care activities: screening, clinical assessment/diagnosis, goal setting, and the planning and performing of interventions. It addresses the need to gather SDOH information in the context of clinical encounters and describes how to share SDOH information and other relevant information with outside organizations for the purpose of coordinating services and support to address SDOH related needs. It also demonstrates how to share clinical data to support secondary purposes such as population health, quality, and research. It supports the following use cases:
1.	Document SDOH data in conjunction with the patient encounter,
2.	Document and track SDOH related interventions to completion,
3.	Gather and aggregate SDOH data for uses beyond the point of care (e.g. public health, population health, quality measurement, risk adjustment, quality improvement, and research.)


### How to Use This Guide

A FHIR IG address the needs of multiple audiences. It provides technical artifacts that assist programmers when implementing standards-based FHIR application program interfaces (APIs) for specific purposes. It provides instructive material that explains how FHIR is used to accomplish specific uses cases. It also provides general information that helps business analysts and technology decision-makers understand the use cases and benefits associated with acheiving specific data exchange capabilities. A FHIR IG is as much a business planning tool as it is an educational resource and a technical specification.

However, one caveat must be clear: this FHIR IG and the other FHIR IG's it depends upon are at low levels of maturity.  Changes to the specification can be major and may happen rapidly as Gravity Project incorporates the full scope of SDOH content domains. Plan accordingly and budget for exploration and potential rework.  For example, the solutions tested at one Connectathon may need to be substantially revised before testing at the next Connectathon. Early engagement in FHIR IG development and sustained collaboration will create the opportunity to have greater impact on the design of these emerging implementer standards.

Additional details are provided in the chapter [Practical Guidance for All Audiences](PracticalGuidanceforAllAudiences.html) for 
* [Implementers with existing systems using proprietary data exchange](PracticalGuidanceforAllAudiences.html#implementers-with-existing-systems-using-proprietary-data-exchange)
* [Implementers currently developing new systems](PracticalGuidanceforAllAudiences.html#implementers-currently-developing-new-systems)
* [Implementers considering future system development](PracticalGuidanceforAllAudiences.html#implementers-considering-future-system-development)
* [Clinical care providers](PracticalGuidanceforAllAudiences.html#clinical-care-providers)
* [Community based organizations](PracticalGuidanceforAllAudiences.html#community-based-organizations)
* [Payer and public health organizations](PracticalGuidanceforAllAudiences.html#payers-and-public-health-organizations)
* [Researchers](PracticalGuidanceforAllAudiences.html#researchers)
* [Technology buyers](PracticalGuidanceforAllAudiences.html#technology-buyers)
* [Patients, care givers, and patient advocates](PracticalGuidanceforAllAudiences.html#patients-care-givers-and-patient-advocates)


### Notes to Reviewers and Balloters

* Review of version 0.0.3 of the IG is intended to gather high-level comments about the overall approach to the Implementation Guide and its positioning in terms of supporting the use cases defined for the Gravity Project. It also is aimed at identifying omissions that impact the quality of the IG. It still contains major IG Build errors and reviewers should be aware of imperfections that still need to be addressed in version 0.0.4. It would be wise to consider the errors associated with a resource as you review the guidance supplied in this version of the IG. The IG Build errors are listed in the QA Report referenced in the footer of the IG. Of the current 199 build errors, there 181 that are considered approved. There are 4 build warnings for examples that lack descriptions. The list of the approved errors that can be disregarded for this version can be found on [Confluence Gravity FHIR IG](https://confluence.hl7.org/pages/viewpage.action?pageId=66922000#GravityFHIRIG-ApprovedSDOHCCFHIRIGErrorsandWarnings).

* Temporary Codes used in this IG will be replaced with permanent codes when they become available and before the IG is published as a Standard for Trial Use (STU).

* For some profiles, value set bindings are set at the wrong level in the data structure. 
 
* For some of the examples, there are known issues/errors with the way IG Publisher is rendering the narrative view of the content. Nonetheless, the narrative view is included (as is) because it is useful to facilitate a general understanding of the profile and may be helpful for generating feedback about how to improve the way narrative is rendered. 

* Message, Transaction, and Workflow Content documentation is incomplete and some of the needed examples have not yet been loaded.

* Capability Statements have been sketched into the document but have not yet been developed and included in the IG.

Feedback on V0.0.3 of the IG should be sent to gravityproject@emiadvisors.net between March 20, 2020 and  April 5, 2020. All of the issues noted above will be addressed in version 0.0.4.  


### Latest Changes

| Number         | Description                                                                                                                                                              |
|---------------|----------------------------------------------------------------------------------------------------|
| 16            | Created Must Support table |
| 15            | Updated Overview of Data Sharing Methods |
| 14            | Updated Security and Consent Considerations |
| 13            | Updated Notes to Reviewers and Balloters  |
| 12            | Added page Practical Guidance for All Audiences |
| 11            | Revisions to profiles and examples |
| 10            | Updates to dependencies to this IG |
| 9            | Updates to Use Case 1 and 2 tables |
| 8            | Change Placeholder Codes to "Temporary codes" and re-work code system naming |
| 7             | Update to How to Read this Guide to align with new publication algorithm                               |
| 6             | Update to Naming Conventions for Implementation Guide Artifacts                                  |
| 5             | Update to Placeholder Code System page                                   |
| 4             | Added notes for Profiles                                       |
| 3             | Updates to Use Case 1                                       |
| 2             | Update naming conventions to sdohcc                                        |
| 1             | Redesign chapters                                         |
{:class="table table-bordered"}
{:.table-striped}


### Acknowledgements
*This section is still under development*

Reserve this area to included acknowledgements for the people and organizations involved in developing and maintaining this Implementation Guide.

There may also be some required copyright acknowledgements for certain Code Systems or other acknowledgements required by HL7 and FHIR.

The Placeholder Code Creation process was originally developed for Elimu profiles and SMART app development. It was modified in the context of creating this IG to make it more broadly applicable.


### Authors
*This section is still under development*

Reserve this area to include authors of this guide.

|**Name:**         | **Org**                                        |
|--------------------------|--------------------------------------------|
|**TBD**             | **TBD**                                         |
{:class="table table-bordered"}
{:.table-striped}


