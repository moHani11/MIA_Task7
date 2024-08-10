## This markdown file shows my work for **Task1**   

[The team's PDF link for the Task description](https://drive.google.com/file/d/1dfXnoe2PdqQlWhrK-ygYNTdZeku3FJ93/view)
---
### In Summary:
> This task consists of 5 C++ programming problem-solving questions. The difficulty increases gradually. All the problems are on a HackerRank contest where i have submitted my solutions in the contest environment.

>**Bonus**:If i show good usage of functions and have clean code.

---
---

## My Work
[The contest Link](https://www.hackerrank.com/mia-robotics-task1)

My username in the contest:  **mohamedhani004**

- **Problem 0 :**

[My lastest submission](https://www.hackerrank.com/contests/mia-robotics-task1/challenges/problem-0-justice-league-greetings/submissions/code/1380211608)

code: 
>using namespace std;  
>  
>void greet_hero(string hero)  
>{  
>    cout << "Hello, " << hero << "!" << endl;  
>}  
>     
>int main() {  
>   string hero;  
>   getline(cin,hero); // taking input from the user  
>   greet_hero(hero); // sending the recieved input to the greet_hero function to greet the hero   
>   return 0;  
>}  
-----
- **Problem 1 :**

[My lastest submission](https://www.hackerrank.com/contests/mia-robotics-task1/challenges/problem-1-building-pyramids-in-atlantis/submissions/code/1380211753)

code: 
>using namespace std;    
>  
>void build_pyramid(int height)  
>{  
>    int i,j;  
>    for (i=1;i<=height;i++){  
>        for (j=0;j<i;j++) cout << "*";  
>    cout << endl;}  
>      
>}  
>int main() {  
>    int h;  //declairin an integer variable representing the height  
>    cin >> h;  // taking the input of the height form the user   
>    build_pyramid(h); // sending the height to the function responsible for printing the pyramid  
>    return 0;  
>}
----
- **Problem 2 :**

[My lastest submission](https://www.hackerrank.com/contests/mia-robotics-task1/challenges/problem-2-green-lanterns-array/submissions/code/1380212375)

code: 
>using namespace std;  
>  
>void make_array(int *arr,int n){  
>    int i =0;  
>    while(i<n){  
>        cin >> arr[i];  i++;  
>    }  
>}  
>  
>int get_target(int arr[],int n,int target){  
>    int i;  
>    for (i=0;i<n;i++) if (target == arr[i]) return i;  
>    return -1;  
>}  
>  
>int main() {  
>  
>    int num_elements;  
>    cin >> num_elements; // taking the number of the users from the input  
>      
>    int arr[num_elements];  
>    make_array(arr,num_elements);  //sending the array to make_array function to take the input  
>                                   //from the user and build the array  
>      
>    int target;  
>    cin >> target;  
>      
>    int target_index = get_target(arr,num_elements,target);  // sending the target variable to get_target function  
>    cout << target_index;  
>      
>    return 0;  
>}  
----
- **Problem 3 :**

[My lastest submission](https://www.hackerrank.com/contests/mia-robotics-task1/challenges/problem-3-flight-training-with-superman/submissions/code/1380220966)

code: 
>// using STL (using the vector container)  
>  
>using namespace std;  
>  
>vector<int> make_vector(int n){  
>        vector<int> v(n);  
>    for (vector<int> :: iterator it=v.begin();it!=v.end();it++) cin >> *it;   
>                    // iterating through the vector using the iterator data type while takng input from the user   
>    return v;  
>}  
>  
>  
>int main() {  
>    int n;  
>    cin >> n; // taking the number of heights recorded as input from the user  
>      
>    vector<int> v = make_vector(n); // sending the number of heights to the make vector function  
>                                    // which takes inputs of the heights and make  a vector from it  
>      
>    vector<int> :: iterator max = max_element(v.begin(),v.end()); //using the max_element built in function that   >returns  
>                    // an iterator of the max elemnt in the vector  
>                    // note that an iterator is like a pointer which refers to an integer in the vector   
>    cout << *max;  
>    return 0;  
>}
-----
- **Problem 4 :**

[My lastest submission](https://www.hackerrank.com/contests/mia-robotics-task1/challenges/problem-4-battle-planning-with-batman/submissions/code/1380213121)

code:   
>using namespace std;   
>   
>void build_grid(int **grid,int r, int c){   
>    for (int i=0;i<r;i++)   
>        for (int j=0;j<c;j++)   
>                cin >> grid[i][j];   
>}   
>   
>void competition(int **justic_lg,int **villans,int r,int c)      
>{   
>    int j_score =0 , v_score =0;   
>        for (int i=0;i<r;i++)   
>            for (int j=0;j<c;j++)   
>            {if(villans[i][j] < justic_lg[i][j]) j_score++;   
>             else if (villans[i][j] > justic_lg[i][j]) v_score++;}   
>       
>    if (v_score < j_score) cout << "Justice League";   
>    else if (v_score > j_score) cout << "Villains";   
>    else cout << "Tie";   
>       
>}   
>   
>int main() {   
>    int r,c;   
>        cin >> r >> c;   
>       
>    int** justic_lg = new int*[r]; // using dynamic memory allocation for building the grids    
>    for (int i = 0; i < r; ++i) {  // so i can send multidimentional arrays to the outside function   
>        justic_lg[i] = new int[c];    
>    }                             // simply just declairing a known size array of pointers    
>                                  // then declaring those pointers as array of known size   
>       
>    int** villans = new int*[r];   // using same way to build the villians grid as the justice league grid    
>    for (int i = 0; i < r; ++i) {   
>        villans[i] = new int[c];   
>    }   
>       
>    build_grid(justic_lg, r, c);   // sending the grids to the build_grid function to   
>    build_grid(villans,r, c);    // take inpt from the user and build the 2D array   
>   
>   
>    competition(justic_lg,villans,r,c); //sending the two grids to the competition function   
>                                        // which determines which team wins   
>       
>        return 0;   
>}   
>