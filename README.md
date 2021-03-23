# Function3
Function3
### 1
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[])
{
    int num, fact; 
    
    if(argc != 2) {
        printf("Invalid Usage.\n\n");
        printf("Usage: ./a.out <number>\n");
        return 0;
    }

    num = atoi(argv[1]); 
    
    if(num<0) {
        printf("Error: Factorial of negative number doesn't exist.");
        return 1;
    }
    
    fact = 1; 
    
    while(num>1){ 
        fact = fact * num; 
        num--;
    }
    
    printf("%d\n", fact); 
    
    return 0;
}
### 2
#include <stdio.h>

int main(int argc, char *argv[])
{
	int a,b,sum;
	int i;
	
	if(argc<2)
	{
		printf("please use \"prg_name value1 value2 ... \"\n");
		return -1;
	}
	
	sum=0;
	for(i=1; i<argc; i++)
	{
		printf("arg[%2d]: %d\n",i,atoi(argv[i]));
		sum += atoi(argv[i]);
	}
	
	printf("SUM of all values: %d\n",sum);
	
	return 0;
}
### 3
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[])
{
    int i, length;

    for(i = 0; i<argc; i++)
    {
        length = strlen(argv[i]);
        printf("%s %d\n", argv[i], length);

        if(strlen(argv[i]) < strlen(argv[i+1]))
        {
            printf("%s is the biggest \n", argv[i+1]);
        }
        else
        {
            printf("%s is the biggest \n", argv[i]);
        }
    }
    return 0;
}
### 4
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(int argc, char* argv[]) {
    int i;
    for (i=0;i<argc; i++) {
        printf("argv[%d]: %s\n", i, argv[i]);
    }
    int result = 1;
    for (i=1;i<argc; i++) {
        int x = strtol(argv[i], NULL, 10);
        result = result * x;
    }
    printf ("Multiplication result us %d\n", result);
    return 0;
}
