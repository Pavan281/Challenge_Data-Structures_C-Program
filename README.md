# Challenge_Data-Structures_C-Program
# Write a C program that defines a structure employee containing the details

#include <stdio.h>
#include <stdlib.h>
typedef struct {
    char name[30];
    int age, phonenumber;
    double salary;
}Employee;
 
int main()
{
    //number of employees
    int n=3;
    //array to store structure values of all employees
    Employee employees[n];
    //Taking each employee detail as input
    printf("Enter %d Employee Details \n \n",n);
    for(int i=0; i<n; i++){
        printf("Employee %d:- \n",i+1);

        //Name
        printf("NAME: ");
        scanf("%[^\n]s",employees[i].name);

        //AGE
        printf("AGE: ");
        scanf("%d",&employees[i].age);
        
        //PHONE NUMBER
        printf("PHONE NUMBER: ");
        scanf("%d",&employees[i].phonenumber);

        //Salary
        printf("SALARY: ");
        scanf("%lf",&employees[i].salary);
        //to consume extra '\n' input
        char ch = getchar();
        printf("\n");
    }
    //Displaying Employee details
    printf("All Employees Details are here \n");
    for(int i=0; i<n; i++){
        printf("NAME : ");
        printf("%s \n",employees[i].name);
 
        printf("AGE : ");
        printf("%d \n",employees[i].age);
        
        printf("PHONE NUMBER : ");
        printf("%d \n",employees[i].phonenumber);
 
        printf("SALARY : ");
        printf("%.2lf \n",employees[i].salary);
 
        printf("\n");
    }
    return 0;
}
