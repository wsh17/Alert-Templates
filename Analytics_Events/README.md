# Analytics Events Template

This template can be used to send data from an Alert into Analytics.  So sending from the backend of AppD to the FrontEnd Analytics API.

In order to send the data first we must make a schema for these Alerts and use the template in this repo.  You will need the Account name an also you need to create
a key in Analytics to use. 

**To make the schema:**

Schema curl command below

curl -X POST "https://analytics.api.appdynamics.com:443/events/schema/appdynamicsEvents2" -H"X-Events-API-AccountName:demo-nfr_0c6d5702-141b-4957-879a-xxxxxxxxxxxx" -H"X-Events-API-Key:xxxxxxxx-fb29-4fee-92f1-36274d891496" -H"Content-type: application/vnd.appd.events+json;v=2" -d '{"schema": { "eventApplication": "string", "topSeverity": "string", "eventGuid": "string", "eventTime": "date", "eventTypeKey": "string", "eventDisplayName": "string", "eventSummaryMessage": "string", "eventDeepLink": "string", "eventMessage": "string", "policyName": "string", "actionName": "string", "actionTriggerTime": "date", "eventTier": "string", "eventNode": "string", "eventHealthRuleEvent": "boolean", "eventHealthRuleName": "string", "eventIncidentName": "string", "eventBtPerformanceEvent": "boolean", "accountName": "string" } }'

**Steps**
- create schema in AppD analytics
- setup up template in AppD
- Setup Action in AppD to invoke template
- Setup Policy to utilize action and template
