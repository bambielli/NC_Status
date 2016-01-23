
### README

This is the README file for the NC_Status app

Created by: Brian Ambielli
Date: Dec 21, 2014

###Purpose:

This app was designed to bring visibility to the quantity and types of Non-Conformances generated in manufacturing.

It works by pinging each of the NC folders to see what files are inside of each. It then does some string processing on the names of the files to determine if the file is a System NC (ends with an -S) or a component NC (ends with a -C). It tallies the number of System and component NCs in each folder, then generates a table with the counts for each type and a total number for each folder. It then creates a global count for the total number of component and system NCs and displays those as totals.

Currently, to get updates on numbers of NCs, the user would either have to re-open the App, or click the "refresh numbers" button at the top.

### Design Assumption
This app works under the assumption that NCs will be saved in the NC folders with the following format:

XXXNCRY12345-Z

XXX -> year and quarter that the NC was generated
NCR -> standard text that the program looks for to tell that the file is an NC
Y -> the type of NC generated
12345 -> the number of that type of NC for this quarter
-Z -> either an S or a C, which tells the app that the NC is either a system or component NC

Current situation that the app does not take in to account, is if the file is saved with a -SC or a -CS, which indicates that the NC is both a system and component NC. Can fix this in future versions.

### Disclaimer
This app was written over the course of a few days, and is in NO way optimized or DRY.
