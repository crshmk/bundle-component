## Bundle React component with rollup

```bash
npm run build
```

creates `/dist/Component.min.js`


```bash
npm run dev
```

runs a watch

---


### Setup 

List peer dependencies in `package.json` and add them to the `external` prop in `rollup.config.js`

```javascript
{ 
  external: ['ramda', 'react']
}
```


Rename the output file in `rollup.config.js`
```javascript
{
  output: {
    file: './dist/FileUploader.min.js'
  }
}
```
and in `package.json`
```json
{
  "name": "file-uploader",
  "main": "./dist/FileUploader.min.js" 
}
```
