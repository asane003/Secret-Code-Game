#include <iostream>
#include <cmath>
#include <cstring>
#include <ctime>
#include <random>

void printIntroduction()
{

    std::cout << " -----------------------------" << std::endl;
    std::cout << "You are a secret agent...da da da...breaking into a secure server room\n";
    std::cout << "Enter the correct code to continue...\n";
    std::cout << "But beware every level the range of possible values increases\n";
    std::cout << std::endl;
}

bool playGame(int &level)
{
    // printIntroduction();
    // defining 3 variables
    // const int CodeA = 4;
    // const int CodeB = 2;
    // const int CodeC = 1;
    int standard = 5;
    int CodeA = (rand() % (standard * level)) + 1;
    int CodeB = (rand() % (standard * level)) + 1;
    int CodeC = (rand() % (standard * level)) + 1;

    int CodeSum = CodeA + CodeB + CodeC;
    int CodeProduct = CodeA * CodeB * CodeC;
    int CodeTest1 = (CodeA + CodeB) * CodeC;
    int CodeTest2 = (CodeA * CodeB) + CodeC;

    std::cout << "Level " << level << std::endl;
    std::cout << "There are 3 numbers in the code \n";
    //<< CodeA << CodeB << CodeC << std::endl;
    std::cout << "The numbers add up to " << CodeSum << std::endl;
    std::cout << "The numbers multiply to " << CodeProduct << std::endl;
    std::cout << "(CodeA + CodeB) * CodeC is " << CodeTest1 << std::endl;
    std::cout << "(CodeA * CodeB) + CodeC is " << CodeTest2 << std::endl;

    int GuessA, GuessB, GuessC;

    std::cout << "Enter guess: \n";
    std::cin >> GuessA;
    std::cin >> GuessB;
    std::cin >> GuessC;

    std::cout << "You entered " << GuessA << " " << GuessB << " " << GuessC << std::endl;

    int GuessSum = GuessA + GuessB + GuessC;
    int GuessProduct = GuessA * GuessB * GuessC;

    if (GuessA == CodeA && GuessB == CodeB && GuessC == CodeC)
    {
        std::cout << "You aced it\n\n";
        return true;
    }
    else
    {
        std::cout << "You failed!!\n\n";
        std::cout << "The numbers and the order: " << CodeA << ' ' << CodeB << ' ' << CodeC << std::endl;
        return false;
    }

    // cout << "Do you want to play again?";
    // getline(cin, continueornot);
    // if (continueornot == "yes" || continueornot == 'y' || continueornot == "Yes")
    // {
    //     return true;
    // }
    // else
    // {
    //     return = false;
    // }
}

int main()
{
    int level = 1;
    printIntroduction();
    // playGame();

    bool levelCompleted = playGame(level);

    while (levelCompleted)
    {
        // increase level difficulty
        level++;
        levelCompleted = playGame(level);
        std::cout << std::endl;
        std::cin.clear();
        std::cin.ignore();
    }

    return 0;
}
