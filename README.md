BOOLEAN-WITH-FOR
================

BOOLEAN WITH FOR



//	By  Reina Olarte

	// Boolean with FOR

	 import java.util.Random;

	 import java.util.Scanner;
	 
public class BooleanLoop
{
		
	public static void main( String[]args)
{
	
	Scanner input = new Scanner(System.in);
	
	//Create the Random number
	Random randomNumber = new Random();
	
	for(int i=0; i<3; i++)
	{
	//Declaring the variables
	int UserNumber;
	int computerNumber;
	computerNumber = 0 + (int)(Math.random() *10);
	boolean GameWon = false;
	boolean ResultLow = false;
	boolean ResultHigh = false;
	boolean EndGame = false;
	
	System.out.println("Welcome to the Guessing game\nPlease enter a digit from 0 to 10:");
	UserNumber = input.nextInt();

	if (computerNumber == UserNumber)
	{
		GameWon = true;
	}

	else
		{
			if (computerNumber < UserNumber)
			{
				ResultHigh = true;
			}
			else
			{	
				ResultLow = true;
			}	
		}

	if(GameWon)
	{
		System.out.println("You Guessed the right number");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}
	else if (ResultHigh)
	{
		System.out.println("You Guessed to High");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}
	else if (ResultLow)
	{
		System.out.println("You Guessed to Low");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}

	}		
}			//End main
}			//End class
