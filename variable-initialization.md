# Variable Initialization in Delphi

* Global scope variables - guaranteed 0 *(both interface and implementation globals)*
* Object scope variables - guaranteed 0
* Function scope variables - undefined
* Function Result variable - undefined *(defined 0 by caller's scope, but recycled, thus effectively undefined)*

Note 1: Using the default memory mapping and default allocators. Mappers like FastMM and allocaters like MAlloc will show different behaviour.

Note 2: Applies to regular typed variables like Integers, Booleans, Strings, Arrays, Objects and Interfaced objects, but also the variables part of Records.

Note 3: 'Guaranteed 0' means 0 on Numeric and Pointer types, False for Booleans, 0 length and 0 references for strings, filled with zeros for Arrays

*These initializations were tested on Delphi XE 8 in both Debug and Release mode*
