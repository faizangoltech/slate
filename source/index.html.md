--- 

title: Swagger Test Page 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 


search: true 

--- 

# Introduction 

This is a test API Docs demo for Alive5 APIS 

**Version:** 1.0 

[Find out more about Alive5](https://www.alive5.com/) 

# Authentication 

|apiKey|*API Key*|
|---|---| 

# /1.0/OBJECTS/TAGS/LIST
## ***GET*** 

**Description:** List of all tags

### HTTP Request 
`***GET*** /1.0/objects/tags/list` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Tag ID, Tag Label |

# /1.0/OBJECTS/CHANNELS-AND-USERS/LIST
## ***GET*** 

**Description:** List of all channels and users that are in each channel.

### HTTP Request 
`***GET*** /1.0/objects/channels-and-users/list` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Channel ID, Channel Label, User ID, User Screen Name, User Email, User Role, User Created Time |

# /1.0/ACCOUNT
## ***GET*** 

**Description:** Gets Account informantion.

### HTTP Request 
`***GET*** /1.0/account` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Org_name |

# /1.0/CONVERSATIONS/SMS
## ***GET*** 

**Description:** Output all SMS conversations based on specific date range.

### HTTP Request 
`***GET*** /1.0/conversations/sms` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date-start | params | Start date | No | string |
| date-end | params | End date | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | org name, alive5_sessionID, Start time, Channel, Assigned To, Tags, (contacts) first name, (contacts) last name, (contacts) email, (contacts) phone, (contacts) notes, Chat Conversation |

# /1.0/CONVERSATIONS/SMS/SEND
## ***POST*** 

**Description:** Send a single SMS message from an Alive5 phone number to a mobile phone number.

### HTTP Request 
`***POST*** /1.0/conversations/sms/send` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| phone_number_from | body | SMS Phone Number (Alive5) | Yes | text |
| phone_number_to | body | SMS Phone Number (Customer) | Yes | text |
| message | body | Text of what to send out | Yes | text |
| assigned_channel | body | Channel ID | Yes | text |
| assigned_user | body | User ID | Yes | text |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Successful |

# /1.0/CONVERSATIONS/LIVECHAT
## ***GET*** 

**Description:**  Output all live chat conversations based on specific date range.

### HTTP Request 
`***GET*** /1.0/conversations/livechat` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date-start | params | Start date | No | string |
| date-end | params | End date | No | string |
| page | params | a numeric value such as 1, designating the set of pages based on the limit value | Yes | string |
| limit | params | a numeric value such a 100, the number of results to return at once. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | org name, alive5_sessionID, Start time, Channel, Assigned To, Tags, (contacts) first name, (contacts) last name, (contacts) email, (contacts) phone, (contacts) notes, user agent, IP address, City, State, Country, ZIP Code, Referrer URL, Page URL, Chat Conversation |

# /1.0/CONVERSATIONS/FBM
## ***GET*** 

**Description:** Output all Facebook Messenger conversations based on specific date range.

### HTTP Request 
`***GET*** /1.0/conversations/fbm` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date-start | params | Start date | No | string |
| date-end | params | End date | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | org name, alive5_sessionID, Start time, Channel, Assigned To, Tags, (contacts) first name, (contacts) last name, (contacts) email, (contacts) phone, (contacts) notes, Chat Conversation |

# /1.0/CONVERSATIONS/SUMMARY
## ***GET*** 

**Description:** Output all Facebook Messenger conversations based on specific date range.

### HTTP Request 
`***GET*** /1.0/conversations/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date-start | params | Start date | No | string |
| date-end | params | End date | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | visitors_web, visitors_fbm, visitors_sms, contacts_web, contacts_fbm, contacts_sms |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
