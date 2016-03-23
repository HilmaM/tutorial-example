# tutorial-example
To practice c++ i need this thing working
//item billing machine
#include <iostream>
# include <iomanip>
# include <cstring>
# include <limits>
# include <conio.h>

using namespace std;

const double TAX = .06;

double CalcSalesTax(double itemCost, double TAX) 
{
	double SalesTax;
	SalesTax = (itemCost * TAX);
	}
	
//inline _Setprecision setprecision(2);

int main()
{
	double TAX  = .06;							//the value of tax got from the function
	double itemCost;					//input at the till
	double SalesTax;
	SalesTax = itemCost * TAX;
	double subTotal;					//after tax
	subTotal = itemCost + SalesTax;			//calculating the subtotal
	double SubTotal;
	SubTotal = SubTotal + subTotal;
	
	double payment;
	double changeDue;					//calculating the change
	changeDue = payment - SubTotal;		//the formular for change
	char ch = 'y' && 'n';
	string usrName;
	int newReceipt, count, receiptNum = 1;
	double ToTl;
	double RcRe;
	double def;
	double ToTa;
	
	setprecision(2);
	
	//the programme initialisatio structure
	do{
	//	int login = usrName;
		cout<<"This programmeis a trial version of receipt cashier\n";
		cout<<"Please login\n";
		cout<<"Enter User Name :";
		cin>>usrName;
		cout<<"You are logged in as:"<<usrName<<endl;
	//code for receipt here!!
			do{
				//request fresh receipt after major transaction
				cout<<"\t\t\t\t\t\t"<<usrName<<endl;
				do {
					
					cout<<"Begin a new receipt : [y/n]";
					cin>>ch;
					if(ch == 'y') {
						cout<<"Successful!"<<endl;
					}
					else if(ch == 'n') {
						cout<<"Try Again!"<<endl;
					}
					else if (ch != 'y' && ch != 'n')
					{
						cout<<"Good Bye!"<<endl;
					}
				}while(ch != 'y');
				//Receipt procedure
			do{
				
				do{
					cout<<"\n###########################################################################"<<endl;
					cout<<"Receipt no.:"<<receiptNum++<<endl;
					do{						
						cout<<"Enter 0 to exit receipt";
						cout<<"\nPlease enter item cost :";
						cin>>itemCost;
						SalesTax = CalcSalesTax(itemCost, TAX);
						cout<<"Sales Tax is :"<<fixed<<showpoint<<setprecision(2)<<SalesTax << endl;
						count =count + 1;
						subTotal = itemCost + SalesTax;
						cout<<"Sub Total :"<<fixed<<showpoint<<setprecision(2)<<subTotal<<endl;
						SubTotal = SubTotal + subTotal;
						cout<<SubTotal<<showpoint<<setprecision<<endl;
					}while(itemCost != 0);
					cout<<"\n-----------------------------------------------------"<<endl;
						do {
							cout<<"The total is :"<<fixed<<showpoint<<setprecision(2)<<SubTotal<<endl;
							cout<<"Payment :";
							cin>>payment;
							if (payment < SubTotal) {
								cout<<"Insufficient Funds!!"<<endl;
							}
							}while(payment < SubTotal);
						changeDue = payment - SubTotal;
						cout<<"\nChange is :"<<fixed<<showpoint<<setprecision(2)<<changeDue<<endl;
						cout<<"Thank you for your purchase.\nPlease call again\nMudFam.org is happy to be associated with you."<<endl;
					}while(itemCost != 0);
					SubTotal =0;
					cout<<"Continue receipting..! [y/n]";
					cin>>ch;
					if(ch != 'y'){
							cout<<"Thank you ..:"<<usrName<<"\nCall again!"<<endl;
						}	
				}while(ch != 'n');
							
			}while(ch != 'y' && ch != 'n');
			ToTl = ++SubTotal;
			cout<<"Total of all receipted revenue for the day : "<<fixed<<showpoint<<setprecision(2)<<++ToTl<<endl;
			cin>>RcRe;
			def = RcRe - ToTa;
			cout<<"Deficit"<<fixed<<showpoint<<setprecision(2)<<def<<endl;
			ToTa = ToTl- def;
			cout<<"The diffference is:"<<fixed<<showpoint<<setprecision(2)<<ToTa<<endl;
		
	//Some chunk of code on top	
		cout<<"Do you want exit this program? [y/n]"<<endl;
		cin>>ch;
		if(ch != 'n'){
			cout<<"Thank you for using this program!\nCall again!"<<endl;
		}
//		else
//		{
//			cout<<newReceipt;
//		}
	}while(ch != 'y');
}
