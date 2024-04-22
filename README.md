#include<iostream>
#include<cstdlib>
#include<time.h>
using namespace std;

int main(){
    cout << "\n_WELCOME TO THE NUMBER GUESSING GAME_"<<endl;
    int randomNumber,userGuess,attempts=0;
    srand(time(0));
    randomNumber = rand() % 100+1;
    do{
    cout<<"\n\nEnter Your Guess (between 1 to 100):"<<endl;
cin>>userGuess;
attempts++;
if(userGuess == randomNumber){
    cout<<"Congratulations! You guessed the correct number in "<<attempts<<" attempts.";
}
else if(userGuess < randomNumber){
    cout<<"Too low! Try Again.\n";
}
else{
    cout<<"Too high! Try Again.\n";
}
    }
    while(userGuess != randomNumber);
    return 0;
}
