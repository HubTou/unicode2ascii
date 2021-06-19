# UNICODE2ASCII(3)

## NAME
unicode2ascii - Unicode to Ascii Python library

## SYNOPSIS
**import unicode2ascii**

*Boolean* unicode2ascii.**is_unicode_category**(String *character*, String *category*)

*Boolean* unicode2ascii.**is_unicode_letter**(String *character*)

*Boolean* unicode2ascii.**is_unicode_mark**(String *character*)

*Boolean* unicode2ascii.**is_unicode_number**(String *character*)

*Boolean* unicode2ascii.**is_unicode_punctuation**(String *character*)

*Boolean* unicode2ascii.**is_unicode_symbol**(String *character*)

*Boolean* unicode2ascii.**is_unicode_separator**(String *character*)

*Boolean* unicode2ascii.**is_unicode_other**(String *character*)

*String* unicode2ascii.**unicode_category**(String *category*)

*String* unicode2ascii.**unicode_to_ascii_character**(String *character*, [String *default* = ''])

*String* unicode2ascii.**unicode_to_ascii_string**(String *string*, [String *default* = ''])

unicode2ascii.**analyze_unicode_character**(String *character*)

## DESCRIPTION
The **is_unicode_category**() function returns True if *character* belongs to the *category* Unicode category or False if not.

All the other **is_unicode_XXX**() functions return True if *character* belongs to the XXX category.

The **unicode_category**() function return a one-line description of the specified *category*.

The **unicode_to_ascii_character**() function returns the ASCII equivalent of an unicode *character*, or an unchanged non-Unicode character.
If there is no ASCII equivalent, it returns the *default* string ("" if not provided).

The **unicode_to_ascii_string**() does the same for all the characters in the *string*.

The **analyze_unicode_character**() function returns all available information about the Unicode *character*.

## ENVIRONMENT
The UNICODE2ASCII_DEBUG environment variable can be set to any value to enable debug mode.

## SEE ALSO
[unicode2ascii(1)](https://github.com/HubTou/unicode2ascii/blob/main/UNICODE2ASCII.1.md)
[iconv(3)](https://www.freebsd.org/cgi/man.cgi?query=iconv&sektion=3)

## STANDARDS
The **unicode2ascii** library tries to follow the PEP 8 style guide for Python code.

## HISTORY
This library was made for [The PNU project](https://github.com/HubTou/PNU).

## LICENSE
This library is available under the [3-clause BSD license](https://opensource.org/licenses/BSD-3-Clause).

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

