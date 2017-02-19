# ng-selectize

[![npm version](https://badge.fury.io/js/ng-selectize.svg)](https://badge.fury.io/js/ng-selectize)

Angular2 component for [selectize.js](https://selectize.github.io/selectize.js/)

[Hosted Example Site](https://nicholasazar.github.io/ng-selectize)

## Including within existing angular-cli project
1. `yarn add jquery selectize ng-selectize`
2. Add:
    `"../node_modules/selectize/dist/css/selectize.css",`
    `"../node_modules/selectize/dist/css/selectize.{your chosen theme}.css"`
    to the styles array within `.angular-cli.json`
    
    (semantic-ui theme has been added to ng-selectize/selectize/selectize.semantic.css if needed)
3. Add:
	`"../node_modules/jquery/dist/jquery.min.js",`
	`"../node_modules/ng-selectize/selectize/selectize.standalone.js"` (or take from /node_modules/selectize/...)
	to the scripts array within `angular-cli.json`
3. Import module within applicable @NgModule:
   `import {NgSelectizeModule} from 'ng-selectize';`
   `imports: [..., NgSelectizeModule, ...],`
4. Use within template: `<ng-selectize {attributes}></ng-selectize>`
 
## Running the demo
 ```
 git pull git@github.com:NicholasAzar/ng-selectize-demo.git
 cd ng-selectize-demo
 yarn
 npm start
 // navigate to localhost:4200
 ```
 
 ## Docs
 The docs directory within this repo is the `ng build --prod --aot` result of the [ng-selectize-demo](https://github.com/NicholasAzar/ng-selectize-demo) repository.
 Hosted at [nicholasazar.github.io/ng-selectize](https://nicholasazar.github.io/ng-selectize)
 
## Attributes
| Attribute | Type | Default | Description | Implemented |
| --- | --- | --- | --- | --- |
| config | Object | null | Selectize config | Yes |
| options | Array | null | Available options to select from | Yes |
| placeholder | String | '' | Placeholder text to be displayed. Is overridden if hasOptionsPlaceholder/noOptionsPlaceholder are non-null | Yes |
| noOptionsPlaceholder | String | '' | Placeholder text to be displayed when no options are available | Yes |
| hasOptionsPlaceholder | String | '' | Placeholder text to be displayed when options are available | Yes |
| enabled | Boolean | true | Enables the input field when true, disabled otherwise | Yes |
| optionGroups | Object | null | Organize options within groups | Yes |

## Included Selectize Plugins
| Name | Options | Description |
| --- | --- | --- |
| dropdown_direction | {'auto', 'up', 'down'} | Control the direction in which the dropdown opens. |

