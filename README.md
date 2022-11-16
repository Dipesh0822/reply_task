### REPLY CRUD

#### Application Start and Install Description

1. Install Dependency using command line. 
    ```npm install```

2. Start Application using command line.
    ```npm start```

#### API Description

##### User API

1. <span style="color:blue">Insert</span>
    - http://localhost:8001/api/v1/users
    - POST
    - 
       ```
       {
            "email" : "test_01@gmail.com",
            "status" : "ACTIVE"
       }
       ```
    - email and status are mandatory. 
    - email is unique key    

2. <span style="color:blue">Update</span>
    - http://localhost:8001/api/v1/users/:id *
    - PUT
    - 
       ```
       {
            "email" : "test_01@gmail.com",
            "status" : "ACTIVE"
       }
       ```
    - email and status are mandatory.
    - email is unique key 
    ```* The is represents the existing user id.```

3. <span style="color:blue">Get</span>
    - http://localhost:8001/api/v1/users/:id *
    - GET
    ```* The is represents the existing user id.```

4. <span style="color:blue">Delete</span>
    - http://localhost:8001/api/v1/users/:id *
    - DELETE
    ```* The is represents the existing user id.```   

5. <span style="color:blue">Pagination</span>
    - http://localhost:8001/api/v1/users?page=1 **
    - GET
    ```* The is represents the existing page number.```



##### Report API

1. <span style="color:blue">Insert</span>
    - http://localhost:8001/api/v1/reports
    - POST
    - 
       ```
       {
            "short_title": "ACTIVE_USERS_1",
            "title": "All active users in country",
            "status": "ACTIVE",
            "paramaters": "country,since_when",
            "sql_string": "select id, email , created_at from users where status='ACTIVE' and country_code=%country and created_at>%since_when order by created_at desc"
       }
       ```
    - all field are mandatory. 
    - short_title is unique key     

2. <span style="color:blue">Update</span>
    - http://localhost:8001/api/v1/reports/:id *
    - PUT
    - 
       ```
       {
            "short_title": "ACTIVE_USERS_1",
            "title": "All active users in country",
            "status": "ACTIVE",
            "paramaters": "country,since_when",
            "sql_string": "select id, email , created_at from users where status='ACTIVE' and country_code=%country and created_at>%since_when order by created_at desc"
       }
       ```
    - all field are mandatory. 
    - short_title is unique key    
    ```* The is represents the existing report id.```

3. <span style="color:blue">Get</span>
    - http://localhost:8001/api/v1/reports/:id *
    - GET
    ```* The is represents the existing report id.```

4. <span style="color:blue">Delete</span>
    - http://localhost:8001/api/v1/reports/:id *
    - DELETE
    ```* The is represents the existing report id.```   

5. <span style="color:blue">Pagination</span>
    - http://localhost:8001/api/v1/reports?page=1 **
    - GET
    ```* The is represents the existing report number.```


##### Report Generate API

1. <span style="color:blue">Create</span>
    - http://localhost:8001/api/v1/reports
    - POST
    - 
      ```
      {
        "id": 1,
        "parameters": {
                "country": "IN",
                "since_when": "2020-01-01"
        },
        "limit": 100,
        "offset": 0
      }
      ```
    - all field are mandatory.

##### Ticket API

1. <span style="color:blue">Insert</span>
    - http://localhost:8001/api/v1/tickets
    - POST
    - 
       ```
        {
            "title" : "Ticket Most Work",
            "description" : "ACTIVE",
            "user_id": 1,
            "file_id": 1
        }
       ```
    - title, description and user_id are mandatory. 
    - file_id is optional    

2. <span style="color:blue">Update</span>
    - http://localhost:8001/api/v1/tickets/:id *
    - PUT
    - 
       ```
       {
            "title" : "Ticket Most Work",
            "description" : "ACTIVE",
            "user_id": 1,
            "file_id": 1
       }
       ```
    - title, description and user_id are mandatory. 
    - file_id is optional 
    ```* The is represents the existing ticket id.```

3. <span style="color:blue">Get</span>
    - http://localhost:8001/api/v1/tickets/:id *
    - GET
    ```* The is represents the existing ticket id.```

4. <span style="color:blue">Delete</span>
    - http://localhost:8001/api/v1/tickets/:id *
    - DELETE
    ```* The is represents the existing ticket id.```   

5. <span style="color:blue">Pagination</span>
    - http://localhost:8001/api/v1/tickets?page=1 **
    - GET
    ```* The is represents the existing page number.```


##### Reply API

1. <span style="color:blue">Insert</span>
    - http://localhost:8001/api/v1/replies
    - POST
    - 
       ```
        {
            "reply_text" : "this task is very often",
            "ticket_id" : 1,
            "user_id" : 1,
            "file_id" : 1
        }
       ```
    - reply_text, ticket_id and user_id are mandatory. 
    - file_id is optional    

2. <span style="color:blue">Update</span>
    - http://localhost:8001/api/v1/replies/:id *
    - PUT
    - 
       ```
        {
            "reply_text" : "this task is very often",
            "ticket_id" : 1,
            "user_id" : 1,
            "file_id" : 1
        }
       ```
    - reply_text, ticket_id and user_id are mandatory. 
    - file_id is optional 
    ```* The is represents the existing reply id.```

3. <span style="color:blue">Get</span>
    - http://localhost:8001/api/v1/replies/:id *
    - GET
    ```* The is represents the existing reply id.```

4. <span style="color:blue">Delete</span>
    - http://localhost:8001/api/v1/replies/:id *
    - DELETE
    ```* The is represents the existing reply id.```   

5. <span style="color:blue">Pagination</span>
    - http://localhost:8001/api/v1/replies?page=1 **
    - GET
    ```* The is represents the existing page number.```


##### Reply API

1. <span style="color:blue">Insert</span>
    - http://localhost:8001/api/v1/replies
    - POST
    - 
       ```
        {
            "group" : "this task is very often",
            "subgroup" : 1,
            "user_id" : 1,
            "file_id" : 1
        }
       ```
    - all field is required.  

2. <span style="color:blue">Get</span>
    - http://localhost:8001/api/v1/replies/:id *
    - GET
    ```* The is represents the existing file id.```

3. <span style="color:blue">Delete</span>
    - http://localhost:8001/api/v1/replies/:id *
    - DELETE
    ```* The is represents the existing file id.```   

4. <span style="color:blue">Pagination</span>
    - http://localhost:8001/api/v1/files?page=1 **
    - GET
    ```* The is represents the existing page number.```