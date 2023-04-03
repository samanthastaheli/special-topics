# Week 11-12

## Notes
### Team 3 Code Requirements

#### Component Requirements
##### Set Icon in super
```JavaScript
icon_path="../assets/component_icons/Fuse_Holder.svg"
```
##### set the components rules in constructor
Example:
```JavaScript
this.blow_type = "Fast-acting";
this.current_rating = {
        min: 0,
        max: 60
      };
```

#### Methods required for each component 

* set_data (might be different name)
* update_self
* get_data_display
  * data that will be displayed for user
  * create JSON and add all attributes
  * only components specified rules not all the data
* get_data_raw
  * returns all data even if not used in the class
  * all data from the parent class (Component)
* add methods that verify UL rules
  * These are extra methods unique to every component. Name them whatever makes sense, they will not be pre-existing methods in Component.js like the get_data_raw() method.
  * call these methods in the update_self() 
 
#### Testing
Every component and its rules need to be tested. This is done in the script_test.html file. 

Take screenshots of test results and add them to the Google doc.

#### Common ErrorsNeed a new way to get display data

`JSON.stringify(this)` doesn't work. Gets circular reference error.

##### Import class wrong
Not including ".js". Will show a 403 error in console in browser.

###### Correct
```JavaScript
import { Fuse } from "./Fuse.js";
```

###### Wrong
```JavaScript
import { Fuse } from "./Fuse";
```

#### CADDIEngine

The CADDIEngine is the user interface. Each component needs to be added to it. 

##### Import component into CADDIEngine class

##### Add to dropdown list
Add to supported_components object near line 77 in CADDIEngine.js

Example:
```JavaScript
"Fuse Class G": ClassG,
```