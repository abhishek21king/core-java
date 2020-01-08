# digitconverter
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package bin2dec;

/**
 *
 * @author admin
 */
  class DigitConverter {
    String number = null;
    boolean decimal = true;
    
    DigitConverter(String num , boolean decimal)
    {
        number = num;
        this.decimal = decimal;
    }
    
    public void convert()
    {
        if (decimal)
        {
            
        }
        else
        {
            int bitnum = 0;
            int sum = 0;
            int temp_bit = 0;
            for (int i =number.trim().length()-1 ; i >=0  ; i--)
            {
                temp_bit = Integer.parseInt(number.charAt(i)+"");
                sum = (int) (sum + temp_bit * Math.pow(2, bitnum));
                //System.out.println("Bit " + bitnum + "is :" + number.charAt(i));
                bitnum ++;
            }
            System.out.println("Decimal: " + sum );

            
        }
    }
    
    
    
    
}

