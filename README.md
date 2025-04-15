# CBT636
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 636 is a REXX to execute TSO commands in a very general   *   FILE 636
//*           manner, against a list of datasets.  A description    *   FILE 636
//*           of how the WCOMMAND exec works, follows below.        *   FILE 636
//*                                                                 *   FILE 636
//*      Description of the WCOMMAND REXX EXEC.                     *   FILE 636
//*                                                                 *   FILE 636
//*         This REXX attempts to execute any TSO command           *   FILE 636
//*      against any (LISTCAT LEV( )) level of files.  It can       *   FILE 636
//*      also select certain files from the designated level        *   FILE 636
//*      with another string required to be a part of the file      *   FILE 636
//*      name in its lower levels.                                  *   FILE 636
//*                                                                 *   FILE 636
//*         The inputs are:  First, the level of the files to be    *   FILE 636
//*      operated on by the command.  The second argument is the    *   FILE 636
//*      TSO command with a single '*' in it which will be          *   FILE 636
//*      replaced with the designated file names.  The command      *   FILE 636
//*      entered should be enclosed in quotes, and either single    *   FILE 636
//*      or double quotes may be used depending on the user's       *   FILE 636
//*      whim or the existing quotes within the command.            *   FILE 636
//*                                                                 *   FILE 636
//*         The third argument is the other string to               *   FILE 636
//*      be looked for in the file names for them to be used        *   FILE 636
//*      in the command.  If there is no selection desired          *   FILE 636
//*      among files within the level, an * may be used for         *   FILE 636
//*      this argument.  The final and optional argument may        *   FILE 636
//*      be EXEC in order to execute the commands.  If this is      *   FILE 636
//*      not used, the commands will only be listed.  The           *   FILE 636
//*      program tries to avoid executing commands without the      *   FILE 636
//*      user taking due caution because it can create havoc        *   FILE 636
//*      with a system, so please be careful trying to use it.      *   FILE 636
//*                                                                 *   FILE 636
//*   Below are sample command lines:                               *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND IBMUSER "LISTC ENT(*) ALL" *                      *   FILE 636
//*       (does LISTC ENT('IBMUSER.*') ALL in all cases - dry run)  *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND IBMUSER "LISTC ENT(*) ALL" string                 *   FILE 636
//*       (does LISTC ENT('IBMUSER.*') ALL only w/string in         *   FILE 636
//*        low level qualifiers - dry run)                          *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND IBMUSER "LISTC ENT(*) ALL" * EXEC                 *   FILE 636
//*       (same as above - actually executes the commands)          *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND IBMUSER "LISTC ENT(*) ALL" string EXEC            *   FILE 636
//*       (same as above - actually executes the commands)          *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND SYSTEMS.DUMP 'DEL *' DMP00                        *   FILE 636
//*       (does DEL 'SYSTEMS.DUMP.*' where the string DMP00 is      *   FILE 636
//*        in the low level qualifiers - dry run)                   *   FILE 636
//*                                                                 *   FILE 636
//*      WCOMMAND SYSTEMS.DUMP 'DEL *' DMP00 EXEC                   *   FILE 636
//*       (does DEL 'SYSTEMS.DUMP.*' where the string DMP00 is      *   FILE 636
//*        in the low level qualifiers - executes the commands)     *   FILE 636
//*                                                                 *   FILE 636
```
