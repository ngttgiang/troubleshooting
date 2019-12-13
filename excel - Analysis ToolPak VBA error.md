# Analysis ToolPak VBA causes error to open and close Excel

### Description of the issue

* Environment: window 10, office 2013
* First, enable Add-in Analysis ToolPak VBA in excel
* Then Excel can't be closed normally. The only option to close is to End Process in Task Manager
* Next time when openning Excel, there is an error message prompted saying ".. _Active method of workbook fail..."

### Solution

* When the error message is prompted, choose "End"
* A new workbook is opened.
* Go to **`File > Options > Trust Center > Trust`** Center Setting
  - In `Trusted Location`: remove the location containing the Add-in.
    i.e C:\Program Files (x86)\Microsoft Office\Office15\Library\Analysis\
  - In `Add-ins` : choose option "Disable all Application Add-ins"
  - In `ActiveX Settings` : choose "Disable all controls without notification"
  - In `Macro Settings`: choose "Disable all macros with notification"
 * Go to **`File>Options > Add-ins > Manage > Excel Add-ins > Go >`** uncheck Analysis ToolPak VBA
 * Save the workbook
 * Try to close the workbook
 * Next time when opening Excel, there should be no more error message. Check in  File>Options > Add-ins whether Analysis ToolPak VBA is not active. 
 Be careful not to add this add-in next time :)
 * Change other setting in Trust Center Setting to the desired values.
 
 -- end ---
