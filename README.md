# Learning mode

A template that allows you to switch windows to user learning mode.

## What do I mean by "learning mode"?  
This is a mode in which the user is guided step by step through the purpose of the window and controls.  
  
Below is a sample usage of learning mode.  

For example, let's take the School application, and the browse of students:
![Learning mode intro tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/browsestudents.jpg?raw=true)  

If the template was set to switch this window to the learning mode immediately on Event:OpenWindow, the user will see this picture instead of the above:
![Learning mode intro tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/lm-browse-intro-tooltip.jpg?raw=true)  
The first step briefly explains where the user is and what to do next.  

Next steps lead to most significant controls and their purpose.  
SHEET control:  
![Learning mode sheet control tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/lm-browse-sheet-tooltip.jpg?raw=true)  
As you can see, the tooltip points to the control being described (in this case, the sheet control), which in turn is highlighted with a frame.

Update buttons:  
![Learning mode change button tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/lm-browse-change-button-tooltip.jpg?raw=true)  

The optional final step brings the entire lesson to a close.
![Learning mode bye tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/lm-browse-bye-tooltip.jpg?raw=true)  

During a lesson, the user can directly click on a control to read the tooltip for that control. It is also possible to navigate between tooltips using the arrow keys, Page Up and Page Down, Home and End.

## Learning mode customization
Almost everything can be customized: 
- fonts
- colors
- transparency
- frame thickness
- anchors (a location of tooltips relative to controls)
- code page
- hot key

See template screenshots below.

## Global extension
Here you set general settings for all application windows in learning  mode.

![Global extension general](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-general.jpg?raw=true)  

Tooltip customization:
![Global extension UI Tooltip](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-ui-tooltip.jpg?raw=true)  

Window caption customization:
![Global extension UI Window caption](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-ui-caption.jpg?raw=true)  

Selected control customization:
![Global extension UI Selected control](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-ui-control.jpg?raw=true)  

## Procedure extension
Create as many tooltips as you need. To set the appropriate anchor mode, refer to the image in "Anchor modes" chapter below.
![Procedure extension general](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-local-general.jpg?raw=true)  
![Procedure extension Tooltip settings](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/tpl-local-tooltip-settings.jpg?raw=true)  

Or, instead, you can load tooltips from an external JSON file. Below is an excerpt from the file corresponding to the BrowseStudents example:

```
{
  "name": "BrowseStudents",
  "tooltips": [{
    "control": "WINDOW",
    "text": "The window 'Browse the Students File' is designed to search\r\nand edit student records.\r\nClick on this tooltip to continue learning\r\nor press ESC to cancel.\r\nYou can always return to learning mode\r\nby pressing Ctrl+Shift+L.",
    "anchor": "CenterCenter"
  },  {
    "control": "?CURRENTTAB",
    "text": "You can change\r\na sort order \r\nby clicking on an \r\nappropriate tab",
    "anchor": "LeftBelow"
  },  {
    "control": "?CHANGE:2",
    "text": "These buttons are used to add, edit and delete records.",
    "anchor": "LeftAbove"
  },  {
    "control": "WINDOW",
    "text": "This is the final tip.\r\nClick here to exit learning mode.",
    "anchor": "CenterCenter"
  }]
}
```
## Anchor modes
There are 13 anchor modes, you can see all of them on the screenshot below.
![Anchor modes](https://github.com/mikeduglas/Learning-mode/blob/master/screenshots/anchors.jpg?raw=true)  

### Requirements
- C6.3 and higher
- ABC and Clarion template chains

### Dependencies
- [winapi](https://github.com/mikeduglas/winapi) (**latest version required**)
- [gdiplus](https://github.com/mikeduglas/gdiplus) (**latest version required**)
- [cjson](https://github.com/mikeduglas/cjson) (**latest version required**)
- [printf](https://github.com/mikeduglas/printf)

### Contacts
mikeduglas@yandex.ru

### Price
Negotiable
