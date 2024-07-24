# pandas-challenge

The Jupyter Notebook file which contains my code for this challenge can be found in the file titled `PyCitySchoolsWorking.ipynb`, located in the `PyCitySchools` folder.

The written analysis component of this challenge can be found in the first cell of the `PyCitySchoolsWorking.ipynb` file.

The source code that was included with the resources for this challenge, titled `PyCitySchools_starter.ipynb`, and the in-class activites were the main resources I used to write the needed code for this challenge.

The only place where I had to stray from the source code a bit was in the "Scores by School Spending" category. I encountered an issue in the "Per Student Budget" column, where numerical dollar amounts had been formatted as strings with a dollar sign in front. I had to find a way to convert this back to a float in order for binning to work properly. I asked ChatGPT for help here, and it suggested I use the line `.replace({r'\$': '', ',': ''}, regex=True)`. I was unfamiliar with the `r` being put in front of the argument of the `.replace` function, which serves to treat the backslashes as normal characters rather than escape characters. I was also unfamiliar with the `regex=True` argument, which makes this function replace all instances of the `$` character and the `,` character. This solution worked to resolve the issue. I have added comments in the code to highlight this change.