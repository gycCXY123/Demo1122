

String


class String
{
private:
int len;
char * rep;
public:
String()
{
len=0;
rep=new char[len+1];
strcpy(rep," ");
}
String(const char* str)
{
len=strlen(str);
rep=new char[len +1];
strcpy(rep,str);
}

String operator+(const String& str)
{
len+=str.len;
char * temp=rep;
rep=new char[len+1];
strcpy(rep,temp);
strcat(rep,str.rep);
delete temp;
temp = NULL;
return *this;

}
String operator+=(const String& str)
{
len + =str.len;
char * temp=rep;
char * rep= new char[len+1];

strcat(rep,str.rep);

}
};

