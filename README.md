# bruno 

## What is Bruno?   
Bruno is a Git-friendly and offline-first open-source API client aimed at revolutionizing the status quo represented by tools like Postman and Insomnia.

```bash
npm i -g openapi-to-postmanv2
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


## [Bruno CLI](https://docs.usebruno.com/bru-cli/overview)  

1. Execute API Requests & Collections: Run individual API requests or entire collections directly from the command line.
2. Generate Test Reports : Easily create reports in multiple formats, including JSON, JUnit, and HTML, to analyze and share test results.
3. CI/CD Integration: Effortlessly integrate with CI/CD pipelines for automated testing and validation.


```bash
npm install -g @usebruno/cli
```

```bash
bru run --reporter-html results.html
```


## [bru-lang](https://docs.usebruno.com/bru-lang/overview)  


## [converters](https://docs.usebruno.com/converters/overview)


## [postman-to-bruno](https://docs.usebruno.com/converters/postman-to-bruno)
```javascript
const { postmanToBruno } = require('@usebruno/converters');
const { readFile, writeFile } = require('fs/promises');
 
async function convertPostmanToBruno(inputFile, outputFile) {
  try {
    const inputData = await readFile(inputFile, 'utf8');
    const brunoCollection = postmanToBruno(JSON.parse(inputData));
    await writeFile(outputFile, JSON.stringify(brunoCollection, null, 2));
    console.log('Conversion successful!');
  } catch (error) {
    console.error('Error during conversion:', error);
  }
}
 
// Usage example
convertPostmanToBruno('path/to/postman-collection.json', 'path/to/bruno-collection.json');
```
## [insomnia-to-bruno](https://docs.usebruno.com/converters/insomnia-to-bruno)
```javascript
const { insomniaToBruno } = require('@usebruno/converters');
const { readFile, writeFile } = require('fs/promises');
 
async function convertInsomniaToBruno(inputFile, outputFile) {
  try {
    const inputData = await readFile(inputFile, 'utf8');
    const brunoCollection = insomniaToBruno(JSON.parse(inputData));
    await writeFile(outputFile, JSON.stringify(brunoCollection, null, 2));
    console.log('Insomnia conversion successful!');
  } catch (error) {
    console.error('Error during Insomnia conversion:', error);
  }
}
 
 
convertInsomniaToBruno('path/to/insomnia-collection.json', 'path/to/bruno-collection.json');
```
## [openapi-to-bruno](https://docs.usebruno.com/converters/openapi-to-bruno)    

```javascript
const { openApiToBruno } = require('@usebruno/converters');
const { readFile, writeFile } = require('fs/promises');
 
async function convertOpenApiToBruno(inputFile, outputFile) {
  try {
    
    const jsonContent = await readFile(inputFile, 'utf8');
    
    const openApiSpec = JSON.parse(jsonContent);
    
    const brunoCollection = openApiToBruno(openApiSpec);
    
    await writeFile(outputFile, JSON.stringify(brunoCollection, null, 2));
    console.log('OpenAPI JSON conversion successful!');
  } catch (error) {
    console.error('Error during OpenAPI JSON conversion:', error);
  }
}
 
 
convertOpenApiToBruno('path/to/openapi-spec.json', 'path/to/bruno-collection.json');
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

```
openapi2postmanv2 -s spec.yaml -o collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
```




## references   
|     |     |
| --- | --- |
|     |     |
|     |     |
|     |     |