FORMAT: 1A
HOST: http://gateway.eigomonster.com/

# Eigomonster

These are the points that allow you to create and consume data on the Eigomonster API. Each endpoint will automatically determine if you have the required rights to execute the request. 
        
## Entity Collection [/entity]

An `entity` represents any role that wishes to create data on the system that could be used by any `user` on the system. `Entities` are similar to super users in that they can create global values for groups of `users`. Entities could be a school, university or similar institution who would want to customize the data that the `users` attributed to that `entity` would be influenced by.

### Add Entity [POST /entity/add/{id}]

+ Parameters
    + id: `2` (string) - page number to use

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
            {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": 00000AAEEDDDBB
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"Will contain list of error messages."}
            }
            
### Display Entity [GET /entity/{pagenumber}]

+ Parameters
    + pagenumber: `2` (string) - page number to use

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

            
### Search for Entity by ID [GET /entity/find/{id}]

+ Parameters
    + id: `2` (string) - page number to use

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Search for Entity by Name [GET /entity/find/name/{searchstring}]

+ Parameters
    + searchstring: `2` (string) - page number to use

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

             
### Add Contact to Entity [POST /entity/add/contact]

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List Contacts for Entity [GET /entity/list/contact/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Add Address to Entity [POST /entity/add/address{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List entity Addresses [GET /entity/list/address/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List entity Address by type [GET /entity/list/address/{entityid}/{type}]

+ Parameters
    + entityid: `oNNuwYphBWZmklPecZEbpPygk` (string) - id of the object that you would like to operate with
    + type: `billing` (string) - the type of address to find
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update entity Address [PUT /entity/update/address/{entityid}/{type}]

+ Parameters
    + entityid: `oNNuwYphBWZmklPecZEbpPygk` (string) - id of the object that you would like to operate with
    + type: `billing` (string) - the type of address to find

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

## Activity Collection [/activities]
### Add an Activity [POST /activity/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Update an Activity [PUT /activity/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List all Activities [GET /activity/list/{pagenumber}]

+ Parameters
    + pagenumber: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List a single Activity by ID [GET /activity/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
                
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Search for an Activity by name [GET /activity/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### Search for an Activity by type [GET /activity/find/{type}]

+ Parameters
    + type: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
### Search for an Activity by duration [GET /activity/find/{duration}]

+ Parameters
    + duration: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### Search for an Activity by level [GET /activity/find/{teachinglevel}]

+ Parameters
    + teachinglevel: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### Add Steps to an Activity [POST /activity/step/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Remove Steps from an Activity [PUT /activity/step/remove/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Removed",
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Step in an Activity [PUT /activity/step/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Search for a single Step by ID [GET /activity/step/search/singe/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List All Steps by Name [GET /activity/step/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page from which to return records
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### Add an Activity Type [POST /activity/types/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update and Activity Type [PUT /activity/types/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
### List a single Activity Type by ID [GET /activity/types/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find an Activity Type by Name [GET /activity/types/find/name/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Activity types [GET /activity/types/list/{pagenumber}]

+ Parameters
    + pagenumber: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Textbook Collection [/textbook]
### Add a Textbook [POST /textbook/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Textbook [PUT /textbook/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Textbook by ID [GET /textbook/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Textbook by Name [GET /textbook/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Textbooks  [GET /textbook/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Objective Collection [/objective]
### Add an Objective [POST /objective/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update an Objective [PUT /objective/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List a single Objective by ID [GET /objective/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find an Objective by Name [GET /objective/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Objectives [GET /objective/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
    
## Teaching Style Collection [/teachingstyle]
### Add a Teaching Style [POST /teachingstyle/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Teaching Style [PUT /teachingstyle/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a Teaching Style single by ID [GET /teachingstyle/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
    
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Teaching Style by Name  [GET /teachingstyle/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Teaching Styles [GET /teachingstyle/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Resources Collection [/resources]
### Add Kids Resources [POST /resources/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update Kids Resources [PUT /resources/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Kids Resource by ID [GET /resources/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Kids Resource by Name [GET /resources/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Kids Resources [GET /resources/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Teaching Ability Collection [/teachingability]
### Add a Teaching Ability [POST /teachingability/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Teaching Ability [PUT /teachingability/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Teaching Ability by ID [GET /teachingability/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Teaching Ability by Name [GET /teachingability/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Teaching Abilities [GET /teachingability/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Board of Education Collection [/boe]
### Add a Board of Education [POST /boe/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Board of Education [PUT /boe/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Board of Education by ID [GET /boe/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Board of Education by Name [GET /boe/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Boards of Education [GET /boe/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### Add a Board of Education Topic [POST /boe/topic/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Board of Education Topic [PUT /boe/topic/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Board of Education Topic by ID [GET /boe/topic/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Board of Education Topic by Name [GET /boe/topic/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Board of Education Topics [GET /boe/topic/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Curriculum Collection [/curriculum]
### Add a Curriculum [POST /add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Curriculum [PUT /curriculum/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Curriculum by ID [GET /curriculum/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
     
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Curriculum by Name [GET /curriculum/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Curricula [GET /curriculum/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Lesson Plan Collection [/lessonplan]
### Add a Lesson Plan [POST /lessonplan/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Lesson Plan [PUT /lessonplan/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Lesson Plan by ID [GET /lessonplan/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
     
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Lesson Plan by Name [GET /lessonplan/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Lesson Plans [GET /lessonplan/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
### Add Comments to a lesson plan [POST /lessonplan/comment/add/{planid}]

+ Parameters
    + planid: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update lesson plan Comments [PUT /lessonplan/comment/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single lesson plan Comment by ID [GET /lessonplan/comment/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find lesson plan Comment  by Name [GET /lessonplan/comment/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all lesson plan Comments for a given lesson plan [GET /lessonplan/comment/list/{planid}/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results
    + planid: `` (string) - id of the lesson plan we want to work with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Standard Section Collection [/standardsection]
### Add a Standard Section [POST /standardsection/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Standard Section [PUT /standardsection/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Standard Section by ID [GET /standardsection/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Standard Section by Name [GET /standardsection/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Standard Sections [GET /standardsection/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Material Files Collection [/materialfiles]
### Add files to Materials [POST /materialfiles/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update Material Files [PUT /materialfiles/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Material File by ID [GET /materialfiles/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Material File by Name [GET /materialfiles/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Material Files [GET /materialfiles/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Material Types Collection [/materialtypes]
### Add Material Types [POST /materialtypes/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update Material Types [PUT /materialtypes/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Material Type by ID [GET /materialtypes/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Material Type by Name [GET /materialtypes/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - the page number from which to return results
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all Material Types [GET /materialtypes/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Schedule Collection [/schedule]
### Add event to Schedule [POST /schedule/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update event in Schedule [PUT /schedule/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Schedule event  by ID [GET /schedule/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Schedule event by Name  [GET /schedule/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Schedule events  [GET /schedule/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }


## Grades Collection [/grades]
### Add Grade to School [POST /grades/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update Grade in a School [PUT /grades/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Grade by ID [GET /grades/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Grade by Name [GET /grades/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Grades [GET /grades/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
## Schools Collection [/school]
### Add a School [POST /school/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a School  [PUT /school/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single School by ID [GET /school/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a School by Name [GET /school/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Schools [GET /school/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### Add a Resource [POST /school/resource/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Resource [PUT  /school/resource/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Resource by ID [GET  /school/resource/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Resource by Name [GET  /school/resource/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all Resources [GET  /school/resource/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Ability Collection [/ability]
### Add an Ability [POST /ability/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update an Ability [PUT /ability/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Ability  by ID [GET /ability/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find an Ability  by Name [GET /ability/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Abilities  [GET /ability/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Country Collection [/country]
### Add a Country [POST /country/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Country [PUT /country/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Country by ID [GET /country/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Country  by Name [GET /country/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Countries [GET /country/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }


## Prefecture Collection [/prefecture]
### Add a Prefecture [POST /prefecture/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Prefecture [PUT /prefecture/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Prefecture by ID [GET /prefecture/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
       
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Prefecture by Name [GET /prefecture/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all Prefectures [GET /prefecture/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

## Level Collection [/level]
### Add a Level [POST /{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Level[PUT /level/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single Level by ID [GET /level/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Level by Name [GET /level/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Levels  [GET /level/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Schedule Color Collection [/schedulecolor]
### Add a Schedule Color [POST /schedulecolor/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Schedule Color [PUT /schedulecolor/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Schedule Color by ID [GET /schedulecolor/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Schedule Color by Name [GET /schedulecolor/find/{name}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all Schedule Colors [GET /schedulecolor/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
## System Limits Collection [/systemlimits]
### Add System Limits [POST /systemlimits/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update System Limits [PUT /systemlimits/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### List a single System Limit  by ID [GET /systemlimits/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a System Limit by Name [GET /systemlimits/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
### List all System Limits [GET /systemlimits/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Class Ability Collection [/classability]
### Add a Class Ability [POST /classability/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### Update a Class Ability [PUT /classability/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Class Ability by ID [GET /classability/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Class Ability  by Name [GET /classability/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all Class Abilities [GET /classability/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }
              
## Class Subject Collection [/subject]
### Add a Subject [POST /subject/add/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
### Update a Subject [PUT /subject/update/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace

    + Body
       
             {
                "VAR_NAME": "",
                "VAR_NAME": ""
            }
            
+ Response 201 (application/json)

            {
                "status" : "OK"
                "message": "Created",
                "objectToken": "00000AAEEDDDBB"
            }
            
+ Response 409 (application/json)

            {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }
            
### List a single Subject by ID [GET /subject/list/single/{id}]

+ Parameters
    + id: `EbpPygkoNNuwYphBWZmklPecZ` (string) - id of the object that you would like to operate with
    
+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace   
        
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data Found",
                "data": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data Found",
                "data": {}
            }
            
+ Response 409 (application/json)

             {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
                
            }

### Find a Subject by Name [GET /subject/find/{name}/{pagenumber}]

+ Parameters
    + name: `Fruits Basket` (string) - id of the object that you would like to operate with
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

### List all Subjects [GET /subject/list/{pagenumber}]

+ Parameters
    + pagenumber: `1` (int) - page number to return in the results

+ Request (application/json)

    + Headers
    
            x-Entity-Accesstoken: ent_replace
            Authorization: auth_replace
            
+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "Data found.",
                "records": {}
                "pageinfo": {}
            }

+ Response 200 (application/json)

            {
                "status" : "OK"
                "message": "No data found.",
                "data": {}
            }
            
+ Response 409 (application/json)

              {
                "status" : "ERROR"
                "message": "I was not able to process your request.",
                "data": {"//list of error messages.\\"
   
              }

