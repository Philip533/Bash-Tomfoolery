Checks if a directory exists and creates it if it doesn't exist.

**[ ! -d "DIRECTORY" ] && mkdir DIRECTORY** or **test -d "DIRECTORY" && mkdir DIRECTORY

Counts how many lines are in a file and outputs it to terminal.

**wc -l file**

Loop over chosen set of numbers with given interval

**for i in $(seq start step end); do** or ** for (( i=0 ; i<5 ; i++ ))**

**commands here**

**done**

Arithmetic stuff using bc + pipe, performs operation to 10dp

**x = $(echo "scale = 10; 5 * 4" | bc)**

Combining operations

**list;list1 - run list then list 1**

**list & list1 - Execute list in background subshell and also execute list1**

**list && list1 - Execute list then execute list1 only if list returns 0**

**list || list1 - Execute list then execute list1 only if list returns non-zero**

Check STDIN condition

[[ -t 0 ]]

Pattern matched conditionals

case word in
  * pattern)
    * list;;
  * pattern1 | pattern 2)
    * list1;;
esac

Parameter Expansion

**${param?error} - Returns error if param is unset**

**{$param:offset:length} - Extracts substring from param**

**{$param#pattern} - Removes pattern from left edge**

**{$paaram%pattern} - Removes pattern from right edge**

**${#param} - Expand parameter length**

Pattern Substitution

**${param/pattern/string} - Simple pattern substitution of first occurrence**

**${param//pattern/string} - Simple pattern substitution of all occurrences**

**${param/#pattern/string} - Simple pattern substitution from left edge**

**${param/%pattern/string} - Simple pattern substitution from right edge**

Positional Parameters

**$# - Prints out the amount of parameters**

**$\* - Prints out the parameters on one line**

**$@ - Prints out the parameters on new lines**

Arrays

**array=(zero one two three "four five") - Assign an array by elements**

**array+=("six seven" [0] = ZERO) - Add an element or modify an element**

**echo ${!array[@]} - Print array indices**

**array=("${array[@]:2:3}") - Recreate array with indices 2 to 4**

Associative Arrays

**declare -A array=( [item] = 1 [item1] = 2 - Create an array using names for indices**

**echo "${array[@]}" - List items in array**

**echo "${!array[@]}" - List item keys in array**

Select parameter from a list of choices

**select choice in one two "three four"** 
**do**

**echo "$REPLY : $choice"**

**done**

Subshells

**(x=hello; echo "x: $x") - Run group of commands in a subshell which will have local variables**

**{ x=hello; echo "x: $x"; } - Runs group of commands in a subshell which will have global variables**

