1/30/23
    - Clean up initial git testing
    - Starting MongoDB MEAN tutorial (https://www.mongodb.com/languages/mean-stack-tutorial)
    - Made MongoDB atlas account
    - Install Homebrew, Atlas CLI, gcc
    - Updated apt-get
    xx issue using Atlas Cli - bash: /home/linuxbrew/.linuxbrew/bin/atlas: Bad address

1/31/23
    - Apparently homebrew install was not permanent ?
        Need to figure out how to make installations permanent?
        > If I open Ubuntu it works (alchemynte@LAPTOP-0SIH392K)
            * Brew works, atlas still does not work
        > If I open Ubuntu wSL, not (alchemynte@LAPTOP-0SIH392K)
    - Still having issues with atlas (Bad Address)
    * Might need to reconsider how I set up development environment

2/25/23
    - Set up Atlas using apt-get instead of brew -> works now
        > set up account and free cluster for practice
    - Set up basic server config and npm dependencies
    - set up connection to database via database.ts
    - initial run of server successful~
    - initial setup of CRUD methods success~ (employee.routes.ts)
    - initial setup of client in progress~
    
    Useful commands: 
        > git-dev/mean-test/client$ ng serve -o
        > git-dev/mean-test/server$ npx ts-node src/server.ts

2/26/23
    - Creating an employee service (Angular.js)
        > ng generate interface employee
        > ng generate service employee 
        > ng generate component employees-list
        >> app/employee.service.ts, app/employee.ts, app/employees-list/employees-list.component.ts 
        >> app/app-routing.module.ts, app/app.component.ts, app/app.module.ts, src/index.html
    - Creating a page for adding employees
        > ng generate component employee-form -m app
        > import ReactiveFormsModule -> app.module.ts
        > ng generate component add-employee -m app
        > ng generate component edit-employee -m app
        XX Error -- cannot POST to http://localhost:5200/employees (404 not found)
            >> fixed - forgot employee.post in employee.routes.ts 
