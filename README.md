# focus-service-generator
 Node package to generate code from a swagger interface 

## How to use 

 - Install as devDependencies `npm i --save-dev focus-service-generator`
 - Add a script line in your package json : `"service-generator": "better-npm-run service-generator"`
 - add a betterScript element in your package json 
 ```json
  "service-generator": {
            "command": "focus-service-generator",
            "env": {
                "TEMPLATE_FOLDER": "./node_modules/focus-service-generator/templates",
                "DEST_FOLDER": "./app/config/server/generated",
                "SWAGGER_SOURCE": "http://host/swagger/ur",
                "EOL": "\r\n"
            }
        },
 ``` 

## Environment variables

- `TEMPLATE_FOLDER` (default `'./node_modules/focus-service-generator/templates'`): Folder containing templates .dot, see http://olado.github.io/doT/
- `DEST_FOLDER` (default `'./app/config/server/generated'`): Destination folder for generated files
- `SWAGGER_SOURCE` (required): JSON of Swagger, either in file (`'file:./my/swagger/file.json'`) or by HTTP request (`http://host/swagger/url`)
- `EOL` (default `'\n'`): End of line in generated files

