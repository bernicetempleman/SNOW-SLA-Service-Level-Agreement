# SNOW-SLA-Service-Level-Agreement

- A Service Level Agreement, or SLA, is a record which defines a set amount of time for a task to reach a certain condition. If the task does not reach the condition by a set amount of time, it is marked Breached.

- SLAs are used to ensure that a task reaches end conditions within a certain amount of time.

## Types of Agreements
As per ITIL standards, there are 3 types of agreements:

- Service Level Agreements (SLA) - Service Provider and Customer
- Operational Level Agreements (OLA) - Internal between two teams
- Underpinning Contract - Vendor and Service Provider

## SLA Components
There are three major components that work together to power the Service Level Agreements Plugin:

SLA Definition - the record which defines the conditions that trigger the SLA.

Task SLA - the individual instances of the SLAs associated with particular tasks.

SLA Workflow - the workflow which powers events or actions based on the SLA definition.

## SLA Definition
- The SLA [contract_sla] table contains the definitions of SLAs, to define a specific set of criteria that would result in an SLA being generated.  Define some of the following parameters:

- Table: The task table that the SLA is defined for.
Duration: The time duration in which the service must be provided to the customer.
- Schedule: The schedule, which indicates valid working and non-working days that the service provider follows to deliver the service. The selected schedule is used to determine when the SLA breaches.
- Conditions: The conditions under which the SLA starts, pauses, stops, or resets.

## TASK SLA
- When an SLA definition is triggered against a particular task, the task SLA record is generated and contains all the tracking data for the specific SLA on that record. 

- For example, if an SLA definition exists for P1 incidents a task SLA record attaches to the P1 incident record and captures all the data associated with it. Often there are multiple task SLA records against a single task because many definitions apply. 

- On the Task SLA form, you can also select the target for the SLA: Response, Resolution, or None.

## SLA Workflow
- SLA typically uses workflows to send out the notifications.

- You can create and edit workflows using the Workflow Editor. 
The default workflow that is available with the SLM plugin is Default SLA Workflow

- The Default SLA Workflow creates the events that send out notifications.
For example, it creates an event to send a notification to the user assigned to a task, such as an incident, when the task SLA reaches 50%, 75% or 100% of its allotted time.

- The SLA Notification and Escalation Workflow creates the events that send out notifications. When a task reaches 50% of its allotted SLA duration, Warning notification is sent to the assignee and the user listed in the incident.
- At 75% and 100%, Warning & Breach notification is sent to the assignee and the assignee's manager.


Assignment: 
- Create 10 SLA's in Training Domain
- Override the parent domain by changing the name and insert/ saving.
- Verify only one copy sla in child domain because you overrode the parent

P1 Response - 15 mins (24x7)
P1 Resolution - 2 hrs (24x7)

P2 Response - 1 hr (24x5)
P2 Resolution - 8 hrs (24x5)

P3 Response - 2 hrs (9x5)
P3 Resolution - 1 day / 24 hrs (9x5)

P4 Response - 4 hrs (9x5)
P4 Resolution - 2 days / 48 hrs (9x5)

P5 Response - 8 hrs (9x5)
P5 Resolution - 5 days / 120 hrs (9x5) 

- Create 4 SLA's in EACH Customer domain which should be overridden from Training Domain:

Customer 1 - 

P1 Response - 15 mins (24x7)
P1 Resolution - 2 hrs (24x7)
P2 Response - 1 hr (24x5)
P2 Resolution - 8 hrs (24x5)

Customer 2 - 

P3 Response - 2 hrs (9x5)
P3 Resolution - 1 day / 24 hrs (9x5)
P4 Response - 4 hrs (9x5)
P4 Resolution - 2 days / 48 hrs (9x5)

Customer 3 - 

P5 Response - 8 hrs (9x5)
P5 Resolution - 5 days / 120 hrs (9x5)

![image](https://user-images.githubusercontent.com/12488769/147860136-8681cdf9-d9e7-44fd-8c56-3ece022bba55.png)

