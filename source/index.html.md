--- 

title: Alive5 API-Docs 

language_tabs: 
   - shell 

toc_footers: 
  - <a href='#'>Sign Up for a new Account </a> 
  - <a href='https://app.alive5.com/signup'>Documentation Powered by Alive5</a>

includes: 
   - errors 

search: true 
--- 

# Introduction 

This is a API Docs for Alive5 Users 

**Version:** 1.0 

[Find out more about Alive5](https://www.alive5.com/) 

# Authentication 

|apiKey|*X-A5-APIKEY*|
|X-A5-APIKEY|fb359c68-6956-4db9-8b0b-9f96654aca1f| 

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/ACCOUNT
## ***GET*** 

**Description:** Gets Account information.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/account` 

**Responses**

| Value | Description |
| ---- | ----------- |
| email | Email |
| api_key | API Key |
| org_name | Org Name |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/OBJECTS/TAGS/LIST
## ***GET*** 

**Description:** List of all tags

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/objects/tags/list` 

**Responses**

| Value | Description |
| ---- | ----------- |
| tag_id | Tag ID |
| tag_label | Tag Label |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/OBJECTS/CHANNELS-AND-USERS/LIST
## ***GET*** 

**Description:** List of all channels and users that are in each channel.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/objects/channels-and-users/list` 

**Responses**

| Value | Description |
| ---- | ----------- |
| channel_id | Channel ID |
| channel_label | Channel Label |
| agents | Agents Information |
| email | Email |
| created_at | Time of Creation |
| screen_name | Agent Name |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/SMS
## ***GET*** 

**Description:** Output of all SMS conversations based on a specific date range.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/conversations/sms` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date_start | params | Start date | No | string |
| date_end | params | End date | No | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| org_name | Alive5 Org Name |
| alive5_sessionID | Alive5 Session ID |
| start_time | Start Time |
| end_time | End Time |
| channel_id | Channel ID |
| channel_name | Channel Name |
| crm_id | CRM ID |
| agent_id | User ID |
| assigned_to | Assigned to UserName |
| tags | Tags |
| contacts_first_name | Clients First Name |
| contacts_last_name | Clients Last Name |
| contacts_email | Clients Email |
| contacts_phone | Clients Phone Number |
| contacts_notes | Clients Notes |
| alive_sms_phone_number | Channel associated Phone Number |
| chat_conversation | Chat Conversations |
| created_at | Time of creation |
| created_by | Created By Client/User |
| message_content | Content of the Message |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/SMS/SEND
## ***POST*** 

**Description:** Send a single SMS message from an Alive5 phone number to a mobile phone number.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/conversations/sms/send` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| phone_number_from | body | SMS Phone Number (Alive5) | Yes | text |
| phone_number_to | body | SMS Phone Number (Customer) | Yes | text |
| message | body | Text of what to send out | Yes | text |
| channel_id | body | Channel ID | Yes | text |
| user_id | body | User ID | Yes | text |

**Responses**

| Value | Description |
| ---- | ----------- |
| error | Response Message |
| newThread | New Message Information |
| phone_mobile |  |
| created_at | Time of Creation |
| thread_id | Thread ID |
| thread_type | Thread Type |
| assignedTo | Agent ID |
| timestamp | Time Stamp |
| updated_at | Clients Phone Number |
| crm_id | CRM ID |
| platform | Platform |
| channel_id | Channel ID |
| status_timestamp | Status | Time Stamp |
| org_name | Org Name |
| lastmessage_at | Time of Last Message |
| thread_status | Status |
| crmData | CRM Information |
| last_name | Clients First Name |
| first_name | Clients Last Name |
| crm_type | CRM Type |
| email | Email |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/SMS/PUSH
## ***POST*** 

**Description:** Send a single SMS message from an mobile phone number to a Alive5 phone number.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/conversations/sms/push` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| phone_number_from | body | Phone Number (Customer) | Yes | text |
| phone_number_to | body | Phone Number (Alive5) | Yes | text |
| message | body | Text of what to send out | Yes | text |

**Responses**

| Value | Description |
| ---- | ----------- |
| assignedTo | Agent Name |
| channel_id | Channel ID |
| created_by | From Number |
| direction | Inbound/Outbound |
| event_mode | Event Mode |
| media_url | Media URL |
| message_content | Message |
| message_type | Message Type |
| org_name | Org Name |
| route | Route |
| thread_id | Thread ID |
| user_id | User ID |
| From | From |
| To | To |
| phone_mobile | Clients Phone Number |
| created_at | Creation Time |
| thread_type | Thread Type |
| timestamp | Time Stamp |
| visible_to_channel | Visible to Channel |
| updated_at | Time of Updation |
| crm_id | CRM ID |
| status_timestamp | Status | Time Stamp |
| first_name | Clients Last Name |
| last_name | Clients First Name |
| thread_status | Status |
| crm_type | CRM Type |
| email | Email |
| alivesms_phone_number | Alive5 Channel Number |
| init_messageid |  |
| init_message_content | Message |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/LIVECHAT
## ***GET*** 

**Description:**  Output of all live chat conversations based on specific date range.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/conversations/livechat` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date_start | params | Start date | No | string |
| date_end | params | End date | No | string |
| page | params | a numeric value such as 1, designating the set of pages based on the limit value | Yes | string |
| limit | params | a numeric value such a 100, the number of results to return at once. | Yes | string |
| filter_by | params | Can filter by the name of the Channel (Ex: "general") | No | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| org_name | Org Name |
| alive5_sessionID | Alive5 Session ID |
| start_time | Start Time |
| end_time | End Time |
| channel_id | Channel ID |
| channel_name | Channel Name |
| crm_id | CRM ID |
| agent_id | User Agent ID |
| assigned_to | User Agent Name |
| contacts_first_name | Clients First Name |
| contacts_last_name | Clients Last Name |
| contacts_email | Clients Email |
| contacts_phone | Clients Phone Number |
| contacts_notes | Clients Notes |
| alive_sms_phone_number | Channel associated Phone Number |
| chat_conversation | Chat Conversations |
| created_at | Time of creation |
| created_by | Created By Client/User |
| message_content | Content of the Message |
| ip_address | IP Address |
| city | City |
| state | State |
| country | Country |
| zip | Zip |
| referrer_url | referrer URL |
| page_url | Page URL |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/FBM
## ***GET*** 

**Description:** Output all Facebook Messenger conversations based on specific date range.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/conversations/fbm` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date_start | params | Start date | No | string |
| date_end | params | End date | No | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| org_name | Org Name |
| alive5_sessionID | Alive5 Session ID |
| start_time | Start Time |
| end_time | End Time |
| channel_id | Channel ID |
| channel_name | Channel Name |
| crm_id | CRM ID |
| agent_id | Agent User ID |
| assigned_to | Agent UserName |
| contacts_first_name | Clients First Name |
| contacts_last_name | Clients Last Name |
| contacts_email | Clients Email |
| contacts_phone | Clients Phone Number |
| contacts_notes | Clients Notes |
| chat_conversation | Chat Conversations |
| created_at | Time of creation |
| created_by | Created By Client/User |
| message_content | Content of the Message |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CONVERSATIONS/SUMMARY
## ***GET*** 

**Description:** Output all Facebook Messenger conversations based on specific date range.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/conversations/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date_start | params | Start date | No | string |
| date_end | params | End date | No | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| visitors_web | total number of web threads that create and don’t create a contact. |
| visitors_fbm | total number of Facebook Messenger conversations that create and don’t create a contact. |
| visitors_sms | total number of SMS conversations. Since every convo includes a phone number, it will create a Contact. |
| contacts_web | total number of web conversations which have at least an email or phone number. |
| contacts_fbm | total number of facebook conversations which have at least an email or phone number. |
| contacts_sms |  same as “visitors_sms” |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/CHANNEL
## ***POST*** 

**Description:** Creates a channel in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/channel` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| channel_name | body | Channel Name | Yes | string |
| org_name | body | Org Name | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| agents | Agents Information |
| channel_id | Channel ID |
| channel_name | Channel name |
| channel_status | Channel Status |
| created_at | Time of creation |
| label | Channel Name |
| org_name | Org Name |
| system_generated |  |
| updated_at | Time of Updation |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/AGENT
## ***POST***  

**Description:** Creates an agent for the channel in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/agent` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | body | Email | Yes | string |
| screenname | body | Agent Name | Yes | string |
| org_name | body | Org Name | Yes | string |
| role | body | Role | Yes | string |
| channels | body | Channels | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| created_at | Time of creation |
| email | Email |
| org_name | Org Name |
| user_email | Email |
| user_id | Agent ID |
| user_status | Status |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/FAQ-CATEGORY
## ***POST***  

**Description:** Creates a new Faq Category in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/faq-category` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| title | body | Title of Category | Yes | string |
| channel | body | Channels | Yes | string |
| org_name | body | Org Name | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| category_id | Category ID |
| category_name | Category Name |
| channel_ids | Channel IDs |
| created_at | Time of Creation |
| label | Label |
| org_name | Org Name |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/FAQ-ARTICLE
## ***POST***  

**Description:** Creates a new Faq Article in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/faq-article` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| content | body | Content | Yes | string |
| category | body | Category | Yes | string |
| org_name | body | Org Name | Yes | string |
| title | body | Title | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| article_id | Article ID |
| body | Body |
| category_name | Category Name |
| created_at | Time of Creation |
| updated_at | Time of Updation |
| org_name | Org Name |
| title | Title |
| channel_ids | Channel IDs |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/TAG
## ***POST***  

**Description:** Creates a new Tag in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/tag` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | body | Email | Yes | string |
| org_name | body | Org Name | Yes | string |
| name | body | Name of Tag | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| created_at | Time of Creation |
| label | Label |
| org_name | Org Name |
| tag_id | Tag ID |
| tagname | Tag Name |
| email | Email |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/WIDGET
## ***POST***  

**Description:** Creates a new Widget in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/widget` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| widget_name | body | Widget Name | Yes | string |
| widget_type | body | Widget Type | Yes | string |
| botname | body | Name of Bot | Yes | string |
| accessChannels | body | Channels to access | Yes | string |
| channel_id | body | Channel ID | Yes | string |
| org_name | body | Org Name | Yes | string |
| shortCode | body | Short Code | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| accessChannels | Channels to access |
| access_type | Access Type |
| channel_id | Channel ID |
| wimg | Widget Image |
| wname | Widget Name |
| wscript | Widget Script |
| created_at | Time of Creation |
| id | ID |
| is_alive5_phone_number | Alive5 Phone Number |
| org_name | Org Name |
| qr_config |  |
| short_code | Short Code |
| sms_phone_number | Phone Number |
| website_url | Website URL |
| widget_auto_msg |  |
| widget_id | Widget ID |
| widget_name | Widget Name |
| botusername | Bot User Name |
| widget_type | Widget Type |
| window_settings | Window Settings |
| icon_url | Icon URL |
| banner_top_bg | Banner Top Background |
| banner_bottom_bg | Banner Bottom Background |
| banner_divider_bg | Banner Divider Background |
| logo_top_bg | Logo Top Background |
| logo_bottom_bg | Logo Bottom Background |
| logo_bg_pattern_type | Logo Background Pattern Type |
| chat_bg_pattern_type | Chat Background Pattern Type |
| footer_bg_pattern_type | Footer Background Pattern Type |
| footer_bg | Footer Background |
| footer_btn_border | Footer Button Border |
| footer_btn_font | Footer Button Font |
| footer_btn_bg | Footer Button Background |
| banner_font | Banner Font |
| chat_body_bg | Chat Body Background |
| agent_bubble_bg | Agent Bubble Background |
| agent_font | Agent Font |
| visitor_bubble_bg | Visitor Bubble Background |
| visitor_font | Visitor Font |
| header_m1 | Header Media1 |
| header_m2 | Header Media2 |
| banner_top_bg_sms | Banner Top Background SMS |
| banner_bottom_bg_sms | Banner Bottom Background SMS |
| banner_font_sms | Banner Font SMS |
| button_background_sms | Button Background SMS |
| button_font_sms | Button Font SMS |
| logo_bg_color_type | Logo Background Color Type |
| title_banner_bg_color_type | Title Banner Background Color Type |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/CREATE/BOTCHAIN
## ***POST***  

**Description:** Creates a new Botchain in Alive5 Account.

### HTTP Request 
`***POST*** https://api.alive5.com/public/1.0/create/botchain` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| widget_id | body | Widget ID | Yes | string |
| org_name | body | Org Name | Yes | string |
| channel_id | body | Channel ID | Yes | string |
| botchain_name | body | Botchain Name | Yes | string |
| bot_type | body | Bot Type | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| bot_type | Botchain Type |
| botchain_label | Botchain Label |
| botchain_name | Botchain Name |
| channel_ids | Channel IDs |
| org_name | Org Name |
| widget_ids | Widget IDs |
| botchain_id | Botchain ID |
| created_at | Time of Creation |

# HTTPS://API-V2.ALIVE5.COM/PUBLIC/1.0/CONTACT/CREATE-NEW
## ***POST***  

**Description:** Creates a new Contact in Alive5 Account.

### HTTP Request 
`***POST*** https://api-v2.alive5.com/public/1.0/contact/create-new` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| org_name | Parameters | Org Name | Yes | string |
| email | Parameters | Email | Yes | string |
| first_name | Parameters |  First Name | Yes | string |
| phone_mobile | Parameters | Phone Number | Yes | string |
| last_name | Parameters | Last Name | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| created_at | Time of Creation |
| crm_id | CRM ID |
| updated_at | Time of Updation |
| email | Email |
| first_name | First Name |
| last_name | Last Name |
| org_name | Org Name |
| phone_mobile | Phone Number |

# HTTPS://API-V2.ALIVE5.COM/PUBLIC/1.0/CONTACT/UPDATE-CONTACT
## ***PUT***  

**Description:** Updates a Contact in Alive5 Account.

### HTTP Request 
`***PUT*** https://api-v2.alive5.com/public/1.0/contact/update-contact` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| crm_id | Body | CRM ID | Yes | string |
| org_name | Body | Org Name | Yes | string |
| email | Body | Email | Yes | string |
| first_name | Body |  First Name | Yes | string |
| phone_mobile | Body | Phone Number | Yes | string |
| last_name | Body | Last Name | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| phone_mobile | Phone Number |
| updated_at | Time of Updation |
| email | Email |
| last_name | Last Name |
| first_name | First Name |
| message | Message |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/OBJECTS/CONTACT/GET-ALL
## ***GET***  

**Description:** Get all the Contacts of current Organization.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/objects/contact/get-all`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| page | params | a numeric value such as 1, designating the set of pages based on the limit value | Yes | string |
| limit | params | a numeric value such a 100, the number of results to return at once. | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| address | Address |
| billing_address | Address |
| billing_city | City |
| billing_country | Country |
| billing_state | State |
| billing_zip | Zip Code |
| city | City |
| company | Company |
| companytitle | Company Name |
| country | Country |
| created_at | Time of Creation |
| crm_id | CRM ID |
| email | Email |
| facebook | Facebook |
| first_name | First Name |
| last_name | Last Name |
| linkedin | Linkedin |
| instagram | Instagram |
| snapchat | Snapchat |
| whatsapp | WhatsApp |
| accountid | ACCOUNT ID |
| wechat | WeChat |
| viber | Viber |
| faq_question | faq_question |
| youtube | Youtube |
| notes | Notes |
| org_name | Org Name |
| phone_mobile | Phone Number |
| state | State |
| thread_id | THREAD ID |
| twitter | Twitter |
| updated_at | Time of Updation |
| xip | XIP |
| crm_type | CRM Type |
| last_interaction_at | Last Intteraction Time |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/GET-BOTS-REPORTING
## ***GET***  

**Description:** Get Bots Reporting.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/get-bots-reporting 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| from_datetime | params | From Date | Yes | string |
| to_datetime | params | To Date | Yes | string |
| botflowFilter | params | Bot Flow Filter | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| alivesms_phone_number | SMS Number |
| botchain_name | Botchain Name |
| bot_timestamp | Bot Timestamp |
| from_phone_number | Phone Number |
| org_name | Org Name |
| orgbot_name | Org Bot Name |
| orgbot_type | Org Bot Type |
| thread_id | Thread ID |
| init_messageid | Initial Message ID |
| init_message_content | initial Message Content |
| init_orgbot_name | Initial Org Bot Name |
| bot_message | Bot Message |
| user_reply | User Reply |
| keyword_found | Keyword Found |
| transaction_id | Transaction ID |
| report_id | Report ID |
| donaterequest_status | Donate Request Status |
| donate_amount | Donate Amount |
| question_type | Question Type |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/GET-FAQ-REPORTING
## ***GET***  

**Description:** Get FAQ Reporting.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/get-faq-reporting 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| from_datetime | params | From Date | Yes | string |
| to_datetime | params | To Date | Yes | string |
| botflowFilter | params | Bot Flow Filter | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| alivesms_phone_number | SMS Number |
| botchain_name | Botchain Name |
| bot_timestamp | Bot Timestamp |
| from_phone_number | Phone Number |
| org_name | Org Name |
| orgbot_name | Org Bot Name |
| orgbot_type | Org Bot Type |
| thread_id | Thread ID |
| init_messageid | Initial Message ID |
| init_message_content | initial Message Content |
| init_orgbot_name | Initial Org Bot Name |
| bot_message | Bot Message |
| user_reply | User Reply |
| keyword_found | Keyword Found |
| transaction_id | Transaction ID |
| report_id | Report ID |
| donaterequest_status | Donate Request Status |
| donate_amount | Donate Amount |
| question_type | Question Type |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/GET-MULTIPLEQUESTION-REPORTING
## ***GET***  

**Description:** Get Multi-Question Reporting.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/get-multiplequestion-reporting 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| from_datetime | params | From Date | Yes | string |
| to_datetime | params | To Date | Yes | string |
| botflowFilter | params | Bot Flow Filter | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| alivesms_phone_number | SMS Number |
| botchain_name | Botchain Name |
| bot_timestamp | Bot Timestamp |
| from_phone_number | Phone Number |
| org_name | Org Name |
| orgbot_name | Org Bot Name |
| orgbot_type | Org Bot Type |
| thread_id | Thread ID |
| init_messageid | Initial Message ID |
| init_message_content | initial Message Content |
| init_orgbot_name | Initial Org Bot Name |
| bot_message | Bot Message |
| user_reply | User Reply |
| keyword_found | Keyword Found |
| transaction_id | Transaction ID |
| report_id | Report ID |
| donaterequest_status | Donate Request Status |
| donate_amount | Donate Amount |
| question_type | Question Type |

# HTTPS://API.ALIVE5.COM/PUBLIC/1.0/GET-FREETEXT-REPORTING
## ***GET***  

**Description:** Get Free Text Reporting.

### HTTP Request 
`***GET*** https://api.alive5.com/public/1.0/get-freetext-reporting 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| from_datetime | params | From Date | Yes | string |
| to_datetime | params | To Date | Yes | string |
| botflowFilter | params | Bot Flow Filter | Yes | string |

**Responses**

| Value | Description |
| ---- | ----------- |
| alivesms_phone_number | SMS Number |
| botchain_name | Botchain Name |
| bot_timestamp | Bot Timestamp |
| from_phone_number | Phone Number |
| org_name | Org Name |
| orgbot_name | Org Bot Name |
| orgbot_type | Org Bot Type |
| thread_id | Thread ID |
| init_messageid | Initial Message ID |
| init_message_content | initial Message Content |
| init_orgbot_name | Initial Org Bot Name |
| bot_message | Bot Message |
| user_reply | User Reply |
| keyword_found | Keyword Found |
| transaction_id | Transaction ID |
| report_id | Report ID |
| donaterequest_status | Donate Request Status |
| donate_amount | Donate Amount |
| question_type | Question Type |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
