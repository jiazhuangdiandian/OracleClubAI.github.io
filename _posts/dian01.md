# c51单片机c代码解析
<pre>
#include<reg52.h>
#include<intrins.h>
#define uchar unsigned char
#define uint unsigned int
uint i;
uchar j;
void delay_ms(uint k)                                  //延时子程序
{

  for(i=0;i<k;i++)
   {
    for(j=0;j<230;j++)
        {
         ;
        }
   }
  }

<pre>
main()
{
          uchar a,b;
          P1=0xfe;
          delay_ms(1000);
          b=P1;

          while(1)
          {
                for(a=0;a<7;a++)
                {
                         b=_crol_(b,1);
                         P1=b;
                         delay_ms(1000);
                }


                   for(a=0;a<7;a++)
                {
                          b=_cror_(b,1);
                          P1=b;
                          delay_ms(1000);

                }

           }

  }
 
