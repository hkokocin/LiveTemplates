# LiveTemplates

* **What it is for:** stop writing the same stuff over and over again
* **What it is not for:** make it easier to introduce code duplication

### Location

* **Windows**: <your_user_home_directory>\.IntelliJ IDEA<version_number>\config\templates
* **Linux**: ~IntelliJ IDEA<version>/config/templates
* **OS X**: ~/Library/Preferences/IntelliJ IDEA<version>/templates

## Create a new template
* use the preferences ( *Preferences/Editor/Live Templates* )
* Select a code snippet you want create a template from and use *Tools/Save as Live Template* from the menu

## Basics
### Imports
* Use fully qualified names of the entities you want imported
* Imports are organized automatically when template is applied

### Variables
* Are enclosed in ***$*** signs e.g. ***$NAME$***
* To escape the ***$*** sign use ***$$***
* predefined variables:
	*  ***$END$*** to set cursor position after finishing all variables 
	* ***$SELECTION$*** used in surround templates to place the snippet you want to surround with something 
* hit ***"Edit variables"***-Button to edit variables

### Context
The context defines where your new template will be available. A new tempate has no context set by default. 
* Below the template text you find a label saying ***"no applicable contexts yet"***
* click the link ***"define"*** next to that label to set a context
* you can set context for the different file types

## Predefined functions

* used to enhance variables
* when editing live template hit ***"Edit variables"***-Button to edit variables 
* [predefined functions reference](https://www.jetbrains.com/help/idea/2016.3/live-templates-2.html#predefined_functions)

### Gradle script
```
fun groovyScript(codeSnippet: String, varArg arguments: Any)
```
```
groovyScript("\"${_1} ${_2}\".toString()", "Hello", "World")
```
* arguments can be other variables or predefined functions
* access arguments with ***"_1"*** , ***"_2"*** , ***"_3"*** etc.
* escape **"** with **\\**
