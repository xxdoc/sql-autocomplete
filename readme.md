
![screenshot](https://raw.githubusercontent.com/dzzie/sql-autocomplete/master/screen-shot.png)

<pre>

I am sure this still has some behaviors to refine but is mostly there.
its a bit parsing heavy right now. There may be some clever ways to lighten up the load.

behaviors:
   - syntax highlight sql keywords and quoted strings
   - load tables and fields from database for intellisense/auto suggest
   - auto suggest tables after keywords FROM and JOIN (including , list of tables)
   - auto suggest field names after tableName dot
   - do not trigger within quoted strings
   - CTRL Space auto complete partial table name or tableName.fieldName
   - CTRL Space at anytime will bring up table list
   - trigger auto suggest at proper times with proper context automatically (only)
   - support for table aliases (parsed incrementally as you type and on big changes like paste)

to do:
   - if only one table queried, auto suggest unqualified field names after WHERE, AND etc

dependencies: (installed with pdfstreamdumper and yara workbench)
   - open source Scintilla syntax highlight control written in C (300kb to 1mb)
      - http://www.scintilla.org

   - open source scivb2.ocx wrapper to access it written in VB6 (420kb)
      - https://github.com/dzzie/scivb2

discussion:
   https://www.vbforums.com/showthread.php?889424-sql-autocomplete-control


bugs: 
- ocx  "select * from tblpositions as t where t. - will auto complete title because its the only match in the list..
- ocx  table names ending in numbers cause a problem

</pre>
