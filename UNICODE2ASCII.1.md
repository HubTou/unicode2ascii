# UNICODE2ASCII(1)

## NAME
unicode2ascii - Unicode to Ascii command-line tool

## SYNOPSIS
**unicode2ascii**
\[-a|--analyze\]
\[-t|--translated\]
\[-u|--untranslated\]
\[--debug\]
\[--help|-?\]
\[--version\]
\[--\]

## DESCRIPTION
The **unicode2ascii** utility filters Unicode characters in the standard input and replaces them by their standard or corrected Unicode equivalent,
or its internal equivalent if missing in Unicode.

Command line options disable filtering mode and analyze Unicode characters (**-a** option)
or report (un)translated Unicode characters (**-t** and **-u** options) in a format suitable for updating the source code.

### OPTIONS
Options | Use
------- | ---
-a\|--analyze|Analyze Unicode characters. Disable filter mode
-t\|--translated|Report translated Unicode characters. Disable filter mode
-u\|--untranslated|Report untranslated Unicode characters. Disable filter mode
--debug|Enable debug mode
--help\|-?|Print usage and a short help message and exit
--version|Print version and exit
--|Options processing terminator

## ENVIRONMENT
The UNICODE2ASCII_DEBUG environment variable can also be set to any value to enable debug mode.

## EXIT STATUS
The **unicode2ascii** utility exits 0 on success, and >0 if an error occurs.

## SEE ALSO
[unicode2ascii(3)](https://github.com/HubTou/unicode2ascii/blob/main/UNICODE2ASCII.3.md),
[iconv(1)](https://www.freebsd.org/cgi/man.cgi?query=iconv)

## STANDARDS
The **unicode2ascii** utility is not a standard UNIX/POSIX command.

It tries to follow the [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide for [Python](https://www.python.org/) code.

## HISTORY
This utility was made for [The PNU project](https://github.com/HubTou/PNU).

## LICENSE
This utility is available under the [3-clause BSD license](https://opensource.org/licenses/BSD-3-Clause).

## AUTHORS
[Hubert Tournier](https://github.com/HubTou)

## CAVEATS
So far, only the following Unicode character sets are processed for missing ASCII equivalents:
* C0 control characters
* C1 control characters
* Basic Latin characters
* Latin-1 Supplement
* Latin Extended-A
* Latin Extended-B
* Latin Extended Additional
* IPA Extensions
* Spacing Modifier Letters
* Unicode symbols
* General Punctuation
* Number Forms
* Cyrillic

