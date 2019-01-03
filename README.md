# VSC-cheatsheet
Some helpful commands and shortcuts for VSCODE

All key bindings can be found [here](https://code.visualstudio.com/docs/getstarted/keybindings).

### Features 

* IntelliSense
  * Bracket Matching
* Peeking
  * See a function/variable def. in line
* Code Navigation
  * Regex expressions
  * Hovering
  
## Peek
We think there's nothing worse than a big context switch when all you want is to quickly check something. That's why we support peeked editors. When you execute a Peek References search (via Shift+F12)

```
Shift+F12
```

## Errors and Warnings
Warnings or Errors can be generated either via configured tasks, by rich language services, or by linters, that constantly analyze your code in the background. Since we love bug-free code, warnings and errors show up in multiple places:

* In the Status Bar, there is a summary of all errors and warnings counts.
* You can click on the summary or press Ctrl+Shift+M to display the PROBLEMS panel with a list of all current errors.
* If you open a file that has errors or warnings, they will be rendered inline with the text and in the overview ruler.

## Find and Replace control
The Find and Replace control appears in the upper right corner of the code editor window. The Find and Replace control immediately highlights every occurrence of the given search string in the current document. You can navigate from one occurrence to another by choosing the Find Next button or the Find Previous button on the search control.

```
CTRL+F2
```
## Command Palette
VS Code is equally accessible from the keyboard. The most important key combination to know is Ctrl+Shift+P, which brings up the Command Palette. From here, you have access to all of the functionality of VS Code, including keyboard shortcuts for the most common operations.

Creating your own keybindings can be done by going to file -> prefrences -> keyboard shortcuts

```
CTRL+SHIFT+P
```

* Opening all recently opened files can be done with:
```
CTRL+TAB
```
* Jump to certain line number
```
CTRL+G
```
* Find multiple instances of a variable
```
CTRL+SHIFTL
```
* Activating IntelliSense
```
CTRL+SPACE
```
* Cycle through available options
```
CTRL+SHIFT+. [cycles forward]

CTRL+SHIFT+, [cycles backward]
```

## Side Bar
Toggle side bar on and off

```
CTRL+D
```

## Side by Side Editing
You can open as many editors as you like side by side vertically and horizontally. If you already have one editor open, there are multiple ways of opening another editor to the side of the existing one

```
CTRL+ENTER
```

## Searching Accross Files
For a specific word or phrase.

Will search accross all files and folders you have on VS

```
CTRL+SHIFT+F
```
**Regular expression searching

ex: Searching for projects that start with A and are C#
```
[A]*\.csproj
```

## HTML
[Emmet](https://docs.emmet.io/) is a set of plug-ins for text editors that allow for high-speed coding and editing in HTML, XML, XSL, and other structured code formats via content assist.

Basically, most text editors out there allow you to store and re-use commonly used code chunks, called “snippets”. While snippets are a good way to boost your productivity, all implementations have common pitfalls: you have to define the snippet first and you can’t extend them in runtime.

Emmet takes the snippets idea to a whole new level: you can type CSS-like expressions that can be dynamically parsed, and produce output depending on what you type in the abbreviation. Emmet is developed and optimised for web-developers whose workflow depends on HTML/XML and CSS, but can be used with programming languages too. 

```
#page>div.logo+ul#navigation>li*5>a{Item $}

```
would be transformed to 
```HTML
<div id="page">
    <div class="logo"></div>
    <ul id="navigation">
        <li><a href="">Item 1</a></li>
        <li><a href="">Item 2</a></li>
        <li><a href="">Item 3</a></li>
        <li><a href="">Item 4</a></li>
        <li><a href="">Item 5</a></li>
    </ul>
</div>
```
Create your own snippet by going to File -> Prefrences -> User Snippets

Choose the language you want to add a snippet to

```
"multi line comment":{
  "prefix":"multilinecomment",
  "body":[
    "<!-", "", "->"
    ],
    "description":"Multi line HTML comment"
},
```

## Markdown
Markdown can be used to automate our HTML 

Previewing a markdown fil can be done with:
```
CTRL+SHIFT+V
```

Turn a .md file into HTLM by utilizing a tasks.json file, opening up the options pallete and choosing configure task runner

gulp and gulp-markdown allow gulp task runner to run tasks that convert .md files to compiled HTML, also acts as a file watcher and automatically compiles markdown to HTML
