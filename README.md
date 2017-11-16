# PolymerVis
PolymerVis is a suite of Polymer elements for visualizations.

## Usage
**Installation**
```
npm i @polymer-vis/polymer-vis --save
```
```
yarn add @polymer-vis/polymer-vis --save
```
**Import into project**
```js
import PolymerVis from '../polymer-vis/polymer-vis.js';
```
```js
import {insertCssIntoShadowRoot} from '../polymer-vis/polymer-vis.js';
```
  
## API reference
  <a name="PolymerVis.loadScript"></a>

## PolymerVis.loadScript(src, onload, onerror, optAsync) ⇒ <code>HTMLScriptElement</code>
Convenience method for dynamically loading a script.

This method creates a new `<script>` element with the provided URL and
appends it to the document to start loading. In the onload callback, the
import property of the link element will contain the imported document
contents.

**Kind**: static method of [<code>PolymerVis</code>](#PolymerVis)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| src | <code>string</code> |  | The url to the script to load. |
| onload | <code>function</code> |  | callback when script is loaded. |
| onerror | <code>function</code> |  | callback when error loading script. |
| optAsync | <code>boolean</code> | <code>true</code> | whether to execute the script asynchronously. |

  <a name="PolymerVis.loadStylesheet"></a>

## PolymerVis.loadStylesheet(href, onload, onerror, optAsync) ⇒ <code>HTMLLinkElement</code>
Convenience method for dynamically loading a stylesheet.

This method creates a new `<link rel="stylesheet">` element with the
provided URL and appends it to the document to start loading. In the onload
callback, the import property of the link element will contain the
imported document contents.

**Kind**: static method of [<code>PolymerVis</code>](#PolymerVis)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| href | <code>string</code> |  | The url to the script to load. |
| onload | <code>function</code> |  | callback when script is loaded. |
| onerror | <code>function</code> |  | callback when error loading script. |
| optAsync | <code>boolean</code> | <code>true</code> | whether to execute the script asynchronously. |

  <a name="PolymerVis.insertCssIntoShadowRoot"></a>

## PolymerVis.insertCssIntoShadowRoot(cssSrc, shadowRoot, onload, id)
Load an external CSS file, and insert a `style` element
into the shadowRoot.

**Kind**: static method of [<code>PolymerVis</code>](#PolymerVis)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| cssSrc | <code>String</code> |  | url to the css file |
| shadowRoot | <code>String</code> |  | Node to insert the `style` element |
| onload | <code>function</code> |  | callback when CSS is inserted |
| id | <code>String</code> | <code>custom</code> | id for style element |

**Example**  
```js
import PolymerVis from '../polymer-vis/polymer-vis.js';
PolymerVis.insertCssIntoShadowRoot('https://some.css', ele.shadowRoot, null, 'custom');
```
  <a name="PolymerVis.isInShadowRoot"></a>

## PolymerVis.isInShadowRoot(node) ⇒ <code>Node</code>
Check if the node is inside a [`shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/shadowRoot) or not.
Return the `shadowRoot` otherwise return `false`.

**Kind**: static method of [<code>PolymerVis</code>](#PolymerVis)  

| Param | Type | Description |
| --- | --- | --- |
| node | <code>Node</code> | the node to check |

