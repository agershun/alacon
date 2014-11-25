# alacon
======
(c) 2014, Andrey Gershun Version 0.0.0 Date: 26.11.2014

Alacon - command-line SQL for text (CSV, TAB) and Excel (XSLX, XLS) files powered by [Alasql](https://github.com/agershun/alasql).

How to use from command line:
```
    alacon "select [1] from tab('./mytext.txt') where [0] = 1"
    
    # From command file
    alacon -f myprogram.sql 

    # like grep 
    alacon "select * from csv(?) where [0] != 1 and [1] like 'A%'" mytext.csv
    
    # like calculator
    alacon "select 2*2"
    
    # Process Excel file
    alacon "select [2] from xls(?) where [0]>0 and [1] in ('Cuba','Swiss')" mysheet.xlsx
    
    # Join TAB and xlsx
    alacon "select a.* from tab(?) as a left join xls(?) as b on a[0] = b[0] where b[0] != 2" sales.txt cities.xls
    
```

How to install:
```
    npm install alacon -g
```

## Warning
Work in progress
