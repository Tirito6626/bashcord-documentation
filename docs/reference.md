# Reference 
Firstly, bashcord uses Discord REST API v10 and Discord websocket
* https://discord.com/api/v10
* wss://gateway.discord.gg

Secondly, every bashcord function represents Discord REST API function, so you can always check Discord API documentation for functions
* https://discord.com/developers/docs/

Bashcord has:

* Functions
* Builders
* Events 
* Data variables

## Functions 
Functions are used to communicate with Discord REST API using GET, PATCH, PUT and DELETE methods

Every function has this structure:
```bash
category # category, guild for example
        _subcategory # subcategory, ban for example
                    _method # method, delete for example
```

To use function, you need:
```bash
function "argument 1" "argument 2" "argument 3" ... 
```
Argument can be anything, string, int, number, variable and etc...

## Builders
Builders are functions which help with building correct JSON Object, Embed for example

```bash
addFunction # addField for example
```

To use builder, you need:
```bash
addFunction "argument 1" "argument 2" "argument 3" ...
```
Argument can be anything, string, int, number, variable and etc...


## Events
Events are used to execute function/command on action

To use event, you need:

```bash
function hello {
   ... # function code
}
onFunction hello # onMessage for example
#           ^^^ function name
```

Every event saves its data into data variables


## Data variables
Data variables are used to keep data inside, which can be used later

```bash
$data_onMessageCreate
``` 
Here is an example of data variable
Every event saves its data into data variables, `data_on(event name with capital letter, $data_onInteractionCreate for example)`
Every variable keeps object of event, so you can use it on your own

* $message_json
* $client_json
* $slash_json
These 3 variables represent message object, client object and application command object
You can use them inside commands functions and etc

## Tips
* Use `jq` to manage JSON objects and arrays
* Use `grep` to return data from pattern
* Use `awk` to split data into arguments