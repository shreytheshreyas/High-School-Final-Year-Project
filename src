/*final version of computer science project  class -12                     `
by Sanjay and Shreyas.*/
#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<iomanip.h>
#include<time.h>
#include<stdlib.h>
#include<ctype.h>
#include<constream.h>
#include<process.h>
#include<fstream.h>
#include<string.h>
#define T "Correct"
#define F "Wrong"
#define square(x) x*x
#define power3(x) x*x*x
#define power4(x) x*x*x*x
#define power5(x) x*x*x*x*x
struct player_info //structure for storing player information
{char name[20];
 int age;
}PI;
int inputting_age()// age error handler:to make sure the age makes sense
{int n;
 while(!(cin>>n)||n<=0||n>145)
 {clrscr();
  cout<<"Incorrect input.Please enter your age again."<<endl;
  cin.clear();
  cin.ignore();
 }
 return n;
}
int inputting()//number error handler: to make sure the number entered by the user make sense
{int n;
 while(!(cin>>n))
 {clrscr();
  cout<<"Incorrect input.Please enter your answer again."<<endl;
  cin.clear();
  cin.ignore();
 }
 return n;
}
void input_details()
{cout<<"Enter your name: ";
 gets(PI.name);          //changed
 cout<<"Enter your age: ";
 PI.age=inputting_age();
}
void write_review()
{clrscr();
 char A[10000];
 fstream datafile;
 cin.ignore();
 cout<<"Write your review."<<endl;
 cin.getline(A,10000);
 cout<<endl;
 datafile.open("reviews.txt",ios::app);
 datafile<<endl;
 datafile.write(PI.name,strlen(PI.name));
 datafile<<":";
 datafile.write(A,strlen(A));
 getch();
}
void read_review()
{clrscr();
 char ch='Y',A[10000];
 fstream datafile;
 datafile.open("reviews.txt",ios::in);
 while(!datafile.eof()&&toupper(ch)=='Y')
 {datafile.getline(A,10000);
  for(int i=0;i<80;i++)
  cout<<"*";
  cout<<endl;
  cout<<A<<endl;
  cout<<"Do you wanna continue(y->yes/n->no)"<<endl;
  cin>>ch;
  while((toupper(ch)!='Y')&&(toupper(ch)!='N'))
   {cout<<"Invalid entry. Please try again"<<endl;
    cin>>ch;
   }
 }
 if(datafile.eof())
 {cout<<"End of reviews"<<endl;
 }
 getch();
}
int round_counter=0;
struct round_stack
{int value;
 round_stack*next;
}*top=NULL;
round_stack*new_node(int n)
{round_stack*node;
 node=new round_stack;
 if(node==NULL)
 cout<<"Out of memory"<<endl;
 else
 {node->value=n;
  node->next=NULL;
 }
 return node;
}
void push(int n)
{round_stack *temp=NULL,*p=NULL;
 temp=new_node(n);
 if(top==NULL)
 top=temp;
 else
 {p=top;
  top=temp;
  top->next=p;
 }
}
void round_stack_display()
{int n=round_counter;
 round_stack *temp=top;
 cout<<"Your score for all the rounds are :"<<endl;
 while(temp!=NULL&&n>0)
 {cout<<"Round "<<n<<": "<<temp->value<<endl;
  n--;
  temp=temp->next;
 }
}
class memory_game_details
{protected:
 char *name;
 int age;
 int points;
 int wronganswer;
 int correctanswer;
 int ans;
 public:
 void result()
 { cout<<"RESULT \n"
     <<"NAME: "<<PI.name<<endl;
  cout<<"AGE: "<<PI.age<<endl
     <<"SCORE: "<<points<<endl
     <<"NUMBER OF QUESTIONS WRONG : "<<wronganswer<<endl
     <<"NUMBER OF QUESTIONS CORRECT : "<<correctanswer<<endl;
 }
};
class memory_game_operations:public memory_game_details
{protected:
 int a;
 int b;
 int c;
 int d;
 int e;
 int f;
 int g;
 int h;
 int t;
 int n;
 int m[3][3];
 int p[3][3];
 int A[20];
 int B[20];
 int C[20];
 int D[20];
 addition(int x,int y)

 {int z;
  z=x+y;
  return z;
 }
 subtraction(int x,int y)
 {int z;
  z=x-y;
  return z;
 }
 multiplication(int x,int y)
 {int z;
  z=x*y;
  return z;
 }
 division(int x,int y)
 {int z;
  z=x/y;
  return z;
 }
 function1(int y)//for mathematical functions of type y^2+y+10
 {int p=0;
  p=square(y)+y+10;
  return p;
 }
 long function2(int y)//for mathematical functions of type y^4+3*y^3+7*y^2+5*y+10
 {long q=0;
  q=power4(y)+3*power3(y)+7*square(y)+5*y+10;
  return q;
 }


 generaltAP(int ,int );
 generaltGP(int ,int);
 factorial(int);
 matrixsum(int X[][3]);
 bubble_sort_asc(int[],int[]);
 bubble_sort_desc(int[],int[]);
 arraysum(int[],int[],int[]);
 public:
 memory_game_operations()
 {a=0;
  b=0;
  c=0;
  d=0;
  e=0;
  f=0;
  g=0;
  h=0;
  t=0;
  n=0;
 }
};
class Level_1:public memory_game_operations
{public:
 void rules_level_1()
 {char ch;
  clrscr();
  cout<<"RULE:The rule of the game is that the answer you give for the question "<<endl
      <<"should  actually  be the answer of the previous question"<<endl
      <<"Example: "<<endl
      <<"Q. what is 1 + 1 ?(keep the answer in you mind) "<<endl
      <<"Q. what is 2 - 1? "<<endl
      <<"ans. 2 (answer to the previous question)"<<endl
      <<"This pattern continues for the following qustions"<<endl;
  cout<<"The use of calculators or writing on paper is prohibited"<<endl;
  cout<<"correct question :1 point "<<endl
      <<"wrong question : -2 points "<<endl;
  cout<<"Once you start playing the level you cannot exit the game"<<endl
      <<"until you are done"<<endl;
  cout<<"Press any key to start";
  getch();
 }
 void question_bank1();
};
class Level_2:public memory_game_operations
{public:
 void rules_level_2()
 {clrscr();
  cout<<"RULE:The rule of the game is that the answer you give for a question "<<endl
      <<"should be the answer to the question that preceedes the previous question "<<endl
      <<"Example : "<<endl
      <<"Q. what is 1 + 1 ?(keep the answer in your mind) "<<endl
      <<"Q. what is 2-3 ?(keep the answer in your mind)"<<endl
      <<"Q. what is 2*3 ?"
      <<"ans. 2 (answer of the question preceedes the question by two steps)"
      <<"The pattern continues for the folowing questions "<<endl;
  cout<<"The use of calculators or writing on paper is prohibited"<<endl;
  cout<<"Correct answer:3 points "<<endl
      <<"Wrong answer:-2 points "<<endl;
  cout<<"Once you start playing the level you cannot exit the game"<<endl
      <<"until you are done"<<endl;
  cout<<"Press any key to start "<<endl;
  getch();
 }
 void question_bank2();
};
class Level_3:public memory_game_operations
{public:
 void rules_level_3()
 {clrscr();
 cout<<"RULE:The rule of the game is that answer you give for a question must be "<<endl
     <<"the answer that preceedes the question by three steps. "<<endl
     <<"Example: "<<endl
     <<"Q. what is 1+1 ?(keep the answer in your mind) "<<endl
     <<"Q. what is 2-1 ?(keep the answer in your mind) "<<endl
     <<"Q. what is 4*4 ?(keep the answer in your mind) "<<endl
     <<"Q. what is 3/3 ? "<<endl
     <<"ans 2(answer that preceedes the question by three steps) "<<endl
     <<"The pattern continues for the folowing questions "<<endl;
 cout<<"The use of calculators is prohibited"<<endl
     <<"Calculations can be done on paper"<<endl;
 cout<<"Correct answer:5 points"<<endl
     <<"wrog answer:-2 points"<<endl;
 cout<<"Once you start playing the level you cannot exit the game"<<endl
      <<"until you are done"<<endl;
 cout<<"press any key to start "<<endl;
 getch();
 }
 void question_bank3();
};
int memory_game_operations::arraysum(int X[5],int Y[5],int Z[5])
{int check=0;
 for(int i=0;i<5;i++)
 if(Z[i]!=X[i]+Y[i])
 check++;
 if(check==0)
 return 0;
 else
 return 1;
}
int memory_game_operations::bubble_sort_asc(int X[5],int Y[5])
{int temp=0,check=0;
 for(int i=0;i<5;i++)
 for(int j=0;j<4-i;j++)
 if(X[j]>X[j+1])
 {temp=X[j];
  X[j]=X[j+1];
  X[j+1]=temp;
 }
 for(i=0;i<5;i++)
 if(Y[i]!=X[i])
 check++;
 if(check==0)
 return 0;
 else
 return 1;
}
int memory_game_operations::bubble_sort_desc(int X[5],int Y[5])
{int temp=0,check=0;
 for(int i=0;i<5;i++)
 for(int j=0;j<4-i;j++)
 if(X[j]<X[j+1])
 {temp=X[j];
  X[j]=X[j+1];
  X[j+1]=temp;
 }
 for(i=0;i<5;i++)
 if(Y[i]!=X[i])
 check++;
 if(check==0)
 return 0;
 else
 return 1;
}
int memory_game_operations::generaltAP(int x,int y)
{int z;
 z=x+(y-1)*x;
 return z;
}
int memory_game_operations::generaltGP(int x,int y)
{int z=1;
 for(int i=0;i<y;i++)
 z=z*x;
return z;
}
int memory_game_operations::factorial(int x)
{int z=1;
 for(int i=1;i<=x;i++)
 z=z*i;
 return z;
}
int memory_game_operations::matrixsum(int x[][3])
{int a=0;
 for(int i=0;i<3;i++)
 a+=x[i][i];
return a;
}
void Level_1::question_bank1()
{char ch;
 round_counter=0;
 do{clrscr();
 points=0;
 correctanswer=0;
 wronganswer=0;
 srand(time(0));
 a=(rand()%10)+1;
 b=(rand()%10)+1;
 cout<<"1.What is "<<a<<"+"<<b<<". \n";
 getch();
 clrscr();
 c=(rand()%10)+1;
 d=(rand()%10)+1;
 cout<<"2.What is "<<c<<"-"<<d<<". \n";
 ans=inputting();
 if(ans==addition(a,b))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++ ;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 b=(rand()%10)+1;
 cout<<"3.What is "<<a<<"x"<<b<<"\n";
 ans=inputting();
 if(ans==subtraction(c,d))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"4.What is 4/2 ? \n";
 ans=inputting();
 if(ans==multiplication(a,b))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%5)+1;
 cout<<"5.What is"<<a<<"! ?\n";
 ans=inputting();
 if(ans==2)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%20)+10;
 d=(rand()%20)+10;
 cout<<"6.What is "<<c<<"x"<<d<<"?\n";
 ans=inputting();
 if(ans==factorial(a))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"7.What is 48/16? \n";
 ans=inputting();
 if(ans==multiplication(c,d))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 cout<<"8.What is ("<<a<<")^2 ?\n";
 ans=inputting();
 if(ans==3)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"9.What is the Square root of 16?\n";
 ans=inputting();
 if(ans==square(a))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"10. What is tan(45)(if 45 is in degree measure)? \n";
 ans=inputting();
 if(ans==4)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%50)+20;
 b=(rand()%50)+30;
 cout<<"11. What is"<<a<<"+"<<b<<"?\n";
 ans=inputting();
 if(ans==1)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"12. Whatis the 10th term in the sequece 2,4,6,8,... ?\n";
 ans=inputting();
 if(ans==addition(a,b))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"13.What is the sum of the first diagonal of the given matrix ?\n";
 for(int i=0;i<3;i++)
 {for(int j=0;j<3;j++)
  {m[i][j]=(rand()%9)+1;
   cout<<m[i][j]<<" ";
  }
  cout<<"\n";
 }
 ans=inputting();
 if(ans==20)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%20)+15;
 b=(rand()%10)+5;
 cout<<"14. What is the value of "<<a<<"x"<<b<<"?\n";
 ans=inputting();
 if(ans==matrixsum(m))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%50)+40 ;
 d=(rand()%160)+50;
 cout<<"15. What is the value of "<<c<<"+"<<d<<"?\n";
 ans=inputting();
 if(ans==multiplication(a,b))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"16. What is the value of 144/24?\n";
 ans=inputting();
 if(ans==addition(c,d))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 cout<<"17. What is the value of f(x)=x^2+x+10 if x="<<a<<"?\n";
 ans=inputting();
 if(ans==6)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%100)+40;
 d=(rand()%150)+70;
 cout<<"18. What is the value of "<<c<<"-"<<d<<"? \n";
 ans=inputting();
 if(ans==function1(a))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"19. What is the value of ln(e) ?\n";
 ans=inputting();
 if(ans==subtraction(c,d))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+2;
 cout<<"20. What is the value of f(x)=x^4+3x^3+7x^2+5x+10? if x="<<a<<"?\n";
 ans=inputting();
 if(ans==1)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"21. What is sum of the corresponding elements of the following two arrays"<<endl;
 cout<<"A: ";
 for(i=0;i<5;i++)
 {b=(rand()%10)+1;
  A[i]=a;
  cout<<A[i]<<"\t";
 }
 cout<<endl<<"B: ";
 for(i=0;i<5;i++)
 {b=(rand()%10)+1;
  B[i]=b;
  cout<<B[i]<<"\t";
 }
 cout<<endl;
 ans=inputting();
 if(ans==function2(a))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"22. Arrange the following elements in ascending order"<<endl<<"D: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  D[i]=a;
  cout<<D[i]<<"\t";
 }
 cout<<endl;
 for(i=0;i<5;i++)
 C[i]=inputting();
 if(arraysum(A,B,C)==0)
 /*functions returns a zero value if elements of C is equal to the sum
   of the elements of A and B*/
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"23. Arrange the following elements in descending order"<<endl<<"A: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  A[i]=a;
  cout<<A[i]<<"\t";
 }
 cout<<endl;
 for(i=0;i<5;i++)
 C[i]=inputting();
 if(bubble_sort_asc(D,C)==0)//it will return 0 if it is in ascending order
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 b=(rand()%10)+1;
 cout<<"24. What is the result of the operation "<<a<<" + "<<b<<endl;
 for(i=0;i<5;i++)
 B[i]=inputting();
 if(bubble_sort_desc(A,B)==0)
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%20)+1;
 d=(rand()%20)+1;
 cout<<"25. What is the result of the operation "<<c<<" * "<<d<<endl;
 ans=inputting();
 if(ans==addition(a,b))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"26. What is the answer of the 25th question"<<endl;
 ans=inputting();
 if(ans==multiplication(c,d))
 {cout<<T;
  points++;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 result();
 round_counter++;
  getch();
  clrscr();
  push(points);
  round_stack_display();
  getch();
  cout<<"Do you wanna play level-1 again ?(y->yes/n->no)"<<endl;
  cin>>ch;
  while((toupper(ch)!='Y')&&(toupper(ch)!='N'))
  {cout<<"Invalid entry. Please try again"<<endl;
   cin>>ch;
  }
 }while(toupper(ch)=='Y');
}
void Level_2::question_bank2()
{char ch;
 round_counter=0;
 do{clrscr();
 points=0;
 correctanswer=0;
 wronganswer=0;
 srand(time(0));
 a=(rand()%5)+0;
 b=(rand()%5)+0;
 cout<<"1.What is the value of "<<a<<"+"<<b<<"?\n";
 getch();
 clrscr();
 c=(rand()%15)+2;
 d=(rand()%5)+2;
 cout<<"2.What is the value of"<<c<<"x"<<d<<"?\n";
 getch();
 clrscr();
 e=(rand()%50)+20;
 f=(rand()%50)+20;
 cout<<"3. What is the value of"<<e<<"-"<<f<<"?\n";
 ans=inputting();//needs to be the answer of the first question
 if(ans==addition(a,b))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"4. What is the value of 625/25 ?\n";
 ans=inputting();//needs to be the answer of the second question
 if(ans==multiplication(c,d))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 cout<<"5. What is the value of ("<<a<<")^3 ?\n";
 ans=inputting();//needs to be the answer of the third question
 if(ans==subtraction(e,f))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"6.What is the value of tan45 (Whhere 45 is the angle in degrees) ? \n";
 ans=inputting();//needs to be the answer of the fourth question
 if(ans==25)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%5)+1;
 cout<<"7. What is the coeffient of x in the expansion of (x+"<<c<<")^2 ?\n";
 ans=inputting();//needs to be the answer of the fifth question
 if(ans==power3(a))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 e=(rand()%5)+2;
 cout<<"8.What is the fifth term is the G.P: "<<e<<","<<e*e<<","<<e*e*e<<"... ?\n";
 ans=inputting();//needs to be the answer of the sixth question
 if(ans==1)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%100)+90;
 b=(rand()%100)+90;
 cout<<"9. What is the value of "<<a<<"x"<<b<<"?\n";
 ans=inputting();//needs to be the answer of the seventh question
 if(ans==2*c)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"10. What is the value of sin(90) (if 90 is the angle in degrees) ?\n";
 ans=inputting();//needs to be the answer of the eighth question
 if(ans==power5(e))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%200)+100;
 d=(rand()%300)+100;
 cout<<"11. What is the value of"<<c<<"-"<<d<<"?\n";
 ans=inputting();//needs to be the answer of the 9th question
 if(ans==multiplication(a,b))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 e=(rand()%9)+1;
 cout<<"12. What is the value of f(x)=x^2+x+10 if x="<<e<<"?\n";
 ans=inputting();//needs to be the answer of the tenth question
 if(ans==1)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"13. What is the value 168/12?\n";
 ans=inputting();//needs to be the answer of the 11th question
 if(ans==subtraction(c,d))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"14. What is the sum of the diagonal of the following matrix ?\n";
  for(int i=0;i<3;i++)
 {for(int j=0;j<3;j++)
  {m[i][j]=(rand()%9)+1;
   cout<<m[i][j]<<" ";
  }
  cout<<"\n";
 }
 ans=inputting();//needs to be the answer of the 12th question
 if(ans==function1(e))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+5;
 b=(rand()%10)+5;
 cout<<"15. What is the value of "<<a<<"x"<<b<<"?\n";
 ans=inputting();//needs to be the answer of the 13th question
 if(ans==14)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%5)+1;
 d=(rand()%10)+1;
 cout<<"16. What is the "<<d<<"th term in the A.P: "<<c<<","<<c+c<<","<<c+c+c<<"....?\n";
 ans=inputting();//needs to be the answer of the 14th question
 if(ans==matrixsum(m))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"17. What is the value of (8)^3?\n";
 ans=inputting();//needs to be the answer of the 15th question
 if(ans==multiplication(a,b))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 e=(rand()%3)+1;
 cout<<"18.What is the f(x)=x^4+3x^3+7x^2+5x+10 if x="<<e<<"?\n";
 ans=inputting();//needs to be the answer of the 16th question
 if(ans==generaltAP(c,d))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"19.What is the cube root of 1331?\n";
 ans=inputting();//needs to be the answer of the 17th question
 if(ans==512)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"20.What is the value of (2)^10?\n";
 ans=inputting();//needs to be the answer of the 18th question
 if(ans==function2(e))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"21.Arrange the following elements in descending order"<<endl<<"A: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  A[i]=a;
  cout<<A[i]<<"\t";
 };//needs  to be the answer of the 19th question
 cout<<endl;
 ans=inputting();
 if(ans==11)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"22.What is the result of 3^3 ?"<<endl;//needs to be the answer of the 20th question
 ans=inputting();
 if(ans==1024)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"23. What is the sum of the diagonal elements of the following matrix ?"<<endl;
 //needs to be the answer of the 21st question
  for(i=0;i<3;i++)
 {for(int j=0;j<3;j++)
  {m[i][j]=(rand()%9)+1;
   cout<<m[i][j]<<" ";
  }
  cout<<"\n";
 }
 for(i=0;i<5;i++)
 B[i]=inputting();
 if(bubble_sort_desc(A,B)==0)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"24.Arrange the following elements in ascending order"<<endl<<"D: ";
 //needs to be the answer of the 22nd question
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  D[i]=a;
  cout<<D[i]<<"\t";
 }
 cout<<endl;
 ans=inputting();
 if(ans==power3(3))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%5)+1;
 d=(rand()%10)+1;
 cout<<"25.What is result of the operation "<<c<<'+'<<d<<" ?"<<endl;
 //needs to be the answer of the 23rd question
 ans=inputting();
 if(ans==matrixsum(m))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"Q.What is the answer of the 24th question"<<endl;
 for(i=0;i<5;i++)
 C[i]=inputting();
 if(bubble_sort_asc(D,C)==0)
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"Q.What is the answer of the 25th question ?"<<endl;
 ans=inputting();
 if(ans==addition(c,d))
 {cout<<T;
  points+=3;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 result();
 round_counter++;
  getch();
  clrscr();
  push(points);
  round_stack_display();
  getch();
  cout<<"Do you wanna play level-2 again ?(y->yes/n->no)"<<endl;
  cin>>ch;
  while((toupper(ch)!='Y')&&(toupper(ch)!='N'))
  {cout<<"Invalid entry. Please try again"<<endl;
   cin>>ch;
  }
  }while(toupper(ch)=='Y');
}
void Level_3::question_bank3()
{char ch;
 round_counter=0;
 do{clrscr();
 points=0;
 correctanswer=0;
 wronganswer=0;
 srand(time(0));
 a=(rand()%10)+1;
 cout<<"1.What is the value of ("<<a<<")^3?"<<endl;
 getch();
 clrscr();
 c=(rand()%1000)+1;
 d=(rand()%2000)+1;
 cout<<"2.What is the value of "<<c<<"+"<<d<<"?\n";
 getch();
 clrscr();
 cout<<"3.What is the value of cot(90) (if 90 is the angle in degrees)?\n";
 getch();
 clrscr();
 e=(rand()%30)+20;
 f=(rand()%30)+20;
 cout<<"4.What the value of "<<e<<"x"<<f<<"?\n";
 ans=inputting();//needs to be the answer of the first question
 if(ans==power3(a))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 g=(rand()%2)+5;
 t=(rand()%4)+8;
 cout<<"5.What is the "<<t<<"th term of the G.P: "<<g<<","<<g*g<<","<<g*g*g<<"...?\n";
 ans=inputting();//needs to be the answer of the second question
 if(ans==addition(c,d))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"6.What is the value of cos(0) (if 0  is the angle in degrees)?\n";
 ans=inputting();//needs to be the answer of the third question
 if(ans==0)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 a=(rand()%10)+1;
 b=(rand()%100)+1;
 cout<<"7.What is the "<<b<<"th term of the AP: "<<a<<","<<a+a<<","<<a+a+a<<".... ?\n";
 ans=inputting();//needs to be the answer of the 4th question
 if(ans==multiplication(e,f))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"8.What is the 125/25 ?\n";
 ans=inputting();//needs to be the answer of the 5th question
 if(ans==generaltGP(g,t))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%5)+1;
 cout<<"9.What is the value of f(x)=x^2+x+10 if x="<<c<<"?\n";
 ans=inputting();//needs to be the answer of the 6th question
 if(ans==1)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"10.What is the sum of the diagonal(from left to right) in the following matrix? \n";
 for(int i=0;i<3;i++)
 {for(int j=0;j<3;j++)
  {m[i][j]=(rand()%9)+1;
   cout<<m[i][j]<<" ";
  }
  cout<<"\n";
 }
 ans=inputting();//needs to be the answer of the 7th question
 if(ans==generaltAP(a,b))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"11.Arrange the following elements in ascending order"<<endl<<"D: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  D[i]=a;
  cout<<D[i]<<"\t";
 }
 cout<<endl;
 //needs to be the answer of the 8th question
 ans=inputting();
 if(ans==5)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"12.What is the sum of the first diagonal of the given matrix ?\n";
 for(i=0;i<3;i++)
 {for(int j=0;j<3;j++)
  {p[i][j]=(rand()%9)+1;
   cout<<p[i][j]<<" ";
  }
  cout<<"\n";
 }
 //needs to be the answer of the  9th question
 ans=inputting();
 if(ans==function1(c))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 e=(rand()%30)+20;
 f=(rand()%30)+20;
 cout<<"13.What is the operation on the "<<e<<" * "<<f<<" ?"<<endl;
 //needs to be the answer of the 10th question
 ans=inputting();
 if(ans==matrixsum(m))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"14.What is sum of the elements of the following two arrays"<<endl;
 cout<<"A: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  A[i]=a;
  cout<<A[i]<<"\t";
 }
 cout<<endl<<"B: ";
 for(i=0;i<5;i++)
 {a=(rand()%10)+1;
  B[i]=a;
  cout<<B[i]<<"\t";
 }
 cout<<endl;
 for(i=0;i<5;i++)
 C[i]=inputting();//needs to be the answer of the 11th question
 if(bubble_sort_asc(D,C)==0)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 c=(rand()%15)+1;
 d=(rand()%10)+1;
 cout<<"15.What  is the result of the operation "<<c<<" * "<<d<<" ?"<<endl;
 ans=inputting();//needs to be the answer of the 12th question
 if(ans==matrixsum(p))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"Q.What is the answer of the 13th question ?"<<endl;
 ans=inputting();
 if(multiplication(e,f)==ans)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"Q.What is the answer of the 14th question ?"<<endl;
 for(i=0;i<5;i++)
 C[i]=inputting();
 if(arraysum(A,B,C)==0)
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
 cout<<"Q.What is the answer of the 15th question ?"<<endl;
 ans=inputting();
 if(ans==multiplication(c,d))
 {cout<<T;
  points+=5;
  correctanswer++;
 }
 else
 {cout<<F;
  points-=2;
  wronganswer++;
 }
 getch();
 clrscr();
  result();
  round_counter++;
  getch();
  clrscr();
  push(points);
  round_stack_display();
  getch();
  cout<<"Do you wanna play level-3 again ?(y->yes/n->no)"<<endl;
  cin>>ch;
  while((toupper(ch)!='Y')&&(toupper(ch)!='N'))
  {cout<<"Invalid entry. Please try again"<<endl;
   cin>>ch;
  }
 }while(toupper(ch)=='Y');
}
int main()
{clrscr();
 int n;
 char ch;
 Level_1 L1;
 Level_2 L2;
 Level_3 L3;
 for(int o=0;o<11;o++)
 cout<<endl;
 constream cout;
 cout<<setclr(3);
 cout<<setw(48)<<"MEMORY GAME!!!"<<endl;
 cout<<setclr(500);
 cout<<setw(52)<<"Press any key to start";
 textcolor(GREEN);
 getch();
 clrscr();
 input_details();
 getch();
 do
 {textcolor(BROWN);
  clrscr();
  cout<<"Select an option: "<<endl
      <<"1.Play level-1"<<endl
      <<"2.Play level-2"<<endl
      <<"3.Play level-3"<<endl
      <<"4.Write a review"<<endl
      <<"5.Read reviews by other players"<<endl
      <<"6.Exit from the game"<<endl;
  n=inputting();
  switch(n)
  {case 1:textcolor(YELLOW);
	  L1.rules_level_1();
	  L1.question_bank1();
	  top=NULL;
	  break;
   case 2:textcolor(CYAN);
	  L2.rules_level_2();
	  L2.question_bank2();
	  top=NULL;
	  break;
   case 3:textcolor(RED);
	  L3.rules_level_3();
	  L3.question_bank3();
	  top=NULL;
	  break;
   case 4:textcolor(WHITE);
	  write_review();
	  break;
   case 5:textcolor(WHITE);
	  read_review();
	  break;
   case 6:exit(0);
	  break;
   default:cout<<"You have selected the wrong option"<<endl;
  }
  clrscr();
  cout<<"Do you wanna play again ?(y->yes/n->no)"<<endl;
  cin>>ch;
  while((toupper(ch)!='Y')&&(toupper(ch)!='N'))
  {cout<<"Invalid entry. Please try again"<<endl;
   cin>>ch;
  }
 }while(toupper(ch)=='Y');
 clrscr();
 for(o=0;o<11;o++)
 cout<<endl;
 cout<<setclr(507);
 cout<<setw(52)<<"Thank You For Playing :)"<<endl;
 getch();
 return 0;
}

