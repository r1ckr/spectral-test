# Spectral Test for issue [#1097](https://github.com/stoplightio/spectral/issues/1097)

## Running example:
lastIndexOf error:
```bash
$ spectral lint reference/petstore.yaml
Cannot read property 'lastIndexOf' of undefined
```

Skipping the error by adding brackets:
```bash
$ spectral lint [reference/petstore.yaml]
No results with a severity of 'error' or higher found!
```

But it's not linting properly, there's an issue in the `petstore.yaml` file line `13:20` since the OperationId is in 
snake_case and should be camelCase as specified in `.spectral.yml`