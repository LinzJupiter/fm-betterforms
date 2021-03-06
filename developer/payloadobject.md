# Payload Object

## Overview

The `payload object` is the main 'package' of data and meta data that gets passed along the workflow. By mutating different areas of the `payload object` you can affect the users experience.

#### Things you can do:

* Redirect the user to different areas 
* Validate data
* Mutate data and inject data based on business logic
* add or hide form elements

Changing nearly any aspect of the `payload object` will immediately render that change to the user.

```
// $payload JSON
{
    "service": "serviceBeingCalled",
    "formSchema": {
        // see formChema  object    


    },
    "state"; {
        //state object (tab, userid etc)

    },
    "actions": 
    [
        {
            // array of actions to be performed when server is complete
        },
        {
            // another action
        }
    ]


}
```

Some services do not return all keys  the `payload object` .

## 

## _state_ Object

| Key | Description |
| :--- | :--- |
| subdomain | eg: mySite1 - contains the subdomain for the site being called. used for dispatching HookSet's etc. |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

## _actions_ Object \[array\]

Each action type has its own keys that are relevant to that action.

```
{
    "action":"showModal",
    "options":{
        "type": "someTypeOfModal"
        "body": "Text for th alert body"

    }

}
```

| Action Name | Description |
| :--- | :--- |
| actions | _modal, route, logout, _ |
| options { } | object of the various options relating to the action |
|  |  |
|  |  |









