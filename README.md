SCHEMA DIFF
===========
This script produces SQL differences between to database schemas, so that applying the diff to the first database produces the second database.

Usage variant 1:
----------------
	schema-diff schema1 schema2 [outfile]
	This variant is used to specify the schema files for DB1 and DB2 along with an optional output file

Usage variant 2:
----------------
	schema-diff [options]
	This variant allows specifying additional options
	Available options:
	-1, --s1, --schema1 [filename] - Read first schema from file
	-2, --s2, --schema2 [filename] - Read second schema from file
	-o, --output [filename]        - Output to file (optional, output is normaly displayed)
	-f, --skip-fk-changes          - Skip any foreign key changes
	-c, --skip-create-table        - Don't check if tables are missing
	-d, --skip-drop-table          - Don't check there are too many tables
	-t, --skip-full-tables         - Don't show CREATE/DROP for full tables (the above two together)
	-r, --skip-renames             - Don't allow renaming columns
	-h, --help                     - Show this help
