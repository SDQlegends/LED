int BASE = 2 ; 
int NUM = 4;   
int ledpin=2;
int inpin=7;
int val;
void setup()
{
pinMode(ledpin,OUTPUT);
pinMode(inpin,INPUT);
}
void loop()
{
val=digitalRead(inpin);
if(val==LOW)
{ digitalWrite(ledpin,LOW);}
else
{ for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);   
     delay(200);      
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);   
     delay(200);       
   } 
;}
}
