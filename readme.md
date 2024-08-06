# Advanced DAX  

Testing and practicing:
1. Advanced CALCULATE with different modifiers
- ALL(), REMOVEFILTERS(), KEEPFILTERS(), ALLSELECTED(), ALLEXCEPT()
2. Advanced Time Intelligence functions
3. Calculated Table Joins
- CROSSJOIN, UNION, EXCEPT, INTERSECT
4. Iterators
5. Performance tuning
6. Scalar functions
- SUM(), AVERAGE(), MIN(), MAX(), COUNT(), DISTINCTCOUNT(), COUNTROWS()
- IN(), ROUND(), ROUNDUP(), ROUNDDOWN(), MROUND(), TRUNC(), FIXED(), CEILING(), FLOOR()
- ISBLANK(), ISERROR(), ISLOGICAL(), ISNUMBER(), ISNONTEXT(), ISTEXT()
- CURRENCY(), FORMAT(), DATE(), TIME(), DATEVALUE(), VALUE()
- IF(), AND(), OR()
- SWITCH()
- COALESCE()
7. Table and Filter Functions
- ALL(), FILTER() - returns tables but also used as modifiers in CALCULATE
- DISTINCT(), VALUES()
- SELECTEDVALUE()
- SELECTCOLUMNS(), ADDCOLUMNS(), SUMMARIZE(), GROUPBY()
- ROW(), DATATABLE(), GENERATESERIES(), TABLE CONSTRUCTOR


# Notes

## Calculated columns
- Values are calculated based on information from each row of a table (has row context)
- Appends static values to each row in a table and stores them in the model (which increases file size)
- Recalculate on data source refresh or when changes are made to component columns
- Primarily used as rows, columns, slicers or filters

## Measures
- Values are calculated based on information from any filters in the report (has filter context)
- Does not create new data in the tables themselves (doesn’t increase file size)
- Recalculate in response to any change to filters within the report
- Almost always used within the values field of a visua
