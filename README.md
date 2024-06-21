# Proofpoint SOAR App

Publisher: Splunk  
Connector Version: 1\.0\.0  
Product Vendor: Proofpoint  
Product Name: Proofpoint  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 6\.1\.1  

Splunk SOAR app that integrates with the Proofpoint Threat Protection API. It leverage the strengths of Proofpoint's email protection to automate responses to threats and improve our overall security posture. According to short time expiration of token, all action are generating new one during execution.

[comment]: # " File: README.md"
[comment]: # "  Copyright (c) 2019-2023 Splunk Inc."
[comment]: # ""
[comment]: # "Licensed under the Apache License, Version 2.0 (the 'License');"
[comment]: # "you may not use this file except in compliance with the License."
[comment]: # "You may obtain a copy of the License at"
[comment]: # ""
[comment]: # "    http://www.apache.org/licenses/LICENSE-2.0"
[comment]: # ""
[comment]: # "Unless required by applicable law or agreed to in writing, software distributed under"
[comment]: # "the License is distributed on an 'AS IS' BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,"
[comment]: # "either express or implied. See the License for the specific language governing permissions"
[comment]: # "and limitations under the License."
[comment]: # ""

## Asset Configuration

To start working with such SOAR connector user need to collect **Client ID**, **CLient Secret** and of course Company **base url** for API execution.

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a EC2 asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**Base Url** |  required  | string | Company hostname for API execution
**Client ID** |  required  | string | Client ID
**Client Secret** |  required  | password | Client Secret

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using token generation  
[get safe list entries](#action-get-safe-list-entries) - Get safe list entries by API endpoint  
[add to safe list](#action-add-to-safe-list) - Add to safe list by API endpoint  
[delete from safe list](#action-delete-from-safe-list) - Delete from safe list by API endpoint  
[get block list entries](#action-get-block-list-entries) - Get block list entries by API endpoint  
[add to block list](#action-add-to-block-list) - Add to block list by API endpoint  
[delete from block list](#action-delete-from-block-list) - Delete from block list by API endpoint

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'get safe list entries'
Get safe list entries by API endpoint

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.data\.\*\.attribute | string | 
action\_result\.data\.\*\.operator | numeric | 
action\_result\.data\.\*\.value | string | 
action\_result\.data\.\*\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'add to safe list'
Add to safe list by API endpoint

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 
**attribute** |  required  |  | string | 
**operator** |  required  |  | string | 
**value** |  required  |  | boolean | 
**comment** |  optional  | A short comment about the entry | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.parameter\.attribute | string | 
action\_result\.parameter\.operator | string | 
action\_result\.parameter\.value | boolean | 
action\_result\.parameter\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'delete from safe list'
Delete from safe list by API endpoint

Type: **generic**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 
**attribute** |  required  |  | string | 
**operator** |  required  |  | string | 
**value** |  required  |  | boolean | 
**comment** |  optional  | A short comment about the entry | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.parameter\.attribute | string | 
action\_result\.parameter\.operator | string | 
action\_result\.parameter\.value | boolean | 
action\_result\.parameter\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get block list entries'
Get block list entries by API endpoint

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.data\.\*\.attribute | string | 
action\_result\.data\.\*\.operator | numeric | 
action\_result\.data\.\*\.value | string | 
action\_result\.data\.\*\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'add to block list'
Add to block list by API endpoint

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 
**attribute** |  required  |  | string | 
**operator** |  required  |  | string | 
**value** |  required  |  | boolean | 
**comment** |  optional  | A short comment about the entry | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.parameter\.attribute | string | 
action\_result\.parameter\.operator | string | 
action\_result\.parameter\.value | boolean | 
action\_result\.parameter\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'delete from block list'
Delete from block list by API endpoint

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**clusterid** |  required  | PPS Cluster ID | string | 
**attribute** |  required  |  | string | 
**operator** |  required  |  | string | 
**value** |  required  |  | boolean | 
**comment** |  optional  | A short comment about the entry | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.clusterid | string | 
action\_result\.parameter\.attribute | string | 
action\_result\.parameter\.operator | string | 
action\_result\.parameter\.value | boolean | 
action\_result\.parameter\.comment | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   