# SurevyBuilderConsoleFile
<html>
<body>
 <h3>File Types List</h3>
<br><p><table border="1" cellpadding="5">
<tr><td bgcolor="E0E0E0" nowrap><b>Extension</b><td bgcolor=#FFFFFF nowrap>.sbconsole
<tr><td bgcolor="E0E0E0" nowrap><b>Type Name</b><td bgcolor=#FFFFFF nowrap>.sbconsole_auto_file
<tr><td bgcolor="E0E0E0" nowrap><b>Description</b><td bgcolor=#FFFFFF nowrap>SurveyBuilderConsole
<tr><td bgcolor="E0E0E0" nowrap><b>MIME Type</b><td bgcolor=#FFFFFF nowrap>text/sbconsole
<tr><td bgcolor="E0E0E0" nowrap><b>Perceived Type</b><td bgcolor=#FFFFFF nowrap>document
<tr><td bgcolor="E0E0E0" nowrap><b>In New Menu</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Excluded</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Always Show Extension</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Flags</b><td bgcolor=#FFFFFF nowrap>0x00020000
<tr><td bgcolor="E0E0E0" nowrap><b>Browser Flags</b><td bgcolor=#FFFFFF nowrap>0x00000000
<tr><td bgcolor="E0E0E0" nowrap><b>Default Icon</b><td bgcolor=#FFFFFF nowrap>C:\xampp\htdocs\SurveyBuilder\favicon.ico,0
<tr><td bgcolor="E0E0E0" nowrap><b>Modified Time</b><td bgcolor=#FFFFFF nowrap>10/05/2020 1:33:02 PM
<tr><td bgcolor="E0E0E0" nowrap><b>File Type Group</b><td bgcolor=#FFFFFF nowrap>Standard
<tr><td bgcolor="E0E0E0" nowrap><b>User Choice</b><td bgcolor=#FFFFFF nowrap>.sbconsole_auto_file
<tr><td bgcolor="E0E0E0" nowrap><b>Icon Handler CLSID</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Product Name</b><td bgcolor=#FFFFFF nowrap>SurveyBuilderConsole File
<tr><td bgcolor="E0E0E0" nowrap><b>Product Version</b><td bgcolor=#FFFFFF nowrap><a href="https://github.com/surveybuilderteams/surveybuilder/releases">Version</a>
<tr><td bgcolor="E0E0E0" nowrap><b>Product Description</b><td bgcolor=#FFFFFF nowrap>This is for SurveyBuilder Console file
<tr><td bgcolor="E0E0E0" nowrap><b>Company Name</b><td bgcolor=#FFFFFF nowrap>SurveyBuilder
</table><p>
<table border="1" cellpadding="5">
<tr><td bgcolor="E0E0E0" nowrap><b>Extension</b><td bgcolor=#FFFFFF nowrap>.sbconsole_auto_file
<tr><td bgcolor="E0E0E0" nowrap><b>Type Name</b><td bgcolor=#FFFFFF nowrap>SurveyBuilderConsole
<tr><td bgcolor="E0E0E0" nowrap><b>Description</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>MIME Type</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Perceived Type</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>In New Menu</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Excluded</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Always Show Extension</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Flags</b><td bgcolor=#FFFFFF nowrap>0x00000000
<tr><td bgcolor="E0E0E0" nowrap><b>Browser Flags</b><td bgcolor=#FFFFFF nowrap>0x00000000
<tr><td bgcolor="E0E0E0" nowrap><b>Default Icon</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Modified Time</b><td bgcolor=#FFFFFF nowrap>10/05/2020 1:29:46 PM
<tr><td bgcolor="E0E0E0" nowrap><b>File Type Group</b><td bgcolor=#FFFFFF nowrap>Standard
<tr><td bgcolor="E0E0E0" nowrap><b>User Choice</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Icon Handler CLSID</b><td bgcolor=#FFFFFF nowrap>&nbsp;
<tr><td bgcolor="E0E0E0" nowrap><b>Product Name</b><td bgcolor=#FFFFFF nowrap>SurveyBuilderConsole File
<tr><td bgcolor="E0E0E0" nowrap><b>Product Version</b><td bgcolor=#FFFFFF nowrap><a href="https://github.com/surveybuilderteams/surveybuilder/releases">Version</a>
<tr><td bgcolor="E0E0E0" nowrap><b>Product Description</b><td bgcolor=#FFFFFF nowrap>This is for SurveyBuilder Console file
<tr><td bgcolor="E0E0E0" nowrap><b>Company Name</b><td bgcolor=#FFFFFF nowrap>SurveyBuilder
</table><p>

</body></html>

***

# How to use

### Setting up(pt.1, setting up folders/startup's)
1. Go to RegEdit(Registry Editor)
2. Add folder name it ".sbconsole" in HKEY_CLASSES_ROOT
3. add 3 new files
 - new: "String", name: "(Default)", value: ".sbconsole_auto_file"
 - new: "String", name: "Content Type", value: "text/sbconsole"
 - new: "String", name: "PerceivedType", value: "document"
4. Add another folder name it ".sbconsole_auto_file" in the HKEY_CLASSES_ROOT
5. add 2 files
 - new: "String", name: "(Default)", value: "SurveyBuilderConsole"
 - new: "DWORD (32-bit) value", name: "EditFlag", value="20000", base: "hexadecimal"

### Setting up(pt.2, Icon)
1. Inside of ".sbconole_auto_file" click new>key(2x)
2. the first key name it "DefaultIcon" and the second key name it "shell"
3. Inside the "DefaultIcon"
 - new: "String", name: "(Default)", value: "C:\xampp\htdocs\SurveyBuilder\favicon.ico,0" (or wherever the surveybuilder icon is located).

### Setting up(pt.3, Shell)
1. Inside of "shell" click new>key(2x)
2. name the first key "edit" and the second key "open"
3. go to "edit"
 - new: "String", name: "(Default)", value: ""
 3a. new>key name it "command
 3b. in "command" 
- new: "Expandable String value", name: "(Default)", value: "%SystemRoot%\system32\NOTEPAD.EXE %1"
4. Go to "open"
 - new: "String", name: "(Default)", value: ""
 4a. new>key name it "command"
 4b. in "command"
 - new: "Expandable String value", name: "(Default)", value: "%SystemRoot%\system32\NOTEPAD.EXE %1"
 
 ### Finished
 

 

