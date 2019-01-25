# Description
Decode base64 to image and save the image to disk.

# base64-to-image

To install  
```sh
npm install base64-to-image --save
```

To run test  
```sh
npm test
```

### Usage  

Require the library in your .js file  
```js
const base64ToImage = require('base64-to-image');`  
```

#### Change base64 string to image and save it to disk  
```js
let base64Str = "Add valid base64 str";
let path = "put a valid path where you want to save the image";
let optionalObj = {fileName: "imageFileName", type: "png"};

base64ToImage(base64Str, path, optionalObj);

// Get Image Info
// Note base64ToImage function returns imageInfo which is an object with imageType and fileName.
let imageInfo = base64ToImage(base64Str, path, optionalObj); 
```


##### Parameters
- `base64Str` (string) - base64 string.
- `path` (string) - a valid path where you want to save the image.
- `optionalObj` (object) - have three properties fileName, type and debug
  - fileName holds image file name. If this value is not passed the image will be saved as 'img-' + Date.now().
  - type holds image type e.g. ('png' or 'jpg'  and so on). If this value is not passed it will extract the image type from the base64 if present ..if not the default is 'png'
  - debug properties helps to log error message, if added it enables logs.


### License  
  Anyone can contribute and use it 

### Issues  
Report a bug in the issues.   
