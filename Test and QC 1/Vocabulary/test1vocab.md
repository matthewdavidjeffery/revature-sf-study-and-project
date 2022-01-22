# HTML
## Components of Basic HTML Document
```
<!DOCTYPE html>
<html>
<head>
<body></body>
</html>
```
## Complete `<head/>` Tag

```
<head>
	<title>My Title</title>
	<meta charset="utf-8">
	<meta name="description" content="Place the meta description text here.">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" type="text/css" href="path/to/css/file">
	<script src="demo_defer.js" defer></script>
</head>
```
## Semantic Markup
HTML Elements itself that convey some information about the type of content contained between the opening and closing tags.
Examples:
```
<header/>
<footer/>
```

# CSS

## Selectors
### Tag
`tag { };`
### Id
`#element-id { };`
### Class
`.class-name { };`
### Box Model
Margin > Border > Padding > Content (Outermost to innermost)


# JavaScript

## Types of Primitive Data Types
- Big Int
- Boolean
- Undefined
- Number
- Null
- Symbol

## Event Model
- Bubbling : Events travel down the DOM to the root element
- Capturing : Occurs before bubbling, traverses from the root element down to the target element
- Event phases: Capturing, Target Reached, Bubbling
- Capturing must be enabled to occur:
```
elem.addEventListener(..., {capture: true})
```

## ES Modules
 - JavaScript file that explicitly exports variables or functions that other modules can import and use.
 - For LWC, .html and .js are required to provide the display and code behind for the module to function.
 - A resource module may consist of a single CSS file to allow cross module style sharing
 - Name space is determined by folder location and exports in the `lwc.config.json` file
 - Modules use camelCase for JS and, when used in other components, kebab-case

 ```
 <!-- example.html -->
<template>
    My Component
</template>
 ```
 ```
// example.js
import { LightningElement } from 'lwc';

export default class Example extends LightningElement {}
export default class Example extends LightningElement {}

 ```

# Salesforce

## Definitions
- CRM : Customer relationship management (CRM) is a technology for managing all your company’s relationships and interactions with customers and potential customers. 
- PaaS : Platform as a Service (Custom Apex Apps, not the default prebuilt SF experience)
- Saas : Salesforce as software, so more the default experience
- Multi-tenant Environment : Cloud is shared among companies using SF PaaS and SaaS
- Governor Limits : Limits placed on tenants' use of resources such as storage, bandwidth or processing time
- Apex : Java-like Custom Salesforce Language
- Lightning Web Components : Responsive Web Components for immersive SPA development for SF

## Cloud Parts of SF
- Marketing Cloud
- Service Cloud
- Sales Cloud

# Lightning Web Components OSS

## Defintions
- Reactive: The framework observes changes to the values of fields and properties. When it observes a change, it reacts. It reevaluates all the expressions used in the template and rerenders the component, which displays the new values.

## Starting an LWC-OSS project
- [LWC-OSS Site]("http://lwc.dev")
```
npx create-lwc-app project-name
cd project-name
npm run watch
```
## Module Structure
- Folder in namespace
- HTML file with same name as folder
- JS file with same name as folder
- Optional CSS file with same name as folder
- HTML file minimally structured:
```
<template>
<!-- Template Code Here -->
</template>
```
- JS File minimally structured:
```
import {LightningElement} from 'lwc';

export default class myElement extends LightningElement {
	// Element code here
}
```

