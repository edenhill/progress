progress
========

Provides a generic progress meter for any shell command.
It saves runtimes for each unique command (pwd + cmd + arguments) to provide
relevant time estimates.

Typical usage is for recurring long running makes.

Usage
-----

Provide a progress meter for any command:

    progress <command> <arguments..>


Always wrap 'make' in progress:

    alias make='progress make'


Show time statistics for the specified command:

    progress --stats <command> <arguments..>


Run times are saved to ~/.progress/.


Example
-------

Run progress on a linux kernel make:

    cd linux
    progress make

