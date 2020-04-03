# mise en place d'un projet leaflet

Dans un nouveau dossier:

```
npm init -y
npm install parcel-bundler --save-dev
npm install leaflet leaflet-defaulticon-compatibility --save
```

Dans `.gitignore`

```
node_modules
dist
.cache
```

Dans un dossier `src`

## `src/index.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="../node_modules/leaflet/dist/leaflet.css">
    <link rel="stylesheet" href="../node_modules/leaflet-defaulticon-compatibility/dist/leaflet-defaulticon-compatibility.css">
  </head>
  <body>
    <div id="map" style="width:1000px;height:500px;"></div>
    <script src="index.js"></script>
  </body>
</html>
```

## `src/index.js`

```js
import L from 'leaflet'
import 'leaflet-defaulticon-compatibility'
```

Dans `package.json`, un scripte pour démarrer:

```js
{
  "name": "mise-place-d3",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "parcel src/index.html"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "parcel-bundler": "^1.12.4"
  },
  "dependencies": {
    "d3": "^5.15.1"
  }
}
```