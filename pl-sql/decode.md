# What is DECODE function in SQL?

In Oracle, DECODE function allows us to add procedural if-then-else logic to the query. DECODE compares the expression to each search value one by one. If expression is equal to a search, then the corresponding result is returned by the Oracle Database. If a match is not found, then default is returned. If default is omitted, then Oracle returns null.
### Exp

```sql
SELECT bank_name,
DECODE(bank_id, 001, 'SBI',
                    002, 'ICICI',
                    003, ‘Dena',
                    'Gateway') result
FROM banks;

```
Equivalent IF-THEN-ELSE statement for the above DECODE() statement:

```sql
IF bank_id = 001 THEN
   result := 'SBI';

ELSIF bank_id = 002 THEN
   result := 'ICICI';

ELSIF bank_id = 003 THEN
   result := 'Dena';

ELSE
   result := 'Gateway';

END IF;

```
