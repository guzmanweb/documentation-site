{
  "title": "AlertConfigurationInputAverageTime",
  "description": "",
  "weight": 1,
  "fields": [
    {
      "typeString": "Int",
      "name": "historicalWindow",
      "url": "/travelgatex/reference/scalars/int",
      "description": "The timeframe in minutes",
      "args": null
    },
    {
      "typeString": "Int",
      "name": "offset",
      "url": "/travelgatex/reference/scalars/int",
      "description": "Time frame in minutes to set the beginning of historicalWindow",
      "args": null
    },
    {
      "typeString": "Int",
      "name": "max_average",
      "url": "/travelgatex/reference/scalars/int",
      "description": "maximum average time allowed in miliseconds",
      "args": null
    },
    {
      "typeString": "Int!",
      "name": "periodicity",
      "url": "/travelgatex/reference/scalars/int",
      "description": "Frequency of time in minutes in which the alert will be reviewed",
      "args": null
    },
    {
      "typeString": "Int!",
      "name": "window",
      "url": "/travelgatex/reference/scalars/int",
      "description": "The time frame in minutes",
      "args": null
    },
    {
      "typeString": "Int!",
      "name": "timesToAlert",
      "url": "/travelgatex/reference/scalars/int",
      "description": "The number of times the alert must be triggered in order to notify",
      "args": null
    },
    {
      "typeString": "Boolean!",
      "name": "noRecoveries",
      "url": "/travelgatex/reference/scalars/boolean",
      "description": "To allow recoveries notifications",
      "args": null
    },
    {
      "typeString": "Boolean!",
      "name": "stateChangesOnly",
      "url": "/travelgatex/reference/scalars/boolean",
      "description": "To allow notifications only if the status change",
      "args": null
    },
    {
      "typeString": "Int!",
      "name": "minNumberRequests",
      "url": "/travelgatex/reference/scalars/int",
      "description": "OPTION 1: defines the minimum number of requests must be in our historical Data before cheking the alert. \nOPTION 2: defines the minimum number of requests must be in the window time frame to check the alert.",
      "args": null
    },
    {
      "typeString": "Int!",
      "name": "percentageToAlert",
      "url": "/travelgatex/reference/scalars/int",
      "description": "Defines the minimum percentage to consider alert in status ALERTING.\nOPTION 1: Average time difference between window and historical window will be used to calculate the percentage and compared with the minimum percentage set.\nOPTION 2: Average time difference between window and max_average value field will be used to calculate the percetage and compared with the minimum percentage set.\nOPTION 3: Average time difference between Requests and max_average value field will be used to calculate the percetage and compared with the minimum percentage set.",
      "args": null
    },
    {
      "typeString": "[EmailInput]!",
      "name": "email",
      "url": "/travelgatex/reference/inputobjects/emailinput",
      "description": "Email addresses to send notifications",
      "args": null
    },
    {
      "typeString": "[HubStatusInput!]",
      "name": "hubStatus",
      "url": "/travelgatex/reference/inputobjects/hubstatusinput",
      "description": "Possibility to filter traffic by hubStatus",
      "args": null
    },
    {
      "typeString": "[ErrorCodeInput!]",
      "name": "errorCode",
      "url": "/travelgatex/reference/inputobjects/errorcodeinput",
      "description": "Possibility to filter traffic by errorCodes",
      "args": null
    },
    {
      "typeString": "[ErrorTypeInput!]",
      "name": "errorType",
      "url": "/travelgatex/reference/inputobjects/errortypeinput",
      "description": "Possibility to filter traffic by errorTypes",
      "args": null
    },
    {
      "typeString": "[AlertObjectInput!]",
      "name": "supplier",
      "url": "/travelgatex/reference/inputobjects/alertobjectinput",
      "description": "Possibility to filter traffic by suppliers (hub provider",
      "args": null
    },
    {
      "typeString": "[AlertObjectInput!]",
      "name": "client",
      "url": "/travelgatex/reference/inputobjects/alertobjectinput",
      "description": "Possibility to filter traffic by clients (hub user)",
      "args": null
    },
    {
      "typeString": "[AlertGroupInput!]",
      "name": "group",
      "url": "/travelgatex/reference/inputobjects/alertgroupinput",
      "description": "Must filter traffic by group. Only PRODUCT group type is allowed",
      "args": null
    },
    {
      "typeString": "[AlertObjectInput!]",
      "name": "access",
      "url": "/travelgatex/reference/inputobjects/alertobjectinput",
      "description": "Possibility to filter traffic by accesses",
      "args": null
    },
    {
      "typeString": "[AlertObjectInput!]",
      "name": "operation",
      "url": "/travelgatex/reference/inputobjects/alertobjectinput",
      "description": "Possibility to filter traffic by operations",
      "args": null
    },
    {
      "typeString": "[AlertGroups!]",
      "name": "groupBy",
      "url": "/travelgatex/reference/enums/alertgroups",
      "description": "Possibility to group by traffic and calculate its parameters separately ",
      "args": null
    }
  ],
  "requireby": [
    {
      "name": "AlertInput",
      "description": "Alert information. Only one configuration has to be set at once.",
      "url": "/travelgatex/reference/inputobjects/alertinput"
    }
  ],
  "enumValues": null,
  "operator": "type",
  "typename": "AlertConfigurationInputAverageTime",
  "hideGithubLink": true
}
Configuration for AVERAGE_TIME. 
Average time is used to verify requests times.
There are 3 options:
- OPTION 1: Can verify average time traffic of a time frame and compare it with an other time frame. (window and historical window) Must set field window and historical windows higher than 0.
- OPTION 2: Can verify average time traffic of a time frame and compare it with the value max_average. Must set window higher than 0.
- OPTION 3: Can verify average time traffic of a specific number of requests and compare it with the value max_average. Must set window as 0 and minNumRequests higher than 0.
## GraphQL schema definition

{{% graphql-schema-type %}}

## Fields

{{% graphql-field %}}

## Required by

{{% graphql-require-by %}}
