# Rocket_Elevators_GraphQL

**Updated on 12/15/21 for use in the Rocket Elevators Customer Portal. 
info added:
Battery, Column and Elevator types and queries.

Implemented using Node.js and Express to deploy this GraphQL API on Heroku. Link: https://jakegapi.herokuapp.com/graphql

Instruction for calling Qureies:

Question 1:
Retrieving current pending interventions with start and end time stamps.
Query 1:

```
{
 pending_interventions {
 	id
	status
	intervention_start
	intervention_end
 }
}
```

Question 2:
Retrieving Intervention info for a specific Interventiong (id: 1 in this example) and modifying the start date.
Query 2:

```
mutation {
	 update_intervention_intervention_start(id: 1) {
		id
		status
		intervention_start
		intervention_end
	 }
}
```

Question 3:
Retrieving Intervention info for a specific Interventiong (id: 1 in this example) and modifying the end date.
Query 3:

```
mutation {
	 update_intervention_intervention_end(id: 1) {
		id
		status
		intervention_start
		intervention_end
	 }
}
```
