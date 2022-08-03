# upside-down-word
# c program
# *이전까지 입력받은 문자를 거꾸로 출력하되 모음이 있다면 포인터를 이용해서 한번 더 출력하도록 한다! * Print the previously entered characters backwards, but if there is a vowel, use a pointer to print it again!
#include <stdio.h>
int main(void)
{
    char s[100];
    char *p;
    int i=0;
    printf("입력:");
    scanf("%c",s);
    while(*(s+i)!='*'){ //마지막이 *로 끝나때까지 입력  
    	i++;
    	scanf("%c",s+i);	
    }
    for(p=(s+i-1);p>=s;p--){ //거꾸로 출력  
        printf("%c",*p);
    	if(*p=='a'||*p=='e'||*p=='i'||*p=='o'||*p=='u'){
    		printf("%c",*p);
		}
	}
	printf("*");
    return 0; 
}
#input--> abc*
#result--> cbaa*
