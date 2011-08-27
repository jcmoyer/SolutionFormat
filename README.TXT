================================================================================
== INSTALLING
================================================================================
1.) Open Visual Studio 2010.

2.) Go to Tools -> Macros -> Macro Explorer or press ALT+F8.

3.) Right click on Macros at the top of the Macro Explorer and click Load Macro
    Project...

4.) Navigate to FormatSolution.vsmacros and click OK.

================================================================================
== HOW TO USE
================================================================================
1.) With Visual Studio 2010 open and a project loaded, go to Tools -> Macros ->
    Macro Explorer or press ALT+F8.

2.) Expand the FormatSolution macro project, then expand the FormatSolution
    module. Double click Run.

3.) The macro will then cycle through all of the available files in your
    solution and execute the Format Document command.

================================================================================
== SUPPORTING MORE FILETYPES
================================================================================
1.) After you have installed the macro project, go to the Macro Explorer
    (ALT+F8).

2.) Expand the FormatSolution macro project, then right click on the
    FormatSolution module. Click Edit.

3.) Find "Public Sub Run()" (it is the topmost sub in the file -- if outlining
    is enabled, expand the Methods region).

4.) Under the area marked "Modify list of extensions here," add the file
    extensions you want this macro to support. For example, if you wanted to
    allow the macro to format code files with a ".foo" extension, add a line
    like so:
        allowedExts.Add(".foo")

