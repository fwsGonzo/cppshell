<<<<<<< HEAD
# Perfdata

A lightweight library / toolkit for:
  * Collecting system totals 
    * CPU-usage from `/proc/stat` 
      * for each CPU core
    * Memory-usage from `/proc/meminfo`
  * Collecting Process usage data from `/proc/<pid>/stat` and `/proc/<pid>/meminfo`

## Usage
Mostly intended as a static library -  `perfdata.a`. The makefile will also output `procstat`, which can be used as-is for creating csv-files, and and `pidstat` which is just a demo.

* `procstat -H` will output a tab-separated list of table headers for /proc/stat data
* `procstat` will output a tab-separated list of data, matching the above headers
* `pidstat <pid>` will output some of the information it collected from `/proc/<pid>/stat`. NOTE: As of Linux 3.3, everyghing gets collected - just not printed out. 
=======
# cppshell
Run shell commands from C++. Also a simple subprocess module for running commands asynchronously.

## `cmd` basic usage (C++11 syntax)

```
cout << cmd{"ls -l"} << endl;
```
Outputs whatever `ls -l` outputs. To get the results as a string:

```
string user = cmd{"whoami"}.str();
cout << "Username: " << user << endl;
```

The default behavior is for a command to throw an exception if it fails. See [demo.cpp](./demo.cpp) for more examples.

## `subprocess` basic usage (C++11 syntax)
```
cppshell::subprocess proc{"ls","-l"};
```
This call will return immediatly, having started the command in a separate thread. You can now read from it's stdout, by getting its file descriptor: `proc.stdout()` (no support for writing back to it yet - that just requires another pipe).  

Reading "everything" from the subprocess:
```
    cout << proc << endl;
```

>>>>>>> 28bac77493ea14b41708e787ef143d095d190383


## License: GPL v3
```
<<<<<<< HEAD
    perfdata - C++ classes to parse /proc/stat and /proc/<pid>/stat
    Copyright (C) 2015 Alfred Bratterud
=======
    cppshell - facilities to simplify calling shell commands for C++
    Copyright (C) 2015 Alfred Bratterud

>>>>>>> 28bac77493ea14b41708e787ef143d095d190383
    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
<<<<<<< HEAD
```

Full license text under [LICENSE.txt](./LICENSE.txt)
=======

```
Full license text under [LICENSE.txt](./LICENSE.txt)
>>>>>>> 28bac77493ea14b41708e787ef143d095d190383
