# <b>Autonauts Modding API Snippents

This is an extention that contains snippets for all classes/functions of the Autonauts Modding API</b>


## **Snippet Format**
- **Prefix**: API call, including class
- **Description**: Information from the class member function documentation from [the Autonauts Modding API docs](http://www.denki.co.uk/autonauts/modding/index.html)
- **Body**:
  - Full function with parameters, one line per parameter.
  - Tabstops for each parameter.
  - An asterisk (*) before parameters that are required.
  - Includes the data type and default value (if any) commented to the right of the parameter

# **Snippets**
You can type things like "modobject." (case-***in***sensitive) and you will see options for "ModObject.GetObjectType", "ModObject.DestroyObject", "ModObject.GetObjectTileCoord", etc.
Typing just the function without the function's class also works. No need to memorise which class each function comes from.

TODO: gif of snippets usage

## **Snippet Example**

ModTool.CreateTool()

<pre>
ModTool.CreateTool(
    *UniqueName,               --string
    NewIngredientsStringArr,   --string[] = null
    NewIngredientsAmountArr,   --int[] = null
    ObjectsToUseOnArr,         --string[] = null
    TilesToUseOnArr,           --string[] = null
    ObjectsToProduceArr,       --string[] = null
    ObjectsToProduceAmountArr, --int[] = null
    AnimationDuration,         --float = 2.0f
    ModelName,                 --string = ""
    UsingCustomModel,          --bool = true
    CallbackOnComplete,        --DynValue = null
    DestroyTarget,             --bool = true
)</pre>

<b>Notes:</b>

<ul>
<li>Each parameter name is a tab stop
<li>comment to right shows you value type and default, if any
<li>Parameters starting with * indicate mandatory values
</ul>

<b>Code for generating the snippets.json file:<\b>
The snippets.json file is generated from the c# files from the game.
I do not host the c# files anywhere, as they are the property of Denki Games.
The program for generating the snippets.json file is available on repl.it at [autonautsVSCodeSnippitGenerator](https://replit.com/@ball-o-twine/autonautsVSCodeSnippitGenerator#main.py). The code is not pretty, and is sparsely commented.
The intermediate json files (which are just json versions of [the Autonauts Modding API docs](http://www.denki.co.uk/autonauts/modding/index.html)) are available there, and the snippets.json file is generated from those.
When updates to the modding API are made, the c# files will need to be TEMPORARILY put into the "API" folder and the program re-run.
Some fixes where made to the various c# files before processing (classes with no public API methods, typos, etc). I have 'corrected' copies of these locally, but a bit of trial-and-error would work out for anyone else.
  
## <b>Release Notes:</b>

### 0.0.4
Fixed trailing-comma issue after last param in snippet functions

### 0.0.3
Fixed repo url

### 0.0.2
Added icon

### 0.0.1
Initial release of Autonauts Modding API Snippents
