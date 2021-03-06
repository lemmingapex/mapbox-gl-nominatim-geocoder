<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [MapboxNominatimGeocoder](#mapboxnominatimgeocoder)
    -   [query](#query)
    -   [setInput](#setinput)
    -   [on](#on)
    -   [off](#off)

## MapboxNominatimGeocoder

A geocoder component using Mapbox Geocoding API

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
    -   `options.zoom` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** On geocoded result what zoom level should the map animate to when a `bbox` isn't found in the response. If a `bbox` is found the map will fit to the `bbox`. (optional, default `16`)
    -   `options.flyTo` **[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** If false, animating the map to a selected result is disabled. (optional, default `true`)
    -   `options.placeholder` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Override the default placeholder attribute value. (optional, default `"Search"`)
    -   `options.bbox` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)?** a bounding box argument: this is
        a bounding box given as an array in the format [minX, minY, maxX, maxY].
        Search results will be limited to the bounding box.
    -   `options.email` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** an email to send with Nominatim requests
    -   `options.country` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** a comma separated list of country codes to
        limit results to specified country or countries.
    -   `options.minLength` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** Minimum number of characters to enter before results are shown. (optional, default `2`)
    -   `options.limit` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** Maximum number of results to show. (optional, default `5`)

**Examples**

```javascript
var geocoder = new MapboxNominatimGeocoder();
map.addControl(geocoder);
```

Returns **[MapboxNominatimGeocoder](#mapboxnominatimgeocoder)** `this`

### query

Set & query the input

**Parameters**

-   `searchInput` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** location name or other search input

Returns **[MapboxNominatimGeocoder](#mapboxnominatimgeocoder)** this

### setInput

Set input

**Parameters**

-   `searchInput` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** location name or other search input

Returns **[MapboxNominatimGeocoder](#mapboxnominatimgeocoder)** this

### on

Subscribe to events that happen within the plugin.

**Parameters**

-   `type` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** name of event. Available events and the data passed into their respective event objects are:-   **clear** `Emitted when the input is cleared`
    -   **loading** `{ query } Emitted when the geocoder is looking up a query`
    -   **results** `{ results } Fired when the geocoder returns a response`
    -   **result** `{ result } Fired when input is set`
    -   **error** \`{ error } Error as string
-   `fn` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** function that's called when the event is emitted.

Returns **[MapboxNominatimGeocoder](#mapboxnominatimgeocoder)** this;

### off

Remove an event

**Parameters**

-   `type` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Event name.
-   `fn` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** Function that should unsubscribe to the event emitted.

Returns **[MapboxNominatimGeocoder](#mapboxnominatimgeocoder)** this
