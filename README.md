#include <stdio.h>
#include <cs50.h>
#include <math.h>

int main(void) 
{
    int cash, dec, num, b, num2, c, w, e;
    
    do 
    {
        cash = get_float("Change owed:");
    } 
    
    while (cash < 0);
    
    
    dec = cash * 100;
    
    int dec2 = (int)dec;
    
    num = dec2 / 25;
    
    num2 = dec2 % 25;
    
    if (num2 < 25 && num2 > 10) 
    {
        b = num2 / 10;
        c = num2 % 10;
        
        if (c > 0 )
        {
            if (c > 5)
            {
                w = c / 5;
                e = c % 5;
                
            printf("%i\n", num + b + c + w);
                
            }
            
            else 
            {
                printf("%i\n", num + b + c);
            }
            
            
        }
        
        else 
        {
            printf("%i\n", b + num);
        }
    }
    
    else 
    {
        printf("%i\n", num);
        
    }
    
}
