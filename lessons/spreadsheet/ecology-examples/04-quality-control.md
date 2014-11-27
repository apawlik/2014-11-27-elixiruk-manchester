---
layout: lesson
root: ../../..
title: "Basic quality control and data manipulation in spreadsheets"
---



Authors:**Christie Bahlai**, **Aleksandra Pawlik**<br>
Contributors: **Jennifer Bryan**, **Alexander Duryee**, **Jeffrey Hollister**, **Daisie Huang**, **Owen Jones**,**Ben Marwick**, and **Sebastian Kupny**

When you have a well-structured data table, you can use several simple techniques within your spreadsheet to ensure the data you’ve entered is free of errors. 

**Tip!** *Before doing any quality control operations, save your original file with the formulas and a name indicating it is the original data. Create a separate file with appropriate naming and versioning, and ensure your data is stored as “values” and not as formulas.  Because formulas refer to other cells, and you may be moving cells around, you may compromise the integrity of your data if you do not take this step!*

**readMe files:** As you start manipulating your data files, create a readMe document / text file to keep track of your files and document your manipulations so that they may be easily understood and replicated, either by your future self or by an independent researcher. Your readMe file should document all of the files in your data set (including documentation), describe their content and format, and lay out the organizing principles of folders and subfolders. For each of the separate files listed, it is a good idea to document the manipulations or analyses that were carried out on those data.


## Sorting ##
Bad values often sort to bottom or top of the column. For example, if your data should be numeric, then alphabetical and null data will group at the ends of the sorted data. Sort your data by each field, one at a time. Scan through each column, but pay the most attention to the top and the bottom of a column. 
If your dataset is well-structured and does not contain formulas, sorting should never affect the integrity of your dataset.

Example:
Let's try sorting on different columns in [soybean aphid suction trap dataset](../../../data/biology/aphid_data_Bahlai_2014.xlsx)

## Conditional formatting ##
Use with caution! But a great way to flag inconsistent values when entering data.



## Check on cell formats ##
A good way to check if you’ve got data of the wrong type in a column is by checking column format. This can also help prevent issues when you export your data.


Previous:[Dates as data.](03-dates-as-data.html) Next: [Exporting data from spreadsheets.](05-exporting-data.html)
