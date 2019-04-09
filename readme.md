# Google Maps HTML Markers

A tiny javascript helper library to create html markers with Google maps.

## Installation

```shell
npm install @posterno/google-maps-html-marker
```

or

```shell
yarn add @posterno/google-maps-html-marker
```

## Usage

Load the helper library in your javascript file:

```js
const createHTMLMapMarker = require( '@posterno/google-maps-html-marker' );

const latLng = new google.maps.LatLng(16.7666, -3.0026);
const mapOptions = {
	zoom: 11,
	center: latLng
};
const map = new google.maps.Map(document.getElementById("map"), mapOptions);

let marker = createHTMLMapMarker({
	latlng: latLng,
	map: map,
	html: `<img id="parrot" src="https://cultofthepartyparrot.com/parrots/hd/parrot.gif">`
});

marker.addListener("click", () => {
	alert("Partyin Partyin Yeah!");
});
```

### Credits

This library was originally created by Dan Ward and published as [a tutorial here](https://levelup.gitconnected.com/how-to-create-custom-html-markers-on-google-maps-9ff21be90e4b).

I've simply converted it to an ES5 javascript module and published it on the npmjs registry so that it's easier to re-use for my projects.
