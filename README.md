# ordenando-lista
#include <stdio.h>  
#include <stdlib.h>
#include <time.h>   

void sortArray(int arr[], int size){
    int i,j,temp;
    for(i=0;i<size -1;i++){
        for(j=0;j<size -i -1;j++){
            if(arr[j]>arr[j+1]){
                temp=arr[j];
                arr[j]=arr[j+1];
                arr[j]=temp;
              }
          }
      }
          
}
int main(){
    int numbers[6];
    int i,j,num;
    srand(time(0));

    for (i=0;i<6;i++) {
       numbers[i] = rand()%50+1;
        for(j=0;j<i;j++){
            if (numbers[i]==numbers[j]){
                i--;
                break;
            }
        }
    }
    printf("numeros sorteados: ");
    for(i=0;i<6;i++){
        printf("%d ",numbers[i]);
    }
    sortArray(numbers,6);
    printf("\nnumeros sorteados em ordem crescente: ");
    for(i=0;i<6;i++){
        printf("%d ",numbers[i]);
    }

}

