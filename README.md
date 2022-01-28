# PPS-Election
#include <stdio.h>

char C1[] = "Shreya";
char C2[] = "Aadith";
char C3[] = "Prisha";
char C4[] = "Lakshay";
char C5[] = "Kristen";
int vc1 = 0;
int vc2 = 0;
int vc3 = 0;
int vc4 = 0;
int vc5 = 0;
int invalid = 0;

void Voter_Choice()
{
    int choice;
    printf("Number 1: %s\n", C1);
    printf("Number 2: %s\n", C2);
    printf("Number 3: %s\n", C3);
    printf("Number 4: %s\n", C4);
    printf("Number 5: %s\n", C5);
    printf("Select any one candidate to vote from the names above:\n");
    scanf("%d", &choice);
    switch(choice)
    {
        case 1:
        vc1++;
        break;
        
        case 2:
        vc2++;
        break;
        
        case 3:
        vc3++;
        break;
        
        case 4:
        vc4++;
        break;
        
        case 5:
        vc5++;
        break;
        
        default:
        invalid++;
        printf("You have entered the wrong choice. Please try again. :(\n");
    }
    printf("Thank you for your choice :)\n");
    getchar();
}

void LeadingCandidate()
{
    if(vc1>vc2 && vc1>vc3 && vc1>vc4 && vc1>vc5)
    printf("Leading candidate is %s\n", C1);
  
    else if(vc2>vc1 && vc2>vc3 && vc2>vc4 && vc2>vc5)
    printf("Leading candidate is %s\n", C2);
  
    else if(vc3>vc1 && vc3>vc2 && vc3>vc4 && vc3>vc5)
    printf("Leading candidate is %s\n", C3);
  
    else if(vc4>vc1 && vc4>vc2 && vc4>vc3 && vc4>vc5)
    printf("Leading candidate is %s\n", C4);
  
    else if(vc5>vc1 && vc5>vc2 && vc5>vc4 && vc5>vc3)
    printf("Leading candidate is %s\n", C5);
    
    else
    printf("Winning cannot be determined cuz its a TIE!!!\n");
}

void No_of_votes()
{
    printf("The respective number of votes for each candidate is given below\n");
    printf("1. %s : %d\n", C1, vc1);
    printf("2. %s : %d\n", C2, vc2);
    printf("3. %s : %d\n", C3, vc3);
    printf("4. %s : %d\n", C4, vc4);
    printf("5. %s : %d\n", C5, vc5);
}

int main()
{
    for(int i = 0; i>=0; i++)
    {
        printf("Welcome to SRM Online BioPresident Voting\n");
        printf("These are the Respective Candidates contesting:\n");
        
        Voter_Choice();
        LeadingCandidate();
        No_of_votes();
    }
    return 0;
}
