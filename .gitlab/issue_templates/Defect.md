# TODO for creating a Defect
* Add [Title]
* Add [Metadata], [Summary], [Funcational Impact], [Pre Conditions], [Steps To Reporduce], [Post Conditions], [Expected Bahavior], [Actual Behavior], [Logs, Screenshots, Test Scripts]
* Add [Backlog], [Defect] labels
* Depending on severity of Defect please add [Blocker] or [Critical] labels
* Depending on priority of Defect please add [Urgent Priority], [Critical Priority], [High Priority], [Medium Priority], or [Low Priority]
* Remove TODO list

## Metadata
| Key Metric                | Value |
| --------                  | ------|
| Name of Reporter          | Jane Doe |
| Who Detected              | [QA|External Customer|Internal Customer|Development] |
| How Detected              | [Testing|Review|Walkthrough|JAD] |
| Email of Reporter         | janedoe@deloitte.com |
| Name of Tester            | John Doe |
| Environment               | [Dev,Test,Stage,Prod] |
| Version or Build          | Genesys 0.1.0.0100 |
| Docker Image              | Genesys 0.1.0.0100 |
| Module or Component       | Cache.Redis        |
| *Platform and OS Verison  | Windows 10.1.1100   |
| **Audience Affected       | [Low|Medium|High]   |

* *Add Additional Builds and Platforms Test On below
* **See Audience Affected range below

## Additional Builds and Platforms Tested On:
| Build                 | Platform          |
| ----------            | ----------------- |
| Genesys 0.1.1.0.140   | Windows 10.1.1100   |
| Genesys 0.1.1.0.140   | Windows Server 2012 |
| Genesys 0.1.2.0.160   | Windows 10.1.1100   |

## Audience Affected
*A range to gauge how much of the user base is affected by the bug*
* Low       -> 0%-30%
* Medium    -> 30% - 70%
* High      -> 70% - 10%

## Summary
*A short description of the defect* 

## Functional impact
*What is the functional issue?*

## Pre Conditions
*Optional conditions that must exist prior to reproducing*

## Steps To Reproduce
*What is the smallest, simplest set of steps to reproduce the issue. If needed, provide a project that demonstrates the issue.*  
1. Step One
2. Step Two
3. Step Three

## Post Conditions
*Optional conditions that must occur at end of steps*

## Expected Results
*What would you expect to happen if there wasn't a defect*

## Actual Results
*What is actually happening*  

## References and Attachements
*Logs, Screenshots, Test Scripts, etc.*  

## Further technical details
*Optional, details of the root cause if known*

# TODO for processing a Defect
* Prioritize
* Determine any existing related workitems 
* Update [Metadata], [Related Workitems] and dependencies
* Assign to developer for review and investigation

## Metadata
| Key Metric                | Value |
| --------                  | ------|
| Developer Contact         | Jay Doe |
| Planned Fix Release       | Release Milestone Sprint 10 |

## Related Workitems
* Related Epic
  - [ ] #3
* Related Features
  - [ ]  
* Related Stories
  - [ ]  
* Related Tasks
  - [ ]  
* Dependency (Pre-Conditional Tasks) 
  - [ ] 
  
## Functional impact on design
*How does the functional issue affect the design and code?*
