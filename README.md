# c-cheatsheet

Array 

declaration:

int a[5]      //declare a array of size 5(int)
int a[]={1,2,3,4}      //declare array of size 4(int) and also assign the value
int a[6]={}      //declare array of size 6(int) and assign all value 0. // {0,0,0,0,0,0}
int a[6]={1}     //declare array of size 6(int) and assign the first value to 1 and all other as 0.   // {1,0,0,0,0,0}

String: (#include<string>) 

declaration:
        c declaration
        
 char str[] = "GeeksforGeeks";

 char str[50] = "GeeksforGeeks";

 char str[] = {'G','e','e','k','s','f','o','r','G','e','e','k','s','\0'};

 char str[14] = {'G','e','e','k','s','f','o','r','G','e','e','k','s','\0'};
    
   // reading string 
    scanf("%s",str); 
      
   // print string 
    printf("%s",str);
    
   //passing function 
   void printStr(char str[]){ .... }
 
   // declare and initialize string 
    char str[] = "GeeksforGeeks"; 
      
   // print string by passing string 
   // to a different function 
    printStr(str); 
    
      c++ declaration
      
  string s="hello world";
  string s("hello world");
      
  // Taking string input using getline() for entire line upto \n
  // "geeksforgeek" in givin output 
   getline(cin,str); 
   
********************   
int a;
string s;
cin>>a;
getline(cin, s)

cin leaves an end of line, \n, character which is then read by getline();. It is possible to overcome this problem by using cin.ignore().

int a;
string s;
cin>>a;
cin.ignore();
getline(cin, s)
*******************

assign:

  std::string str;
  std::string base="The quick brown fox jumps over a lazy dog.";
   
          string
  assign(string_variable);
  str.assign(base);       //"The quick brown fox jumps over a lazy dog."

  assign(string_buffer);
  str.assign("c-string");         // "c-string"

    
       substring
  assign(stirng_variable,str_var_pos,len_to_assign);
  str.assign(base,10,9);         // "brown fox"

  assign(string_buffer,len_to_assign);
  str.assign("pangrams are cool",7);         // "pangram"


  str.assign(10,'*');         // "**********"
      
          iterator
  str.assign(base.begin()+16,base.end()-12);         // "fox jumps over"
  

compare:
std::string str1 ("green apple");
  std::string str2 ("red apple");

if (str1.compare(str2) != 0)
    std::cout << str1 << " is not " << str2 << '\n';        //green apple is not red apple
    
    compare(pos,len,string)
  if (str1.compare(6,5,"apple") == 0)         //still, green apple is an apple
    std::cout << "still, " << str1 << " is an apple\n";

  if (str2.compare(str2.size()-5,5,"apple") == 0)           //and red apple is also an apple
    std::cout << "and " << str2 << " is also an apple\n";

copy:

str1.copy(target_string,len,start_pos);

swap:

str1.swap(str2);

delete

 std::string str ("This is an example sentence.");
  std::cout << str << '\n';
  
     erase(pos,len)                                         // "This is an example sentence."
  str.erase (10,8);                        //            ^^^^^^^^
  std::cout << str << '\n';
                                           // "This is an sentence."
  str.erase (str.begin()+9);               //           ^
  std::cout << str << '\n';
                                           // "This is a sentence."
  str.erase (str.begin()+5, str.end()-9);  //       ^^^^^
  std::cout << str << '\n';
