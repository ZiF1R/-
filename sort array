#include <iostream>
#include <string>
#include <utility>
using namespace std;

void sort(string *array, int length)
{
	for (int startIndex = 0; startIndex < length -1; ++ startIndex)
	{
		int smallestIndex = startIndex;

		for (int currentIndex = startIndex + 1; currentIndex < length; ++currentIndex)
		{
			if (array[currentIndex] < array[smallestIndex])
				smallestIndex = currentIndex;
		}

		swap(array[startIndex], array[smallestIndex]);
	}

}

int main()
{
	// #1.Cпрашиваем у пользователя, сколько имён он хочет ввести;
	int amount; 
	cout << "How many names would you like to enter? ";
	cin >> amount;

	// #2.Просим пользователя ввести каждое имя;
	string *array = new string[amount];

	for (int i = 0; i < amount; ++i)
	{
		cout << "Enter name #" << i + 1 << ": ";
		cin >> array[i];
	}

	//#3.Bызываем функцию для сортировки имён в алфавитном порядке;
	sort(array, amount);
	
	//#4. Bыводим отсортированный список имён;
	cout << "\nHere is your sorted list : \n";

	for (int index = 0; index < amount; ++index)
	{
		cout << "Name #"<< index + 1 << ": " << array[index] << '\n';
	}

	delete[] array;
	array = nullptr;

	system("pause");	
	return 0;
}
