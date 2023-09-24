# PHP REST API

Initial codebase starter project: [https://code.tutsplus.com/how-to-build-a-simple-rest-api-in-php--cms-37000t](https://code.tutsplus.com/how-to-build-a-simple-rest-api-in-php--cms-37000t)

## Skeleton

```bash
├── Controller
│   └── Api
│       ├── BaseController.php
│       └── UserController.php
├── inc
│   ├── bootstrap.php
│   └── config.php
├── index.php
└── Model
    ├── Database.php
    └── UserModel.php
```

- `index.php`: the entry-point of our application. It will act as a front-controller of our application.
- `inc/config.php`: holds the configuration information of our application. Mainly, it will hold the database credentials.
- `inc/bootstrap.php`: used to bootstrap our application by including the necessary files.
-`Model/Database.php`: the database access layer which will be used to interact with the underlying MySQL database.
- `Model/UserModel.php`: the User model file which implements the necessary methods to interact with the users table in the MySQL database.
- `Controller/Api/BaseController.php`: a base controller file which holds common utility methods.
- `Controller/Api/UserController.php`: the User controller file which holds the necessary application code to entertain REST API calls.

## How to Call the REST API

Let's see how the URL of our endpoint looks:

`{BASE_URL}/{MODULE_NAME}/{METHOD_NAME}?limit={LIMIT_VALUE}`

### Modification

- Added the folder name to the base url (localhost/rest), which was `https://localhost/index.php`

    [http://localhost/rest/index.php/user/list?limit=20](http://localhost/rest/index.php/user/list?limit=20)
