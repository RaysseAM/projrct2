#include <stdio.h>
#include <string.h>


int main()
{
     //c = number of students
    int n ;
     int note = 10;
      char name[50];
       int success = 0;
        int fail = 0;
         char c;




    printf("How many students are there? :");
      scanf("%d", &n);
       while ((c = getchar()) != '\n' && c != EOF);




    for(int i = 0; i < n; i++){
         printf("enter name of the student:", i + 1);
          fgets(name, sizeof(name), stdin);
            name[strlen(name) -1] = '\0';


        printf("enter note of student:", i + 1);
          scanf("%d", &note);
            while ((c = getchar()) != '\n' && c != EOF);


     if( note >= 10){
       printf("The student is Success :) \n");
       success++;
     }else{
       printf("The student is fail :( \n");
       fail++;
     }

    }

    printf("Total success: %d\n", success);
    printf("Total fail: %d\n", fail);



    return 0;
}
