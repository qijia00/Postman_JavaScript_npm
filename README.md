# JavaScript_Postman
Sample Postman scripts I created in JavaScript. Authentication information has been removed for privacy reasons.

## npm package for easy execution
Please follow README.md file inside each folder to install npm and execute. Newman execution examples (such as how to overwrite variables in cmd) are added to package.json. Since postman only support overwrite global variables in newman, so variables are separated into globalVariables.json and environment variables located in xx_env.json files. Global variables applies to all postman collections, and environment variables only apply to 1 collections which has the same name just without _env.

## regressionCascadeDelete.json
A complicated example to use postman.setNextRequest("") to create a tree that top node contains n 1st level children, each 1st level child contains n 2nd level children, and each 2nd level child contains n 3rd level children. This is a good example of how to use "Pre-request Script", and how to loop Postman http requests to work around its limitations (instead of loop, you have to use if else, see Tests in the POST requests).

## regressionDiagram.json
regressionDiagram.png displayed the architecture design of the regressionDiagram.json file, which created a sophisticated but not overwhelming test foundation of the building information management (BIM) config APIs. The structure of regressionDiagram.json are reused multiple times in other regression scripts.

## regressionFloor.json
Pre-request of POST EGF/SVG includes how to generate random guid. Also you can see how to randomly pick a node or relation from a return then use it in future calls (look for randomxXx in the http call's name).

## sanityResourceResources.json
In the Tests of "GET /v1/resources/{organizationId} ORGANIZATION", there is a for loop with embeded if else statements to handle random return orders (i.e., jpg may returned as the first element of the list or the second or the thrid or the last.).
