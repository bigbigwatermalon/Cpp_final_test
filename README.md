# Cpp_final_test
---  
#### 第二题 
```  
#include <iostream>
#include <vector>
#include <algorithm>

bool cmp(int a, int b)
{
    return a > b;
}

int main()
{
    std::vector<int> vec(10e6);
    std::sort(vec.begin(), vec.end(), cmp);
    vec.erase(std::unique(vec.begin(), vec.end()), vec.end());
    return 0;
}  
```  
---  
#### 第三题
```  
auto cmp_r = [a] (int b) {return (a>b?a:b);};  
```  
---
#### 第五题
```  
#include <iostream>
#include <string>
#include <vector>
#include <fstream>
template <typename I>
void reserve_print(I s)
{
    std::ofstream fs;
    fs.open("1.txt");
    for (auto it = s.end() - 1; it != s.begin() - 1; it--)
    {
        auto x = *it;
        std::cout << x << ' ';
        fs << x << std::endl;
    }
}

int main()
{
    std::vector<int> vec = {0, 2, 4, 6, 8, 10 };
    reserve_print(vec);
    return 0;
}  
```  
---  
#### 第六题
```  
class Employee
{
private:
    string ID;
    double Salary;
public:
    Employee()  = default;
    Employee(const string &id, const string &salary)
    {
        ID = ID;
        Salary = salary;
    }
    Employee(std::istream &is) { is >> *this; }
public:
    string get_ID() const { return ID; }
    double get_Salary() const { return Salary; }
};  
```  
---  
#### 第七题
#### 第八题
```  
#include <iostream>
#include <math.h>
#include <vector>
int isPrime(long long n)
{
    if (n == 2)
        return 0;
    if (n == 1)
        return 0;
    for (long long i = 2; i < sqrt(n); i++)
    {
        if (n % i == 0)
            return 0;
    }
    return 1;

}
int main()
{
    std::vector<long long> vec;
    long long tot  = 0;
    auto it = vec.begin();
    for (int i = 1; i <= 100; i++)
    {
        if (isPrime(i))
        {
            *(it++) = i;
            tot += 1;
        }
    }
    std::cout << "the number of prime " << tot << std::endl;
    return 0;
}  
'''  
---  
#### 第九题
