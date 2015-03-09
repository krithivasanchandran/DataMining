# DataMining

###DataSet

Our transaction database is a set of reviewers from Amazon.com. Specifically, reviewer ids are our items. The transaction is a set
of reviewer ids. Specifically, all reviewer ids which were used to post a review on that product. The format of the transaction
database follows the standard format seen in class. Each line represents a transaction. For a given transaction, the items (reviewer	ids) are separated by a space character. 

###Data Pre-Processing
	
For pattern mining, one usually requires frequent itemset candidate generation and that is done based on the total
ordering of elements of previous lower order frequent itemsets . Since comparing strings is more expensive than integers, you will be at an advantage if you map all unique reviewer ids to intergers and
convert the transaction database above to set of transaction with integers as items.
	
###Implementation

Mining frequent k+ items sets whose value is greater than minimum support count(minimum_support). . A frequent k+ itemset refer to an itemset
whose size is k (i.e., it has k elements) and the support of that itemset (no. of times that itemset appears in the transaction database)
exceeds minimum_support count. Frequent k+ itemsets refers to all frequent itemsets (i.e., itemsets appearing more than min_supp times in the data) which have sizes greater than k.  

### Examples
1. min_sup=4, k= 3
	```
		A37787I8C184FW AWE8HU0AZKASV A3UIATN5XW74NQ (4)
		A3Y9BX5AS769T AWE8HU0AZKASV A3UIATN5XW74NQ (5)
		AZ7I5GAJZA3JO A28R83ADQPMF2X A2GKW94L6HRND7 A2IE7YPWUYZAXS (4)
  ```
  
2. min_sup=5, k= 3
  ```
		A9TJYY7P2R280 A2S9IDC1IZH7WN AYFQ8ML2PYZ1D (5)
		A3PXX92YUMGMBG A3UIATN5XW74NQ AWE8HU0AZKASV (5)
		A2J96R1J6MDMEV A3UIATN5XW74NQ AWE8HU0AZKASV (5)
		A3Y9BX5AS769T A3UIATN5XW74NQ AWE8HU0AZKASV (5)
	```
	
3. min_sup=8, k =2
	```
		A20JYIHL1W1U54 A7Y6AVS576M03 (10)
		AO2V6YDDYQ2CR A5JLAU2ARJ0BO (8)
		A2AEZQ3DGBBLPR A231WM2Z2JL0U3 (8)
		A231WM2Z2JL0U3 A5JLAU2ARJ0BO (11)
	```
	
4. min_sup=7, k =2
	```
		A20JYIHL1W1U54 A7Y6AVS576M03 (10)
		AO2V6YDDYQ2CR A5JLAU2ARJ0BO (8)
		A39KIFR965H0CX A1MJMYLRTZ76ZX (7)
		A1C9C1QOQB94RT A15S4XW3CRISZ5 (7)
		A1E7QLJVWNFOZY A2ZM9BGE3K3SY2 (7)
		A2AEZQ3DGBBLPR A231WM2Z2JL0U3 (8)
		A3PPXFIVMJ9MV8 AUPUZ14778SD7 (7)
		A231WM2Z2JL0U3 A5JLAU2ARJ0BO (11)
	```
5. min_sup=10, k =2
	```
		A20JYIHL1W1U54 A7Y6AVS576M03 (10)
		A231WM2Z2JL0U3 A5JLAU2ARJ0BO (11)
	```
	
6. min_sup=75, k=1
	```
		A2A10ZSC2RH4RG (629)
		A25HBO5V8S8SEA (159)
		AT6CZDCP4TRGA (87)
		A2CL818RN52NWN (81)
		A2B7BUH8834Y6M (147)
		A2AEZQ3DGBBLPR (91)
		A2ZM9BGE3K3SY2 (92)
		A231WM2Z2JL0U3 (209)
		A5JLAU2ARJ0BO (323)
	```
	
### Execution:
	
```
$> java CandidateKeys min_sup k input_transaction_file_path output_file_path
```
input_transaction_file_path - https://github.com/krithivasanchandran/DataMining/blob/master/Amazon_transactionDB.txt
output_file_path - Any valid output file directory where the file will be produced.
	
###Sample Output Files:
```
https://github.com/krithivasanchandran/DataMining/tree/master/Output
```
	
