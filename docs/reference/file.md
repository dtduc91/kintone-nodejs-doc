# File

Download and upload file via kintone Rest API

## Constructor

**Parameter**

| Name| Type| Required| Description |
| --- | --- | --- | --- |
| connection | [Connection](./connection) | yes | The kintone connection module

**Sample code**

<details class="tab-container" open>
<Summary>Init File module</Summary>

** Source code **

```javascript

const kintone = 'kintone-nodejs-sdk';

let kintoneFile = kintone.File(connection);
```

</details>

## Methods

### upload(filePath)

**Parameter**

| Name| Type| Required| Description |
| --- | --- | --- | --- |
| filePath | String | yes | The full path of file on your enviroment

**Return**

Promise

**Sample code**

<details class="tab-container" open>
<Summary>Upload file</Summary>

** Source code **

```javascript
let fullPathFile = '{your/file/with/full/path}';
kintoneFile.upload(fullPathFile);
```

** Respone **

```javascript
{
    fileKey: "kintone_file_key"
}
```

</details>

### download(fileKey, outPutFilePath)

**Parameter**

| Name| Type| Required| Description |
| --- | --- | --- | --- |
| filePath | String | yes | The full path of file on your enviroment
| outPutFilePath | String | yes | The full path of output file on your enviroment

**Return**

Promise

**Sample code**

<details class="tab-container" open>
<Summary>Download file</Summary>

** Source code **

```javascript
let fileKey = '/*your_file_key*/';
let fullPathFileOuput = '{your/folder/with/full/path}';
kintoneFile.download(fullPathFolder, fullPathFileOuput);
```

** Respone **

```javascript
{
    fileKey: "kintone_file_key"
}
```

</details>