# Tcl String Comparison Bug

This repository demonstrates a subtle bug in a Tcl procedure that incorrectly handles string comparisons. The `badproc` procedure intends to compare two values and return 0 if they are equal and 1 if they are not. However, due to Tcl's dynamic typing and how string comparisons work, it produces unexpected results when comparing non-numeric strings that happen to be lexicographically equal but represented differently (e.g., "1" vs 1).