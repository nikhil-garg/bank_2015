#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
#include<process.h>
struct Customers
{
 char name[20];
 int voterId;
 double bal;
 long accNo;

}ob1[1000];

typedef struct Customers Cust;

void Deposit(int y)
{
 double d;
 clrscr();
 cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";

 cout<<"\n\nEnter the amount you want to deposit Rs:";
 cin>>d;

 ob1[y].bal+=d;

 cout<<"\nYour current balance is Rs."<<ob1[y].bal;
 getch();
}

void Withdraw(int y)
{
 double w;
 clrscr();
 cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";
 cout<<"\n\nEnter the amount you want to withdraw Rs:";
 cin>>w;
 if((ob1[y].bal-w)>=1000)
    ob1[y].bal-=w;
 else
    cout<<"Can't withdraw, insufficient balance, minimum balance should be Rs.1000";

 cout<<"\nYour current balance is Rs."<<ob1[y].bal;
 getch();
}

void Display(int k)
{
 clrscr();
 cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";

 cout<<"\n\n Name :: ";
 puts(ob1[k].name);
 cout<<"VoterID Number :: "<<ob1[k].voterId;
 cout<<"\n Account Number  :: "<<ob1[k].accNo;
 cout<<"\n Balance :: Rs."<<ob1[k].bal;
 getch();
}


void Access(int y)
{

 int ch;
 do
 {
  clrscr();
  cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";
  cout<<"\n\n1. Deposit\n2. Withdraw \n3. Display\n4. Back to Main Menu";
  cout<<"\nEnter your choice :: ";
  cin>>ch;

  switch(ch)
  {
   case 1: Deposit(y);
	   break;
   case 2: Withdraw(y);
	   break;
   case 3: Display(y);
	   break;
   case 4: break;
   default: cout<<"Wrong choice. Enter your choice carefully.";
  }
  getch();
 }while(ch!=3);
}

int Input(int k)
{
 k++;
 clrscr();
 //cout<<k;
 cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";
 cout<<"\n\nEnter your Name :: ";
 gets(ob1[k].name);
 cout<<"\nEnter your VoterID Number :: ";
 cin>>ob1[k].voterId;
 ob1[k].bal=1000;
 ob1[k].accNo=ob1[k].voterId+1000+k;
 cout<<"\nYour Account Number is :: "<<ob1[k].accNo;
 getch();
 return k;
}

void Login(int k)
{
 char n[20];
 long ac;
 int f=-1;

 clrscr();
 //cout<<k;
 cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";
 cout<<"\n\nEnter your Name :: ";
 gets(n);
 cout<<"\nEnter your Account number :: ";
 cin>>ac;
 for(int i=0;i<=k;i++)
 {
  if(strcmp(ob1[i].name,n)==0 && (ob1[i].accNo==ac))
    {
     f=i;
     break;
    }
 }
 if(f>=0 && f<=k)
   Access(f);
 else
   {
     cout<<"\nIncorrect Input";
     getch();
   }
}


void main()
{
 static int p=-1;
 int ch;
 do
 {
  clrscr();

  cout<<"\n########## WELCOME TO PUBLIC NATIONAL BANK ##########";
  cout<<"\n\n1. REGISTER\n2. LOGIN \n3. Exit";
  cout<<"\nEnter your choice :: ";
  cin>>ch;

  switch(ch)
  {
   case 1: p=Input(p);
	   break;
   case 2: Login(p);
	   break;
   case 3: exit(0);
   default: cout<<"Wrong choice. Enter your choice carefully.";
  }

  getch();
 }while(ch!=3);
getch();

}

