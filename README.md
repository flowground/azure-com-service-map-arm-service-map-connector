# ![LOGO](logo.png) Service Map **flow**ground Connector

## Description

A generated **flow**ground connector for the Service Map API (version 2015-11-01-preview).

Generated from: https://api.apis.guru/v2/specs/azure.com/service-map-arm-service-map/2015-11-01-preview/swagger.json<br/>
Generated at: 2019-05-07T17:38:57+03:00

## API Description

Service Map API Reference

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Retrieves the specified client group

*Tags:* `Client Groups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `clientGroupName` - _required_ - Client Group resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns the members of the client group during the specified time interval.

*Tags:* `Client Groups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `clientGroupName` - _required_ - Client Group resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow
* `$top` - _optional_ - Page size to use. When not specified, the default page size is 100 records.

### Returns the approximate number of members in the client group.

*Tags:* `Client Groups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `clientGroupName` - _required_ - Client Group resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Generates the specified map.

*Tags:* `Maps`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.

### Returns all machine groups during the specified time interval.

*Tags:* `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Creates a new machine group.

*Tags:* `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.

### Deletes the specified Machine Group.

*Tags:* `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineGroupName` - _required_ - Machine Group resource name.

### Returns the specified machine group as it existed during the specified time interval.

*Tags:* `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineGroupName` - _required_ - Machine Group resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Updates a machine group.

*Tags:* `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineGroupName` - _required_ - Machine Group resource name.

### Returns a collection of machines matching the specified conditions.  The returned collection represents either machines that are active/live during the specified interval  of time (`live=true` and `startTime`/`endTime` are specified) or that are known to have existed at or  some time prior to the specified point in time (`live=false` and `timestamp` is specified).

*Tags:* `Machines`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `live` - _optional_ - Specifies whether to return live resources (true) or inventory resources (false). Defaults to **true**. When retrieving live resources, the start time (`startTime`) and end time (`endTime`) of the desired interval should be included. When retrieving inventory resources, an optional timestamp (`timestamp`) parameter can be specified to return the version of each resource closest (not-after) that timestamp.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow
* `timestamp` - _optional_ - UTC date and time specifying a time instance relative to which to evaluate each machine resource. Only applies when `live=false`. When not specified, the service uses DateTime.UtcNow.
* `$top` - _optional_ - Page size to use. When not specified, the default page size is 100 records.

### Returns the specified machine.

*Tags:* `Machines`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `timestamp` - _optional_ - UTC date and time specifying a time instance relative to which to evaluate the machine resource. When not specified, the service uses DateTime.UtcNow.

### Returns a collection of connections terminating or originating at the specified machine

*Tags:* `Machines`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Obtains the liveness status of the machine during the specified time interval.

*Tags:* `Machines`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of machine groups this machine belongs to during the specified time interval.

*Tags:* `Machines` `MachineGroups`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of live ports on the specified machine during the specified time interval.

*Tags:* `Machines` `Ports`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns the specified port. The port must be live during the specified time interval. If the port is not live during the interval, status 404 (Not Found) is returned.

*Tags:* `Ports`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `portName` - _required_ - Port resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of processes accepting on the specified port

*Tags:* `Ports` `Processes`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `portName` - _required_ - Port resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of connections established via the specified port.

*Tags:* `Ports`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `portName` - _required_ - Port resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Obtains the liveness status of the port during the specified time interval.

*Tags:* `Ports`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `portName` - _required_ - Port resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of processes on the specified machine matching the specified conditions. The returned collection represents either processes that are active/live during the specified interval  of time (`live=true` and `startTime`/`endTime` are specified) or that are known to have existed at or  some time prior to the specified point in time (`live=false` and `timestamp` is specified).

*Tags:* `Processes` `Machines`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `live` - _optional_ - Specifies whether to return live resources (true) or inventory resources (false). Defaults to **true**. When retrieving live resources, the start time (`startTime`) and end time (`endTime`) of the desired interval should be included. When retrieving inventory resources, an optional timestamp (`timestamp`) parameter can be specified to return the version of each resource closest (not-after) that timestamp.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow
* `timestamp` - _optional_ - UTC date and time specifying a time instance relative to which to evaluate all process resource. Only applies when `live=false`. When not specified, the service uses DateTime.UtcNow.

### Returns the specified process.

*Tags:* `Processes`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `processName` - _required_ - Process resource name.
* `timestamp` - _optional_ - UTC date and time specifying a time instance relative to which to evaluate a resource. When not specified, the service uses DateTime.UtcNow.

### Returns a collection of ports on which this process is accepting

*Tags:* `Processes`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `processName` - _required_ - Process resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns a collection of connections terminating or originating at the specified process

*Tags:* `Processes`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `processName` - _required_ - Process resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Obtains the liveness status of the process during the specified time interval.

*Tags:* `Processes`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `machineName` - _required_ - Machine resource name.
* `processName` - _required_ - Process resource name.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

### Returns summary information about the machines in the workspace.

*Tags:* `Summaries`

#### Input Parameters
* `subscriptionId` - _required_ - Azure subscription identifier.
* `resourceGroupName` - _required_ - Resource group name within the specified subscriptionId.
* `workspaceName` - _required_ - OMS workspace containing the resources of interest.
* `api-version` - _required_ - API version.
* `startTime` - _optional_ - UTC date and time specifying the start time of an interval. When not specified the service uses DateTime.UtcNow - 10m
* `endTime` - _optional_ - UTC date and time specifying the end time of an interval. When not specified the service uses DateTime.UtcNow

## License

**flow**ground :- Telekom iPaaS / azure-com-service-map-arm-service-map-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
