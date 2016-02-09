# Angara.Table
A library for tabular data manipulation, for scientific programming and visualization, and for reading and writing delimited files (e.g. CSV files).

## Table API (F#)

_to do_

## Reading a table from a delimited text file (F#)

The following example reads a column of real numbers named "wheat" from a CSV file:
```F#
use stream = File.OpenRead(@"tests\wheat.csv")
let table = Table.Read ReadSettings.CommaDelimited stream
let wheat = table |> Table.ToArray<float[]> "wheat"
```

## Writing a table to a delimited text file (F#)

The following example writes a table to a CSV file:
```F#
let table : Table = ...
use stream = File.OpenWrite("data.csv")
table |> Table.Write WriteSettings.CommaDelimited stream
```

## View a table in HTML

_to do_
