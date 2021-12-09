[comment]: # "Auto-generated SOAR connector documentation"
# Risk Fabric

Publisher: Bay Dynamics  
Connector Version: 1\.2\.3  
Product Vendor: Bay Dynamics  
Product Name: Risk Fabric  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.5\.210  

This app supports retrieving entity risk scores from Risk Fabric

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Risk Fabric asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**baseurl** |  required  | string | URL of the Risk Fabric instance
**verify\_server\_cert** |  required  | boolean | Verify Server Certificate
**username** |  required  | string | Username of the API user
**password** |  required  | password | Password of the API user

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[get user risk](#action-get-user-risk) - Action to retrieve the latest risk score for a user  
[get ip risk](#action-get-ip-risk) - Action to retrieve the latest risk score for an IP address  
[get host risk](#action-get-host-risk) - Action to retrieve the latest risk score for a host  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'get user risk'
Action to retrieve the latest risk score for a user

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**username** |  required  | Username | string |  `user name` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.username | string |  `user name` 
action\_result\.data\.\*\.entity\_name | string | 
action\_result\.data\.\*\.entity\_type | string | 
action\_result\.data\.\*\.risk\_rating | numeric | 
action\_result\.data\.\*\.risk\_score | numeric | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get ip risk'
Action to retrieve the latest risk score for an IP address

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip\_address** |  required  | IP address | string |  `ip`  `ipv6` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip\_address | string |  `ip`  `ipv6` 
action\_result\.data\.\*\.entity\_name | string | 
action\_result\.data\.\*\.entity\_type | string | 
action\_result\.data\.\*\.risk\_rating | numeric | 
action\_result\.data\.\*\.risk\_score | numeric | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get host risk'
Action to retrieve the latest risk score for a host

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**hostname** |  required  | Hostname | string |  `host name` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.hostname | string |  `host name` 
action\_result\.data\.\*\.entity\_name | string | 
action\_result\.data\.\*\.entity\_type | string | 
action\_result\.data\.\*\.risk\_rating | numeric | 
action\_result\.data\.\*\.risk\_score | numeric | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 