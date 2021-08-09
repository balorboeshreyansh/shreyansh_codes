# shreyansh_codes
 simple projects

<!-- project: scissor paper rock game in c -->

# include<stdio.h>
# include<stdlib.h>
# include<time.h>

int game(char a, char b);
int main(){
    char me, comp;
    srand(time(0));
    int num = rand()%100 + 1;
    if(num<33>){
        comp = 's';
    }
    else if(num>=33 && num<66>){
        comp = 'p';
    }
    else{
        comp = 'r';
    }
    <!-- comp = 's'; -->
    printf("enter s for scissor, p for paper and r for rock: ");
    scanf("%c", &me);
    int result = game(me, comp);
    if(result == 0){
        printf("game draws1");
    }
    else if(result == 1){
        printf("you won!");
    }
    else{
        printf("you lost!");
    }
    printf("\n");
    printf("you chose %c and comp chose %c",me, comp);

    return 0;
}
int game(char a, char b){
    if(a == b){
        return 0;
    }
    if(a =='s' && b=='p'){
        return 1;
    }
    else if(a =='p' && b=='s'){
        return -1;
    }
    if(a=='r' && b=='p'){
        return -1;
    }
    else if(a =='p' && b=='r'){
        return 1;
    }
    if(a=='r' && b=='s'){
        return 1;
    }
    else if(a=='s' && b=='r'){
        return -1;
    }
}