#include <iostream>

int main()
{	
	std::cout << "Enter number of rows: ";	// ask the user how many rows will be in the array
	int ROW;
	std::cin >> ROW;

	std::cout << "Enter number of columns: ";	// ask the user how many columns will be in the array
	int COL;
	std::cin >> COL;

	int **arr = new int*[ROW];	// initialising an array
	for (int i = 0; i < ROW; i++)
		arr[i] = new int[COL];

	for (int i = 0; i < ROW; i++)	// filling an array
		for (int j = 0; j < COL; j++)
			arr[i][j] = rand() % 9;

	for (int i = 0; i < ROW; i++)	// outputting an array
	{
		std::cout << ' ';

		for (int j = 0; j < COL; j++)
			std::cout << arr[i][j] << ' ';
		std::cout << '\n';
	}

	for (int i = 0; i < ROW; i++)	// remove all elements from an array before deleting the array itself
		delete[] arr[i];

	delete[] arr;	// deleting an array

	system("pause");	
	return 0;
}
