[comment]: # "Auto-generated SOAR connector documentation"
# Proofpoint SOAR App

Publisher: Splunk Community  
Connector Version: 1.0.1  
Product Vendor: Proofpoint  
Product Name: Proofpoint Threat Protection API  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 6.1.1.211  

Splunk SOAR app that integrates with the Proofpoint Threat Protection API. It leverage the strengths of Proofpoint's email protection to automate responses to threats and improve our overall security posture

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Proofpoint Threat Protection API asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base_url** |  required  | string | Company hostname for API execution
**client_id** |  required  | string | Client ID
**client_secret** |  required  | password | Client Secret

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[get safelist entries](#action-get-safelist-entries) - Get safe list entries  
[add to safelist](#action-add-to-safelist) - Add to safe list  
[delete from safelist](#action-delete-from-safelist) - Delete from safe list  
[get blocklist entries](#action-get-blocklist-entries) - Get block list entries  
[add to blocklist](#action-add-to-blocklist) - Add to block list  
[delete from blocklist](#action-delete-from-blocklist) - Delete from block list  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'get safelist entries'
Get safe list entries

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.data.\*.attribute | string |  |  
action_result.data.\*.operator | string |  |  
action_result.data.\*.value | string |  |  
action_result.data.\*.comment | string |  |  
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |  
action_result.status | string |  |    

## action: 'add to safelist'
Add to safe list

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 
**attribute** |  required  | Attribute | string | 
**operator** |  required  | Operator | string | 
**value** |  required  | Cluster ID | string | 
**comment** |  optional  | Comment | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |    

## action: 'delete from safelist'
Delete from safe list

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 
**attribute** |  required  | Attribute | string | 
**operator** |  required  | Operator | string | 
**value** |  required  | Cluster ID | string | 
**comment** |  optional  | Comment | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |    

## action: 'get blocklist entries'
Get block list entries

Type: **investigate**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.data.\*.attribute | string |  |  
action_result.data.\*.operator | string |  |  
action_result.data.\*.value | string |  |  
action_result.data.\*.comment | string |  |  
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |    

## action: 'add to blocklist'
Add to block list

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 
**attribute** |  required  | Attribute | string | 
**operator** |  required  | Operator | string | 
**value** |  required  | Cluster ID | string | 
**comment** |  optional  | Comment | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |    

## action: 'delete from blocklist'
Delete from block list

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | Cluster ID | string | 
**attribute** |  required  | Attribute | string | 
**operator** |  required  | Operator | string | 
**value** |  required  | Cluster ID | string | 
**comment** |  optional  | Comment | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.clusterid | string |  |  
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |  