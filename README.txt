Start AliasingScore app on MATLAB Command Line:
-----------------------------------------------

>> AliasingScore(model, tbl);

The input parameters are 'model', a SimBiology model, and 'tbl', a data 
table used for fitting. Remark: the data table must contain a column 
specifying groups, even if the data contains only one group.

Use AliasingScore app:
----------------------

The app has four panels:

 * Data Table
 ------------
   Display the data table 'tbl'.

 * Data Info
 ------------
   Edit column 'Data Association' to associate the data with a model 
      response, group variable and independent variable.
   Edit column 'Defines Dose' to specify if a data column defines a dose.
   Edit column 'Include in Aliasing Score' to specify which model response
      should be included in the aliasing score; this usually includes all
      measured responses.

 * Component Info
 ----------------
   Edit column 'Value' to change the values at which the aliasing score
      is computed.
   Edit column 'Include in Aliasing Score' to specify which model component
      should be included in the aliasing score; this usually includes all
      components to be fitted.

 * Aliasing Score
 ----------------
    The 'Simulate' button simulates the model and computes 
      the aliasing scores.
    Use the 'Response' selection to switch between plots for 
      different responses.
    Use the 'Show Aliasing Score For Current Response Only' to switch 
       between combined and response-wise aliasing scores.
    Use the 'Stop Time' field to change the simulation stop time.
    Use the 'Group' selection to switch between groups.
    Use the 'Percentage' field to specify the relative variation of 
       parameters used to compute finite difference approximations of 
       sensitivities. 
       Remark: for accurate finite difference approximations, the 
               percentage should be set to a small value. If the normalized
               response plots look asymmetric, then the finite difference 
               approximation is inaccurate.
    Use the 'Use Sensitivity for Aliasing Score' to switch between 
       Simbiology's builtin sensitivity analysis and finite difference 
       approximation for computing the aliasing score.
    Use the sliders to adjust the scan window used for the aliasing score.
    Use the 'Zoom' checkbox to zoom in and out of plots.
    Use the 'Use Data Times For Score' checkbox to only use measurement 
       times within the current scan window to compute the aliasing score.
