- 👋 Hi, I’m @sithumabeyrathne
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
sithumabeyrathne/sithumabeyrathne is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
eco
#include <stdio.h>
int main (void)
{
int i, no;
FILE *cfPtr; //Create file pointer
cfPtr = fopen("numbers.txt", "w"); //Create and open file for writing
if ( cfPtr == NULL)
{
printf("Fail to create file\n");
return -1;
}
for(i = 1; i <= 5; i++)
{
printf("Enter integer number : ");
scanf("%d", &no);
fprintf(cfPtr, "%d\n", no); //Write numbers to the file
}
fclose(cfPtr);
cfPtr = fopen("numbers.txt", "r"); //Open file for reading
fscanf(cfPtr, "%d", &no); //Read numbers from the file
while(!feof(cfPtr))
{
printf("%d\t", no);
fscanf(cfPtr, "%d", &no); //Read numbers from the file
}
fclose(cfPtr);
return 0;
} 
