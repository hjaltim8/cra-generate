# React Component Generator

Scaffold a React component for Create React App.

```bash
Usage: cra-generate [options] <component>

Options:
  -h, --help                       output usage information
  -V, --version                    output the version number
  -f, --functional                 create a functional component
  -t, --type-check [system]        add @flow comment to script files
  -c, --css-extension [extension]  changes the extension of generated css files
  -d, --directory [dir]            specify a directory for the component
      --test [type]                either "jest" or "none"
      --no-semi                    remove semicolons
```

If a `.flowconfig` is present, a `// @flow` comment is prepended to all script files.

Project specific settings can be added to the `package.json` file under the `craGenerate` key. Eg

```json
"craGenerate": {
  "fileFormat": "paramCase",
  "cssExtension": "scss",
  "directory": "widgets"
}
```

| option          | type    | default     | description                                                                      |
|-----------------|---------|-------------|----------------------------------------------------------------------------------|
| directory       | `string`  | "components"  | Where, relative to the `./src/` directory, the component should be.                          |
| fileFormat      | `string`  | "pascalCase"  | One of: camelCase, constantCase, headerCase, paramCase, pascalCase or snakeCase. |
| componentFormat | `string`  | "pascalCase"  | One of: camelCase, constantCase, headerCase, paramCase, pascalCase or snakeCase. |
| typeCheck       | `undefined` &#124; `string` | `undefined` | Can be set explicitly to "flow".                                                 |
| cssExtension    | `string`  | "css"         | File extensions, with or without a dot.                                      |
| semi    | `true` &#124; `false`  | `true`         | Should script files be terminated with a semicolon.                                      |
| test            | `false` &#124; `string` | "jest"   | Only jest for now. Can be skipped with false.                                  |

## License

MIT
