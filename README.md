int main(){
    int arr[100][100];
    int n;
    int m;
  
    int co_factor[100][100];
    printf("Enter number of rows and columns of matrix A: ");
    scanf("%d %d",&n,&m);
    
    for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
        
            scanf("%d",&arr[i][j]);
        }
    }
   
    co_factor[0][0]=((arr[1][1]*arr[2][2])-(arr[2][1]*arr[1][2]));
    co_factor[0][1]=((arr[1][0]*arr[2][2])-(arr[2][0]*arr[1][2]));
    co_factor[0][2]=((arr[1][0]*arr[2][1])-(arr[2][0]*arr[1][1]));
    co_factor[1][0]=((arr[0][1]*arr[2][2])-(arr[2][1]*arr[0][2]));
    co_factor[1][1]=((arr[0][0]*arr[2][2])-(arr[2][0]*arr[0][2]));
    co_factor[1][2]=((arr[0][0]*arr[2][1])-(arr[2][0]*arr[0][1]));
    co_factor[2][0]=((arr[0][1]*arr[1][2])-(arr[1][1]*arr[0][2]));
    co_factor[2][1]=((arr[0][0]*arr[1][2])-(arr[1][0]*arr[0][2]));
    co_factor[2][2]=((arr[0][0]*arr[1][1])-(arr[1][0]*arr[0][1]));

    printf("The resulted matrix A: \n");
    for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
            printf("%d ",co_factor[i][j]);
        }
        printf("\n");
    }
}


int main()
{
    int num1,num2;
    printf("enter the two number:");
    scanf("%d%d",&num1,&num2);
    switch(num1>num2)
    {
        case 0:
        printf("%d is maximum",num2);
        break;

        case 1:
        printf("%d is maximum",num1);
        break;
    }
    return 0;
}
