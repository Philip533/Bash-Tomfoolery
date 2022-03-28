Checks if a directory exists and creates it if it doesn't exist.

**[ ! -d "BLOCKED_AVERAGES" ] && mkdir BLOCKED_AVERAGES**

Counts how many lines are in a file and outputs it to terminal.

**wc -l file**

Loop over chosen set of numbers with given interval

**for i in $(seq start step end); do**

**commands here**

**done**

Arithmetic stuff using bc + pipe, performs operation to 10dp

x = `echo "scale = 10; 5 * 4" | bc`



