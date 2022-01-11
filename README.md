#include <stdio.h>
# include <string.h>
int main() {
    FILE *filePointer ;
    filePointer = fopen("ct4.c", "w") ;
    
    if ( filePointer == NULL )
    {
        printf( "ct4.c file failed to open." ) ;
    }
    printf("Enter your choice for menu\n");
    
    printf("\n 1. Book a Room\n");
    
    printf("\n 2. Exit\n");
    int n;
    scanf("%d",&n);
    
    if(n==1)
    {
        printf("Enter room no\n");
        int rn;
        fscanf(filePointer,"%d",&rn);
        
        printf("Enter Name\n");
        char name[25];
        fscanf(filePointer,"%s",name);
        
        printf("Enter address\n");
        char add[50];
        fscanf(filePointer,"%s",add);
        
        printf("Enter your phone no. \n");
        int ph;
        fscanf(filePointer,"%d",&ph);
        
        printf("Nationality\n");
        char nat[20];
        fscanf(filePointer,"%s",nat);
        
        printf("Period\n"); //no of days you want to stay 
        int p;
        fscanf(filePointer,"%d",&p);
        
        printf("room no %d booked for %d days\n",rn,p);
        fclose(filePointer) ;
    }
    
    else if (n==2)
    printf("Thank you");
    
    
    return 0;
}
