~~~
 Ex-1-NFA-to-DFA
 Aim
To write a C program for Conversion of Non-Deterministic Finite Automaton (NFA) To 
Deterministic Finite Automaton (DFA).
 ALGORITHM
Step 1 : Take ∈ closure for the beginning state of NFA as beginning state of DFA. 
Step 2 : Find the states that can be traversed from the present for each input symbol. 
Step 3 : If any new state is found take it as current state and repeat step 2. 
Step 4 : Do repeat Step 2 and Step 3 until no new state present in DFA transition table. 
Step 5 : Mark the states of DFA which contains final state of NFA as final states of DFA.
 PROGRAM

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#define MAX_LEN 100
char NFA_FILE[MAX_LEN];
char buffer[MAX_LEN];
int zz = 0;
struct DFA {
 char *states;
 int count;
} dfa;
int last_index = 0;
FILE *fp;
int symbols;
// of the states which is found
 j = ((int)(S[i]) - 65);
 ar[j]++;
 }
}
// To pick the next closure from closure set
int closure(int ar[], int size) {
 int i;
 // check new closure is present or not
 for (i = 0; i < size; i++) {
 if (ar[i] == 1)
 return i;
 }
 return (100);
}
/* To Display epsilon closure*/
void Display_closure(int states, int closure_ar[],
 int i;
 for (i = 0; i < states; i++) {
 reset(closure_ar, states);
 // till closure get completely saturated
 while (z != 100)
 {
 	if (strcmp(&NFA_TABLE[z][symbols], "-") != 0) {
 strcpy(buffer, &NFA_TABLE[z][symbols]);
 }
 closure_ar[z]++;
 z = closure(closure_ar, states);
 }
 }
 // print the e closure for every states of NFA
 printf("\n e-Closure (%c) :\t", (char)(65 + i));
 bzero((void *)buffer, MAX_LEN);
 state(closure_ar, states, buffer);
 strcpy(&closure_table[i], buffer);
 printf("%s\n", &closure_table[i]);
 }
}
/* To check New States in DFA */
int new_states(struct DFA *dfa, char S[]) {
 int i;
 return 0;
 }
 // Transition function from NFA to DFA
 for (i = 0; i < len; i++) {
 j = ((int)(S[i] - 65));
 strcpy(temp, &NFT[j][M]);
 if (strcmp(temp, "-") != 0) {
 sz = strlen(temp);
 g = 0;
 while (g < sz) {
 k = ((int)(temp[g] - 65));
 strcpy(temp2, &clsr_t[k]);
 check(arr, temp2);
 g++;
 }
}
/* Display DFA transition state table*/
 void Display_DFA(int last_index, struct DFA *dfa_states,
 char *DFA_TABLE[][symbols]) {
 int i, j;
 printf("\n\n**\n\n");
 printf("STATES\t");
 // display the DFA transition state table
 printf("--------+-----------------------\n");
 for (i = 0; i < zz; i++) {
 printf("%s\t", &dfa_states[i + 1].states);
 for (j = 0; j < symbols; j++) {
 printf("|%s \t", &DFA_TABLE[i][j]);
 }
 printf("\n");
 }
}
 // Hard coded input for NFA table
 char *DFA_TABLE[MAX_LEN][symbols];
 strcpy(&NFA_TABLE[0][0], "FC");
 strcpy(&NFA_TABLE[0][1], "-");
 strcpy(&NFA_TABLE[0][2], "BF");
 printf("\n NFA STATE TRANSITION TABLE \n\n\n");
 printf("\n");
 }
 &dfa_states[++start_index].states);
 zz++;
 }
 // display the DFA TABLE
 Display_DFA(last_index, dfa_states, DFA_TABLE);
 return 0;
}
~~~
# OUTPUT 
![image](https://github.com/niranjanadevi-s/Ex-1-NFA-to-DFA/assets/141748873/7e5afd77-5d4a-4f73-b171-4b54397483c7)

# RESULT
The program was sucessfully converted from NFA to DFA.

