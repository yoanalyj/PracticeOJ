/*
The string "PAYPALISHIRING" is written in a zigzag pattern on a given number of rows like this: (you may want to display this pattern in a fixed font for better legibility)

P   A   H   N
A P L S I I G
Y   I   R
And then read line by line: "PAHNAPLSIIGYIR"
Write the code that will take a string and make this conversion given a number of rows:

string convert(string text, int nRows);
convert("PAYPALISHIRING", 3) should return "PAHNAPLSIIGYIR".
*/

class Solution {
public:
    string convert(string s, int numRows) {
        if (numRows <= 1)//缺少边界情况的考虑,而且不仅仅是==1
            return s;
        size_t len = s.length();
        string v;
        for(int j = 0; j < numRows; j++)
        {
            for(int i = j; i < len; i+= (2*numRows-2))
            {
                v.push_back(s[i]);
                if(j && (numRows-1-j) && (i+2*numRows-2-2*j) < len)//if本来在for循环里,没有加括号***另外if条件正好写反.**对[i+2*numRows-2-2*j]没有考虑这种情况.
                    v.push_back(s[i+2*numRows-2-2*j]);
            }
        }
        return v;
    }
};
//note
/*  代码风格:
    int i, j;直接写在用的时候
    size_t是无符号int
    string.length()和string.size()是一样的.不要忘记加括号.长度不包括\0;
    如果有两个for循环嵌套,那么continue只会跳出第一个for循环,然后继续两个循环.
*/
