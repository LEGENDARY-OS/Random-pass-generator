#include<iostream>
#include<cstdlib>
#include<ctime>
using namespace std;
//c++ program
static const char alphanum[]=
"0123456789"
"!@#$%^&*"
"ABCDEFGHIJKLMNOPQRSTUVWXZY"
"abcdefghijklmnopqrstuvxyz";
int size = sizeof(alphanum) - 1;

int main()
{
	//password length
	int length;
	cout<<endl<<"Enter the length of the password.....i.e..8-9 or even more: ";
	cin>>length;
	
	srand(time(0));
	for (int i = 0;i<length;i++)
	{
		cout<<alphanum[rand() % ::size];
	}
	return 0;
}