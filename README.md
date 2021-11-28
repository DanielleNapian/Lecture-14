# Lecture-14
Standard array

    #include <iostream>
    #include<string>
    #include <array>
    using namespace std;

    /*
    int main()
    {
        array<int, 5> myarray = { 9, 7, 5, 3, 1 };
    }
    */

    int main()
    {
        array<string, 4> arr = { "Mars Bar", "Snickers", "Bounty", "Wispa" };
        cout << arr.at(1) << endl;
        cout << arr[1] << endl;

        cout << arr.font() << endl;
        cout << arr.back() << endl;

        for (int i = 0; i < arr.size(); i++) {
            cout << arr.at(i) << ", ";
        }
        cout << endl;
    }
Algorithm

    #include <iostream>
    #include <array>
    #include <algorithm>
    using namespace std;

    /*
    int main()
    {
        array<int, 5> = { 33, 5, 7, 99, 83 };
        sort(numbers.begin(), numbers.end());
        for (int num : numbers) {
            cout << num << " ";
        }
    }
    */

    // largest to smallest
    int main()
    {
        array<int, 5> numbers = { 33, 5, 7, 99, 83 };
        reverse(numbers.begin(), numbers.end()); // ← call to reverse here
        for (int num : numbers) {
            cout << num << " ";
        }
    }

Random func

    #include <iostream>
    #include <string>
    #include <algorithm>
    #include <exception>
    #include <array>
    #include <random>
    using namespace std;

    int main()
    {
        srand(7);
        array<int, 10> randomArry;
        for (int i = 0; i < 10; i++)
        {
            randomArry[i] = rand();
            cout << randomArry[i] << endl;
        }

    }
Exercises

    #include<iostream>
    using namespace std;

    /*
    int main()
    {
        int arr[10], n, i, max, min;
        cout << "Enter the size of the array : ";
        cin >> n;
        cout << "Enter the elements of the array : ";
        for (i = 0; i < n; i++)
            cin >> arr[i];
        max = arr[0];
        for (i = 0; i < n; i++)
        {
            if (max < arr[i])
                max = arr[i];
        }
        min = arr[0];
        for (i = 0; i < n; i++)
        {
            if (min > arr[i])
                min = arr[i];
        }
        cout << "Largest element : " << max;
        cout << "Smallest element : " << min;
        return 0;
    }
    */

    int main()
    {
        int randomArray[1000];
        int j = 0;
        srand(time(0));
        for (int x = 0; x < 1000; x++) {
            randomArray[x] = rand() % 100;
            if (randomArray[x] == 6) {
                cout << randomArray[x] << endl;
                j++;
            }
            else {
                continue;
            }
        }
        cout << "Amount of 6's: " << j;

    }
