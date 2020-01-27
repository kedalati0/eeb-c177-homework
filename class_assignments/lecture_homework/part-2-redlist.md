##1 tail -n +2 European_Red_List.csv | cut -d "," -f 10 | sort -n | uniq -c
    456 CR
      8 CR (PE)
   2409 DD
    687 EN
      4 EW
     29 EX
   5805 LC
    411 NA
      4 NE
    964 NT
      8 RE
    885 VU


##2tail -n +2 European_Red_List.csv | cut -d "," -f 4,10 | sort -n | uniq -c 
## | head -n +23 | tail -n 7
     10 AVES,CR
     18 AVES,EN
      2 AVES,EX
    428 AVES,LC
     32 AVES,NT
      4 AVES,RE
     39 AVES,VU

##3 for the RE or CE we have
## tail -n +2 European_Red_List.csv | cut -d "," -f 4-10 | grep -w "AVES" 
## | cut -d "," -f 2,7 | uniq -c | sort -n | grep -e ",CE\|,RE"
      1 CHARADRIIFORMES,RE
      1 PASSERIFORMES,RE
      1 PELECANIFORMES,RE
      1 SULIFORMES,RE
## for EX in order
## tail -n +2 European_Red_List.csv | cut -d "," -f 4-10 | grep -w "AVES" 
## | cut -d "," -f 2,7 | uniq -c | sort -n | grep -e ",EX"
      1 CHARADRIIFORMES,EX
      1 CHARADRIIFORMES,EX
	
