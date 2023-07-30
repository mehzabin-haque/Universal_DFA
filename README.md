## Universal DFA

Discover the implementation of a Universal Deterministic Finite Automaton capable of simulating other DFAs. This concept plays a significant role in language recognition and computation theory.
This C++ code represents a Universal Deterministic Finite Automaton (DFA) that accepts or rejects strings based on a given set of states, transitions, and final states. The program takes input for the number of states, start state, final states, and transition functions for input symbols '0' and '1'. It then prompts the user to enter a string, which will be checked for acceptance or rejection by the DFA.

### Explanation with an example:

  Let's assume we have the following DFA:
  ```
  Number of states (Q): 3
  Start state (q0): 1
  Number of final states (f): 1
  Final state(s) (F): 3
  Transition table:
  1 --> 0 --> 2
  1 --> 1 --> 3
  2 --> 0 --> 2
  2 --> 1 --> 2
  3 --> 0 --> 3
  3 --> 1 --> 2
  ```
  The DFA diagram:
  ```
         0       1
     --> 2  <--  1 (Start, Final)
       ^  |       |
       |  V       V
       3 <--  2 (Final)
  ```
  
  Now, suppose we want to check the string "101" for acceptance:
  
  1. The program will start from the start state, i.e., state 1.
  2. It will read the first symbol '1', transitioning from state 1 to state 3.
  3. Next, it reads the symbol '0', transitioning from state 3 to state 3.
  4. Finally, it reads the last symbol '1', transitioning from state 3 to state 2.
  
  After processing the entire string, the DFA ends at state 2.
  
  Output:
  ```
  Steps are :
  Start --> 1 --> (1 ) --> 3 --> (0 ) --> 3 --> (1 ) --> 2
  
  String is accepted
  ```
  
  The program displays the steps taken while processing the string. In this case, the DFA ends up in one of the final states (state 2), so the string "101" is accepted.

----
