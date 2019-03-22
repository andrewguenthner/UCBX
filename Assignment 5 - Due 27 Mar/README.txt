Pymaceutical Squamous Cell Carcinoma Candidate Study
Presentation of Results

Expected Product:  a set of graphs summarizing key trial results 
(tumor volume, metastatic spread, and survival) from mouse data
for the latest series of drug candidates.  The graphs should 
be understandable by a broad audience, but retain enough detail
to facilitate in-depth technical discussion and presentation.

Rationale:  Now that the trials are complete, communiccating
the results effectively becomes the key factor in realizing
full value.  The Chief Data Analyst is best suited to ensure key
technical featuers are retained while understanding approach
needed to effectively communicate to a broad audience.

General Procedure:
We want one graph, one per story element, with three elements and
a summary combined to make an easily-digested story.  In this
case, we have three key performance indicators, so each graph
will provide an intuitively understandable comparison of how
candidates performed in each indicator.  The summary will
use color coding and a simpler form to drive home the main points,
and will be designed to be presented either first, last, or
standalone with respect to the other graphs.  The three key
elements will used shared visual elements to tie them together,
though they will be built to be presented in any combination.  To
make the presentation easier to follow, only the data for the
three most viable candidates (and placebo) will be presented.

S.  Summary plot
A1.  Key element:  tumor volume
A2.  Key element:  metastatic spread
A3.  Key element:  survival 

Detailed design
S.  Summary plot
Type = bar chart
Bars = one per drug candidate, include placebo
Error-bars = yes
Axes, x = labeled drug name (include placebo, at left)
y = tumor volume reduction as % (most important indicator, up = greater 
reduction (better performance is always 'up')
color = green if tumors shrink, red if they don't
labels on bars = value to nearest % 
title = main point: promising results from capomulin -- put the
attention-getting part first 

A1.  Tumor volume plot
Type = scatter plot
Series = one series per drug, include placebo
Error-bars = yes
Axes, x = time in days
y = tumor volume in mm^3 (up = higher volume, keep it logical)
color = neutral sequence (placebo = black), match A2, A3
labels on points = no
legend = drug names
title = main point

A2.  Metastatic spread plot
Type = scatter plot
Series = one series per drug, include placebo
Error-bars = yes
Axes, x = time in days
y = metastatic sites (#) (up = higher volume, keep it logical)
color = neutral sequence (placebo = black), match A1, A3
labels on points = no
legend = drug names
title = main point

A1.  Survival plot
Type = scatter plot
Series = one series per drug, include placebo
Error-bars = yes
Axes, x = time in days
y = survival rate in % (up = higher)
color = neutral sequence (placebo = black), same as A1, A2
labels on points = no
legend = drug names
title = main point

