#include <iostream>
#include <string>
#include <unordered_map>


using namespace std;

// input is an arbitrary text string ended with new line
// output is a next line that contains a single number, the answer for the task: the number of distinct words
//
// 99 problems
// 1
//
// a horse and 12 dogs at a home
// 6
//
// super mega test string
// 4
//
// absent-minded
// 1   (DASH_INCLUDED = true)
// 0   (DASH_INCLUDED = false)

const bool DASH_INCLUDED = false; // include words that contain dash symbols, regardless of dash position in the words



int main()
{
    std::unordered_map<std::string, unsigned> dict;


    auto isword = [](const std::string& w) -> bool {
            bool flag = true;
            for (auto c : w)
            {
                if (DASH_INCLUDED == true)
                {
                    if (!isalpha(c) && c != '-')
                    {
                        flag = false;
                        break;
                    }
                }
                else
                {
                    if (!isalpha(c))
                    {
                        flag = false;
                        break;
                    }
                }
            }
            return flag;
        };

    for (std::string word; std::cin >> word; )
    {

        if (isword(word))
            ++dict[word];
    }
    std::cout << "The number of distinct words are: " << dict.size() << "\n";

    return 0;
}
