# channel_invites_create
Create a new invite object for the channel. Only usable for guild channels. Requires the CREATE_INSTANT_INVITE permission. All JSON parameters for this route are optional, however the request body is not. If you are not sending any fields, you still have to send an empty JSON object ({}). Returns an invite object

Count | Name | Type | Required        
----|----|----|---- 
1 | channel_id | Snowflake | True
2 | max_age | Integer | False
3 | max_uses | Integer | False
4 | temporary | Boolean | False
5 | unique | Boolean | False
6 | target_type | Integer | True
7 | target_user_id | Snowflake | True
8 | target_application_id | Snowflake | True