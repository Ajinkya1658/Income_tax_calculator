# Income_tax_calculator
- This is my small mini project of Income tax calculator using java programming language
- Author - Ajinkya Bhagat


import java.util.*;

public class main {
    public static void main (String args []){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter your Name:         ");
        String Employer_name = sc.nextLine();
        System.out.print("Enter your ID:           ");
        int Employer_ID = sc.nextInt();
        System.out.print("Enter your Income:       ");
        int income = sc.nextInt();
        
        int tax;
        
        // Tax based on user income
        
        if ( income < 250000){
            tax = 0;
        }   // No tax below 250000
        
        else if ( income >= 250000 && income < 500000){
            tax = (int) (income * 0.5);
        }   // 5% tax above 250000 and below 500000
        
        else if ( income >= 500000 && income < 1000000){
            tax = (int) (income * 0.20);
        }   // 20% tax above 500000 and below 1000000
        else {
            tax = (int) (income * 0.30);
        }   // 30% tax above 1000000
        
        System.out.println("Employer name is : " + Employer_name);
        System.out.println("Employer ID is: " + Employer_ID);
        System.out.println("Your income is :" + income);
        System.out.println("Your tax on income is :" + tax);
        System.out.println("Net income after tax deduction :" + (int) (income - tax));
        
    }
}
