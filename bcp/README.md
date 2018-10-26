# BCP Example

## Import People

Create database using `ddl.sql`. Then execute the `bcp` command to import the data in `people.csv`.

``` /bin/bash
bcp PeopleBcp in people.csv -T -c -t ,
```

Verify results:

``` /bin/bash
select *
from PeopleBcp;
```
Should result in:

| name | age |
| ---- | --- |
| Sue | 24 |
| Bob | 23 |
| Jan | 13 |
| Peter | 67 |
| Dan | 56 |