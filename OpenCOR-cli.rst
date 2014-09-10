.. _OpenCOR-cli:

============================
Command Line Interface (CLI)
============================

Help
----

::

    $ ./OpenCOR -h
    Usage: OpenCOR [-a|--about] [-c|--command [<plugin>::]<command> <options>] [-h|--help] [-p|--plugins] [-s|--status] [-v|--version] [<files>]
    -a, --about     Display some information about OpenCOR
    -c, --command   Send a command to one or all the CLI plugins
    -h, --help      Display this help information
    -p, --plugins   Display all the CLI plugins
    -s, --status    Display the status of all the plugins
    -v, --version   Display the version of OpenCOR
 
Version
-------

::

   $ ./OpenCOR -v
   OpenCOR 0.3 (64-bit)

About
-----

::

   $ ./OpenCOR -a
   OpenCOR 0.3 (64-bit)
   OS X 10.9 (Mavericks)
   Copyright 2011-2014
   
   OpenCOR is a cross-platform CellML-based modelling environment, which can be used to organise, edit, simulate and analyse CellML files.

Plugins
-------

::

    $ ./OpenCOR -p
    The following plugin is loaded:
     - CellMLTools: a plugin to access various CellML-related tools.

Status
------

::

   $ ./OpenCOR -s
   The following plugins are available:
    - CellMLAPI: the plugin is loaded and fully functional.
    - CellMLSupport: the plugin is loaded and fully functional.
    - CellMLTools: the plugin is loaded and fully functional.
    - Compiler: the plugin is loaded and fully functional.
    - Core: the plugin is loaded and fully functional.
    - CoreSolver: the plugin is loaded and fully functional.
    - LLVM: the plugin is loaded and fully functional.
 
Command
-------

::

   $ ./OpenCOR -c help
   Commands supported by CellMLTools:
    * Display the commands supported by CellMLTools:
         help
    * Export <in_file> to <out_file> using <predefined_format> as the destination format or <user_defined_format_file> as the file describing the destination format:
         export <in_file> <out_file> [<predefined_format>|<user_defined_format_file>]
      <predefined_format> can take one of the following values:
         cellml_1_0: to export a CellML 1.1 file to CellML 1.0
   $ ./OpenCOR -c CellMLTools::export in.cellml out.cellml cellml_1_0
   $ ./OpenCOR -c CellMLTools::export http://mydomain.com/in.cellml out.txt format.xml
