#include<stdio.h>

#include<stdlib.h>

#include<conio.h>

#include<string.h>

#include<ctype.h>

void main()

{

int flag,i=1,m;

char a[10], s[32][10]={"if","else","goto","continue","return","auto","double",

 "int","struct", "break","long","switch","case","enum",

 "register","typedef","char","extern","union","const",

 "float","short","unsigned","sizeof","volatile","for",

 "signed","void","default","do","static","while" };



printf("\n Enter an String to find that it is an Identifier or Keyword :: \n");

scanf("%s",a);

for(i=0;i<32;i++)

{

m=strcmp(a,s[i]);

if(m==0)

flag=1;

}

if(flag==0)

{

 printf("\n It is not a keyword");

 if(isalpha(a[0])||a[0]=='_')

flag=1;

else

{
printf("\n Invalid identifier");

exit(1);

}

while(a[i]!='\0')

{

if(!isdigit(a[i])&& !isalpha(a[i])|| a[i]=='_')

{

flag=1;

break;

}i++;

}

if(flag==1)

printf("\n Valid identifier");



}

else

printf("\n It is a keyword, So it can't be an identifier"); 

getch();

}
