# postman   


## openapi-to-postman   
```bash
npm i -g openapi-to-postmanv2
```



```
openapi2postmanv2 --help
Usage: openapi2postmanv2 [options]

Options:
  -v, --version                               output the version number
  -s, --spec <spec>                           Convert given OPENAPI 3.0.0 spec to Postman Collection v2.0
  -o, --output <output>                       Write the collection to an output file
  -t, --test                                  Test the OPENAPI converter
  -p, --pretty                                Pretty print the JSON file
  -i, --interface-version <interfaceVersion>  Interface version of convert() to be used
  -c, --options-config <optionsConfig>        JSON file containing Converter options
  -O, --options <options>                     comma separated list of options
  -h, --help                                  output usage information
    Converts a given OPENAPI specification to POSTMAN Collections v2.1.0
```

```bash
openapi2postmanv2 -s account-info-openapi.yaml -o account-info-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
openapi2postmanv2 -s confirmation-funds-openapi.yaml -o confirmation-funds-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
openapi2postmanv2 -s event-notifications-openapi.yaml -o event-notifications-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
openapi2postmanv2 -s events-openapi.yaml -o events-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
openapi2postmanv2 -s payment-initiation-openapi.yaml -o payment-initiation-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
openapi2postmanv2 -s vrp-openapi.yaml -o vrp-collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
```



```
Input file:  /home/rock/workspace/github/bruno/obie/v4.0.0/payment-initiation-openapi.yaml
Writing to file:  true /home/rock/workspace/github/bruno/obie/v4.0.0/payment-initiation-collection.json {
  result: true,
  output: [ { type: 'collection', data: [Object] } ],
  analytics: {}
}
Conversion successful, collection written to file
```


## [import-collections](https://docs.usebruno.com/get-started/import-export-data/import-collections)

Whatever the case, you can import the following formats as Bruno Collections:

- Bruno Collection (if a Collection is manually shared with you)
- Postman Collection
- Postman Data Export
- Insomnia Collection
- Cloning a Git Repository
- OpenAPI V3 file
- OpenAPI V3 URL

## [postman-migration](https://docs.usebruno.com/get-started/import-export-data/postman-migration)


## [script-translator](https://docs.usebruno.com/get-started/import-export-data/script-translator)
