The inbuilt python libraries used are 
import csv
import sys
from functools import reduce
from operator import itemgetter

My approach of solving the problem is from map-reduce
using the reduce from functools

I have three higher higher order functions which are:

transform(x) that transforms the input file stored as dictionary to dictionary with only necessary columns i.e.

'id'	 'drug_name'	 'drug_cost'

The table somewhat looks like this.
These are only the field we require.
with id as unique identifier to prescribers.

After the transformation, we want to reduce the dictionary with unique drugs only which is mapped to tuple consisting of list of prescribers using that drug and total revenue for that drug.

After the reduce we want to map the dictionary into a data structure so that we can write to file with list of prescriber for a drug to set so that only unique prescriber is obtanied.




For generating the test case random 20 rows are selected from file conatining 24 million records using following command in linux terminal.

shuf -n 20 de_cc_data.txt > input[n].txt

I have generated 4 test files
