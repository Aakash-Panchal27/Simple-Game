//my first project game hi-lo
//Aakash Panchal

#include "pch.h"
#include <iostream>
#include<string>
#include<cmath>
#include<cstdlib>
#include<ctime>

int randomnumbergenerator();
int reply(int, int);

int main()
{
	std::cout << "\n\nInstructions:\n";
	std::cout << "I have choosen one number between 1 to 100\n\n";
	std::cout << "You are supposed to make guess and I will give you reply \n"
				 "whether your guess is lower than my real number or greater or exactly equal\n"
				 "If your guess come correct under 7 attempts then you will win else lose\n";

	std::cout << "Enter a character to continue\n";
	char m;
	std::cin >> m;
	std::cin.ignore(32768, '\n');
	char mi{ 'y' };
	do {
		std::cout << "\nStart\n";
		int comguess{ 0 };
		comguess = randomnumbergenerator();
		int i{ 0 };

		for (i = 0; i < 7; i++)
		{
			std::cout << "enter number guess " << i + 1 << "\n";
			int ch;
			std::cin >> ch;
			int r{ reply(ch, comguess) };
			if (r == 0)
			{
				std::cout << "Great!\n" << "you won";
				break;
			}
			else if (r == -1)
			{
				std::cout << "greater than mynumber\n";
				continue;
			}
			else
			{
				std::cout << "lower than mynumber\n";
				continue;
			}
		}
		if (i == 7)
		std::cout << "My guess was: " << comguess<<"\n";

		std::cout << "Do you want to play again? \n enter y to play again and n otherwise\n\n";
		std::cin >> mi;
		std::cin.ignore(32678, '\n');
	} while (mi == 'y');

}

int randomnumbergenerator()
{
	std::srand(static_cast<unsigned int>(std::time(nullptr)));
	return (1 + (rand() % 100));
}

int reply(int guess, int ranum)
{
	if (guess == ranum)
		return 0;
	else if (guess < ranum)
		return 1;
	else
		return -1;
}
