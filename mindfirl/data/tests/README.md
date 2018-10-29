# README

- The test samples can be found in this directory. 
- The test files are named test\_{test-no}\_sample\_{file-no}.csv. File number corresponds to the two files to be uploaded. There is also a test\_{test-no}\_sample\_pair.csv that has the groups from which the individual files were made. 
- In a way, the pair file represents the ideal grouping but such a grouping cannot be achived by exact matching methods. 
- However, we try to get all the groups by repeatedly blocking.
- This file would also contain the groups for various blocking variables. 

# Samples

## Sample 2

### Raw (ideal: 5 groups, 10 pairs)

ID,voter_reg_num,first_name,last_name,dob,sex,race
146,1000153844,KEVIN,RANDALL,08/31/1951,M,W
146,1001039939,KEVIN,PURCELL,08/31/1951,M,

223,1063209897,BAKRI,ABDEL-AZIZ SR,03/26/1965,M,O
223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O
223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O

333,,MARY DELL,BAKER,04/08/1928,F,W
333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W

358,,W RICHARD,ARCILESI JR,01/30/1957,M,W
358,1015248678,WILLIAM,ARCILESI JR,01/30/1917,M,W

87,1075008084,ERNIE,SHORE III,12/17/1959,M,W
87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W

### voter_reg_num (correct: 3/5 groups, 3/10 pairs | wrong: 1 pair)

223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O
223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O

333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W

358,,W RICHARD,ARCILESI JR,01/30/1957,M,W
333,,MARY DELL,BAKER,04/08/1928,F,W

87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W


### first_name (correct: 4/5 groups, 4/10 pairs | wrong: 1 pair)

146,1000153844,KEVIN,RANDALL,08/31/1951,M,W
146,1001039939,KEVIN,PURCELL,08/31/1951,M,

223,1063209897,BAKRI,ABDEL-AZIZ SR,03/26/1965,M,O
223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O

223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O
333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W

87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W


### last_name (correct: 4/5 groups, 5/10 pairs | wrong: 0 pairs)

223,1063209897,BAKRI,ABDEL-AZIZ SR,03/26/1965,M,O
223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O
223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O

333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W

358,,W RICHARD,ARCILESI JR,01/30/1957,M,W
358,1015248678,WILLIAM,ARCILESI JR,01/30/1917,M,W

87,1075008084,ERNIE,SHORE III,12/17/1959,M,W
87,1705008084,ERNEST,SHORE III,12/17/1959,M,W

### sex (grouping too big)

146,1000153844,KEVIN,RANDALL,08/31/1951,M,W
146,1001039939,KEVIN,PURCELL,08/31/1951,M,
223,1063209897,BAKRI,ABDEL-AZIZ SR,03/26/1965,M,O
223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O
223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O
358,,W RICHARD,ARCILESI JR,01/30/1957,M,W
358,1015248678,WILLIAM,ARCILESI JR,01/30/1917,M,W
87,1075008084,ERNIE,SHORE III,12/17/1959,M,W
87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W

333,,MARY DELL,BAKER,04/08/1928,F,W
333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W

### race (grouping too big)

146,1000153844,KEVIN,RANDALL,08/31/1951,M,W
333,,MARY DELL,BAKER,04/08/1928,F,W
333,1000295504,BAKER,MARY DELL,04/08/1928,F,W
333_d,1000295504,BAKER,MARY DELL,04/08/1982,F,W
358,,W RICHARD,ARCILESI JR,01/30/1957,M,W
358,1015248678,WILLIAM,ARCILESI JR,01/30/1917,M,W
87,1075008084,ERNIE,SHORE III,12/17/1959,M,W
87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W

223,1063209897,BAKRI,ABDEL-AZIZ SR,03/26/1965,M,O
223,1100128569,BAKRI,ABDEL-AZIZ SR,03/26/1915,M,O
223_d,1100128569,BAKER,ABDEL-AZIZ SR,04/08/1982,M,O

### date (correct: 3/5 groups, 4/10 pairs | wrong: 0 pairs)


146,1000153844,KEVIN,RANDALL,08/31/1951,M,W
146,1001039939,KEVIN,PURCELL,08/31/1951,M,

333,,MARY DELL,BAKER,04/08/1928,F,W
333,1000295504,BAKER,MARY DELL,04/08/1928,F,W

87,1075008084,ERNIE,SHORE III,12/17/1959,M,W
87,1705008084,ERNEST,SHORE III,12/17/1959,M,W
87_d,1705008084,ERNEST,SHORE,12/17/1959,M,W