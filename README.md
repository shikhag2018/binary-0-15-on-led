# binary-0-15-on-led
//it will show 0-15 numbers in binary on led's attached to arduino
int count=0;
int x;
int binary(int n)
{
  int y=n;
  for(int i=0;i<4;i++)
  {
    x=y%2;
    y=y%2;
    count=count+1;
  
    
  if(count==1) digitalWrite(10,x);
                  
  if(count==2)digitalWrite(11,x);
                     
  if(count==3)digitalWrite(12,x);
                      
   if(count==4)digitalWrite(13,x);
                     
   if(count>4)
     {count=0;delay(1000);}
 }delay(1000);
  }
void setup()
{
  // put your setup code here, to run once:
for(int i=10;i<14;i++)
{
  pinMode(i,OUTPUT);
}
}

void loop() {
  // put your main code here, to run repeatedly:
for(int i=0;i<16;i++)
{
  binary(i);
}
}
