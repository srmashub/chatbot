## greet
* greet
    - utter_greet
	- action_chat_restart

## thank
* thank
    - utter_thank
	- action_chat_restart

## bye
* bye
    - utter_bye
	- action_chat_restart










## trigger_jenkinsjob1
* trigger_jenkinsjob
	- action_jenkins
	- slot{"requested_slot": "jenkinsjob"}
* inform{"jenkinsjob": "sampleapp_ppl"}
	- action_jenkins
	- slot{"jenkinsjob": "sampleapp_ppl"}
	- action_chat_restart
	
	











## trigger_deploy1
* trigger_deploy
	- action_jenkins_param
	- slot{"requested_slot": "appname"}
* inform{"appname": "deploytest"}
	- action_jenkins_param
	- slot{"appname": "deploytest"}
	- slot{"requested_slot": "environment"}
* inform{"environment": "uat"}
	- action_jenkins_param
	- slot{"environment": "uat"}
	- action_chat_restart
	



## check_jira_request1
* check_JIRA_Status
    - action_GetJIRAStatus_param
	- slot{"requested_slot": "JIRAID"}
* inform{"JIRAID": "TS-3"}
	- action_GetJIRAStatus_param
	- slot{"JIRAID": "TS-3"}
	- action_chat_restart
	
	
## check_jira_request2
* check_JIRA_Status
    - action_GetJIRAStatus_param
	- slot{"requested_slot": "JIRAID"}
* inform{"JIRAID": "TS-20"}
	- action_GetJIRAStatus_param
	- slot{"JIRAID": "TS-20"}
	- action_chat_restart
	
## create JIRA ISSUE1
* create_JIRA_request
	- action_createJIRArequest_param
	- slot{"requested_slot": "description"}
* inform{"description": "description"}
	- action_createJIRArequest_param
	- slot{"description": "description"}
	- slot{"requested_slot": "summary"}
* inform{"summary": "summary"}
	- action_createJIRArequest_param
	- slot{"summary": "summary"} 
	- action_chat_restart
	
## create JIRA ISSUE2
* create_JIRA_request
	- action_createJIRArequest_param
	- slot{"requested_slot": "description"}
* inform{"description": "test"}
	- action_createJIRArequest_param
	- slot{"description": "test"}
	- slot{"requested_slot": "summary"}
* inform{"summary": "access required"}
	- action_createJIRArequest_param
	- slot{"summary": "access required"}
	- action_chat_restart




		
## CHECK SERVICE1
*check_service
	- action_checkservice
	- slot{"requested_slot": "servicename"}
* inform{"servicename": "google"}
	- action_checkservice
	- slot{"servicename": "google"}
	- action_chat_restart

## CHECK SERVICE2
*check_service
	- action_checkservice
	- slot{"requested_slot": "servicename"}
* inform{"servicename": "accenture"}
	- action_checkservice
	- slot{"servicename": "accenture"}
	- action_chat_restart

## CHECK SERVICE3
*check_service
	- action_checkservice
	- slot{"requested_slot": "servicename"}
* inform{"servicename": "cnbc"}
	- action_checkservice
	- slot{"servicename": "cnbc"}
	- action_chat_restart
	
## CHECK SERVICE4
*check_service
	- action_checkservice
	- slot{"requested_slot": "servicename"}
* inform{"servicename": "travelers"}
	- action_checkservice
	- slot{"servicename": "travelers"}
	- action_chat_restart

## CHECK SERVICE5
*check_service
	- action_checkservice
	- slot{"requested_slot": "servicename"}
* inform{"servicename": "yahoo"}
	- action_checkservice
	- slot{"servicename": "yahoo"}
	- action_chat_restart








##NEW STORY
* request_restaurant
     - action_search_restaurants
     - slot{"requested_slot": "cuisine"}
* inform{"cuisine": "chinese"}
     - action_search_restaurants
     - slot{"cuisine": "chinese"}
     - slot{"requested_slot": "people"}
* inform{"people": 3}
   - action_search_restaurants