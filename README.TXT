================================================================================
== DESCRIPTION
================================================================================
SolutionFormat is a tool for formatting all the documents in a Visual Studio
project. Sometimes, you receive a project that has a different brace style than
you or your team do, or maybe you just want to make sure that every file in your
project has a standard format. FormatSolution lets you do this automatically so
that you don't have to go through the hassle of manually opening every file
yourself!

SolutionFormat uses the Edit.FormatDocument command. Therefore, whatever
formatting options are specified by your Text Editor -> [LANGUAGE] settings are
used in the formatting process.

================================================================================
== INSTALLATION
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
== MODIFYING SUPPORTED FILETYPES
================================================================================
By default, FormatSolution only formats the following types of documents:

    .cs     - C# source files
    .vb     - Visual Basic source files
    .xml    - XML files
    .config - XML configuration files
    .aspx   - ASP.NET files

You may want to modify this list to support more filetypes, or remove a
filetype altogether. Here are the steps to do so:

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

