# ng-haversine

**ng-haversine** is an AngularJS module that applies the Haversine formula to a pair of coordinates to calculate the distance between them.

## How to

The first step is to download the **ng-haversine** script. You can do it cloning this repo:
```bash
$ git clone https://github.com/vermicida/ng-haversine.git
```

Or via NPM:
```bash
$ npm install ng-haversine
```

Once the library is downloaded, make sure you are referencing it in your `index.html`, just after the AngularJS library reference:
```html
<script src="./node_modules/ng-haversine/ng-haversine.min.js"></script>
```

You must inject the **ng-haversine** dependency within your module setter:
```javascript
angular.module("test", ["dahr.ng-haversine"]);
```

Now, you are ready to go. You will need two coordinates given in the format below:
```javascript
var coord1 = {
  "latitude": 40.4169473,
  "longitude": -3.7057172
};

var coord2 = {
  "latitude": 40.4236942,
  "longitude": -3.7109793
};
```

To calculate the distance between them, you must use the function `distance()` from the service `$haversine`:
```javascript
var distance = $haversine.distance(coord1, coord2);
```

**IMPORTANT:** The distance is given in meters.

## License

Code released under the [MIT license](./LICENSE).
