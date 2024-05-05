# Ex-1-NFA-to-DFA
## Aim
To write a C program for Conversion of Non-Deterministic Finite Automaton (NFA) To 
Deterministic Finite Automaton (DFA).
# ALGORITHM
Step 1 : Take ∈ closure for the beginning state of NFA as beginning state of DFA. 

Step 2 : Find the states that can be traversed from the present for each input symbol. 

Step 3 : If any new state is found take it as current state and repeat step 2. 

Step 4 : Do repeat Step 2 and Step 3 until no new state present in DFA transition table. 

Step 5 : Mark the states of DFA which contains final state of NFA as final states of DFA.
# PROGRAM
~~~
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
// To find new Closure States
void state(int ar[], int size, char S[]) {
 int j, k = 0;
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
// Check new DFA states can be
// entered in DFA table or not
int indexing(struct DFA *dfa) {
 int i;
 for (i = 0; i < last_index; i++) {
 if (dfa[i].count == 0)
 return 1;
 }
 return -1;
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
 // call the check function
 check(closure_ar, buffer);
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
 // push the new
 strcpy(&dfa[last_index++].states, S);
 // set the count for new states entered
 // to zero
 dfa[last_index - 1].count = 0;
 return 1;
}
// (generally union of closure operation )
void trans(char S[], int M, char *clsr_t[], int st,char *NFT[][symbols + 1], char TB[]) {
 int len = strlen(S);
 int i, j, k, g;
 int arr[st];
 int sz;
 reset(arr, st);
 char temp[MAX_LEN], temp2[MAX_LEN];
 char *buff;
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
 }
 bzero((void *)temp, MAX_LEN);
 state(arr, st, temp);
 if (temp[0] != '\0') {
 strcpy(TB, temp);
 } else
 strcpy(TB, "-");
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
 printf("STATES\t");
 for (i = 0; i < symbols; i++)
 printf("|%d\t", i);
 printf("eps\n");
 printf("\n");
 }
 // Till new states can be entered in DFA table
 while (ind != -1) {
 dfa_states[start_index].count = 1;
 strcpy(buffer, &dfa_states[++start_index].states);
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

