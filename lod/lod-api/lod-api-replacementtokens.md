# ReplacementTokens

The **ReplacementTokens** command retrieves all @lab replacement tokens available for a particular lab instance.

## Parameters

|Name|Type|Required|Note|
|--- |--- |--- |--- |
| Id | Integer (64-bit) | No | The ID of the lab instance|

## Response

|Property|Type|Nullable|Note
|--- |--- |--- |--- |
|ReplacementTokens|Array of ReplacementTokens|No|See the ReplacementTokens Type below|

## ReplacementTokens

|Property|Type|Nullable|Note
|--- |--- |--- |--- |
|Token|String|No|The token name|
|Replacement|String|No|The replacement value for the token|

## Example Usage

```
https://labondemand.com/api/v3/replacementtokens/38922211
```

## Example Response

Please note that the actual replacement tokens returned will vary by lab type. For instance, virtualization labs will have several VirtualMachine tokens, while Cloud Slice labs will have several CloudResource tokens.

```linenums
{
    "ReplacementTokens": [
        {
            "Token": "@lab.VirtualMachine(machine1).Username",
            "Replacement": "user1"
        },
        {
            "Token": "@lab.VirtualMachine(machine1).Password",
            "Replacement": "h&4Fa?)C3/eQ;)?E"
        },
        {
            "Token": "@lab.VirtualMachine(machine2).Username",
            "Replacement": "user1"
        },
        {
            "Token": "@lab.VirtualMachine(machine2).Password",
            "Replacement": "LXM(#(Z^Hw4Upp>f"
        },
        {
            "Token": "@lab.LabInstance.Id",
            "Replacement": "15167595"
        },
        {
            "Token": "@lab.LabInstance.GlobalId",
            "Replacement": "lod15167595"
        },
        {
            "Token": "@lab.LabInstance.StartDate",
            "Replacement": "20190809"
        },
        {
            "Token": "@lab.LabProfile.Id",
            "Replacement": "1581178"
        },
        {
            "Token": "@lab.User.Id",
            "Replacement": "13832814"
        },
        {
            "Token": "@lab.User.FirstName",
            "Replacement": "Lab "
        },
        {
            "Token": "@lab.User.LastName",
            "Replacement": "User"
        },
        {
            "Token": "@lab.User.Email",
            "Replacement": "lab.user@sample.net"
        }
    ],
    "Error": null,
    "Status": 1
}
```