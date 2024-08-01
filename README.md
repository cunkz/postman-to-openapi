## Installation

Using `npm`:

```bash
npm i postman-ke-openapi
```

Using `yarn`:

```bash
yarn add postman-ke-openapi
```

To install as a `cli` just

```bash
npm i postman-ke-openapi -g
```

## Quick Usage

As a library

```js
// Require Package
const postmanToOpenApi = require('postman-ke-openapi')

// Postman Collection Path
const postmanCollection = './path/to/postman/collection.json'
// Output OpenAPI Path
const outputFile = './api/collection.yml'

// Async/await
try {
    const result = await postmanToOpenApi(postmanCollection, outputFile, { defaultTag: 'General' })
    // Without save the result in a file
    const result2 = await postmanToOpenApi(postmanCollection, null, { defaultTag: 'General' })
    console.log(`OpenAPI specs: ${result}`)
} catch (err) {
    console.log(err)
}

// Promise callback style
postmanToOpenApi(postmanCollection, outputFile, { defaultTag: 'General' })
    .then(result => {
        console.log(`OpenAPI specs: ${result}`)
    })
    .catch(err => {
        console.log(err)
    })
```

As a cli

```bash
p2o ./path/to/PostmantoCollection.json -f ./path/to/result.yml -o ./path/to/options.json
```

## Cli Demo

![cli demo gif](./docs/assets/img/demo.gif)

## Documentation

All features, usage instructions and help can be found in the [Documentation page](https://joolfe.github.io/postman-to-openapi/)

## Credits

All credits goes to [joolfe](https://github.com/joolfe). I re-publish this package because my PR didnt get any response.

## Tags

`Nodejs` `Javascript` `OpenAPI` `Postman` `Newman` `Collection` `Transform` `Convert`

## License

See the [LICENSE](LICENSE.txt) file.
