# image-to-text

* Simple object detection module. Reads Text/Numbers/Characters/Bar codes too.

* Finds the object in an given image file and gives back the text description of it. (Uses api over internet)

* Promise enabled.

#### Usage:
```javascript
 var imageToTextDecoder = require('image-to-text');

 var file = {
   name: 'iphone.jpeg',
   path: './image/'
 };

 imageToTextDecoder.getKeywordsForImage(file).then(function(keywords){
    console.log(keywords);
 });
```

##### output
> space gray iphone 6

##### input file - ./image/iphone.jpeg

![iphone 6 image](http://goo.gl/TEQAbN)

#### File specifications

* File can we object with name and path mentioned
```javascript
 var file = {
  name: 'iphone.jpeg',
  path: './image/'
};
```

* Object with just name. Then path will be treated as root
```javascript
var file = {
  name: 'iphone.jpeg'
};
````

* Object with name, path and content. Content - buffer of the file
```javascript
fs.readFile('./iphone.jpeg', function(err, content){

    var file = {
        name: 'iphone.jpeg',
        path: './',
        content: content
    }
}
```
          

* String - just name of the file. Path will be treated as root.
```javascript
var file = 'iphone.jpeg';
```

