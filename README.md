# codesoft_task
//Create a program that generates a random number and asks the user to guess it. Provide feedback on whether the guess is too high or too low until the user guesses the correct number.

#include <iostream>
#include <cstdlib>  
#include <ctime>    

int main() {
   
    std::srand(static_cast<unsigned int>(std::time(0)));  
    int randomNumber = std::rand() % 100 + 1;  
    int guess;  

    std::cout << "Guess the number between 1 and 100!" << std::endl;

   
    while (true) {
        std::cout << "Enter your guess: ";
        std::cin >> guess;

        if (guess > randomNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else if (guess < randomNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed it!" << std::endl;
            break;  
        }
    }

    return 0;
}


