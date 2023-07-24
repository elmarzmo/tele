# tele
This Java code is a simple phone number decoder. It takes a user input phone number as a string and processes it to print the phone number with only numbers and hyphens. The code also replaces certain alphabetic characters with their corresponding numeric representation based on a phone keypad.




import java.util.Scanner;

public class PhoneNumberDecoder {
   public static void main(String[] args) {
      Scanner scnr = new Scanner(System.in);
      String phoneStr;   // User input: Phone number string
      int i;             // Current index in phone number string
      char currChar;     // Current char in phone number string
      
      System.out.println("Enter phone number: ");
      phoneStr = scnr.next();
     
      System.out.print("Numbers only: ");

      for (i = 0; i < phoneStr.length(); ++i) { // For each element
         currChar = phoneStr.charAt(i);
         if (((currChar >= '0') && (currChar <= '9')) || (currChar == '-')) {
            System.out.print(currChar); // Print character as is
         }
         else if ( ((currChar >= 'a') && (currChar <= 'c')) ||
                   ((currChar >= 'A') && (currChar <= 'C')) ) {
            System.out.print('2');
         }
         // FIXME: Add remaining else-if branches
         else {
            System.out.print('?');
         }      
      }
   }
}
