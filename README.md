# Elixir Enum.each and Process.exit Bug

This repository demonstrates a potential issue when using `Process.exit` within an `Enum.each` loop in Elixir. The example code attempts to iterate through a list and print each element, but terminates the process if a specific element is encountered.

This behavior can lead to unexpected program termination and missed operations. The solution showcases a safer approach to handle such situations, preventing premature process exits.

## Bug
The bug lies in the use of `Process.exit` within `Enum.each`.  If the condition `x == 3` is met, the current process exits, interrupting the loop prematurely. 

## Solution
The solution demonstrates an alternative approach using a conditional statement within the loop that prevents the process from terminating early.