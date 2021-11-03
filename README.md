# code
代码学习
#include <iostream>
using namespace std;
#define countof(x) sizeof(x)/sizeof(x[0])
int main()
{
char szText[256];
int nBytes = 0;//字节数
int nSpace = 0;//空格数
int nRow = 0;//行数
int nAbc = 0;//大小写字母数
cout<<"请输入要统计的字符串，以#号结束"<<endl;
cin.get( szText, countof(szText), '#' );
for ( int i = 0; i < strlen(szText); i++ )
{
if ( (szText[i] >= 'a' && szText[i] <= 'z')
|| (szText[i] >= 'A' && szText[i] <= 'Z') )
{
nAbc++;
}
else if ( szText[i] == ' ' )
{
nSpace++;
}
else if ( szText[i] == '\n' )
{
nRow++;
}
nBytes++;
}
cout<<"字节数："<<nBytes<<endl;
cout<<"空格数："<<nSpace<<endl;
cout<<"行数："<<nRow<<endl;
cout<<"大小写字母数："<<nAbc<<endl;
return 0;
}
