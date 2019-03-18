README -- "Heroes of Pymoli"

Summary:
The requested data analysis and report are found in the Jupyter
Notebook file "Analysis of Heroes of Pymoli (final).jpynb".  The notebook
includes both text commentary and a copy of all the analysis
operations undertaken.  In order to run the operations correctly,
the input data file "purchase_data.csv" must be located in a 
folder called "Resources" within the directory containing the
notebook.  

Detailed design doc:

Objective:  A reproducible analysis and informative summary
report of key player purchasing trends based on observed
user behavior in the game "Heroes of Pymoli".

Rationale: A better understanding of purchasing behavior will
enable improved financial performance through optimization of
the user experience.  Insights from the analysis need to be
communicated in a simple and clear manner so that designers
and developers can use them productively in updating the
environment.  

General Procedure: 
R) Import data to dataframe 
C) Pre-process and clean data (if needed)
A) Analysis -- purchase characteristics & demographic effects
Reporting will be done interactively with notebook tables.

Detailed Procedures / Notebook Cells:
Title cell:  -- includes key findings and requierments for
reproducing the analysis
Task R) -- import
Cell 1 (R):  	set-up (dependencies and file import)
Task C) -- clean
Cell 2 (C1):  	display sample of input data
Text cell:  	introduce the data, state the expectation that data is clean
Cell 3 (C2): 	count missing values in data columns, expected to display zeros
Cell 4 (C3):  	display data types to ensure they are appropriate for analysis
Text cell:  	explain that the data is clean and ready to go
Task A) -- analyze
Text cell:	introduce analysis and summary table
Cell 5 (A1):	generate descriptive statistics:  total players, total items,
		average price, total purchases, and total revenue.
Text cell:	comment on the statistics -- sample sizes
Text cell:      introduce analysis by gender
Cell 6 (A2):	generate:  total players, percent of players, grouped by gender
Text cell: 	comment on results 
Text cell: 	introduce purchase characteristics by gender
Cell 7 (A3):	generate:  number of purchases, average purchase amount, total
		spent, and average spent per player, grouped by gender
Text cell:      comment on results (predominance and any differences in buying habits)
Text cell:	introduce age-group analysis (5-yr co-horts)
Cell 8 (A4):	generate:  total players and percent of players, grouped by age
Cell 9 (A5):	generate:  number of purchases, average purchase amount, total
		spent, and average spent per player, grouped by age-group
Text cell:   	comment on results (which age groups buy the most)
Text cell:	introduce discussion of exceptional characteristics, top spenders
Cell 10 (A6):	generate:  player name, items purchased, average price per item, and
		total spent, grouped by player name, then sorted by total spent and
		displayed as top 5
Text cell:	comment on the variance (how much of a multiple of average was spent)
Text cell:	introduce top items by times purchased
Cell 11 (A7):	generate:  item ID, item name, times purchased, price, and total 
		revenue, grouped by item ID, then sorted by times purchased and displayed
		as top 5
Text cell:	comment on the variance
Text cell:	introduce top items by revenue generated
Cell 12 (A8):	generate:  item ID, item name, times purchased, price, and total
		revenue, grouped by item ID, then sorted by total revenue and displayed
		as top 5
Text cell:	comment on the variance, and on similarities between the top 5 by 
		popularity and revenue

Design Notes:
1.  For A1, the data are generated as single variables, which lets them be formatted in
    one step.  The data table can then be built using a DataFrame generator with a dictionary
2.  For A2, a straightforward groupby will build the DataFrame, with a simple derived Series 
    appended
3.  For A3 and A5-A8, the DataFrame is first built with the .agg method and a dictionary
    of column names and functions, to cover the straightforward cases (sums, means, counts). 
    Because the resulting DataTable has only a few columns, the easiest way to fix the Multi-
    Index for diplay and reference purchases is a direct re-wirte of column names.  Derived
    columns (e.g. amount spent per player) can then be appended one at a time as needed.
4.  For A4, pd.cuts is used to append the age group Series to the original DataFrame.  Doing
    so simplifies A5, where groupby age-group will be needed once again. The output table is
    then built in exactly the same manner as A2, but with age-group substitued for gender.  
5.  Overall, this approach is clean, simple, and easy to extend.  The main limitation is
    the direct re-write of column names for data tables to clean up the MultiIndex,
    which would need to be autoamted (can be done with get_levels and string concatenation) if 
    there were a large number of columns.  Because this issue is mainly a formatting one for
    displaying tables read by human beings, it seems safe to assume there won't ever be a
    very large number of columns that would need to be handled this way.  





