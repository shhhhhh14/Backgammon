//Backgammon
==========

//Software Engineering project

import java.util.Scanner;

public class HumanPlayer{//designed for the input options for the user

 private int[]   point = new int[10]; 
 Play play = new Play();
	
	public int[] Enter (int[] point) {//to enter the desired moves
									  //if i had time would have included an if statement
									  //to enter moves for 0- 4 moves
	    point = new int[10]; 
	
	    Scanner scan = new Scanner(System.in);

	    int i = 0;
	    while(scan.hasNextInt()){
	        point[i] = scan.nextInt();
	        i++;
	        if(i == 4){
	            break;
	        }
	    }
	    return point ;
	}
	
	
	public void SyntaxError(){//
		String moveChecker;
		String[] syntaxString;
		syntaxString = moveChecker.split("\\s+");
		if(moveChecker = in.useDelimiter("(0-9)*-(0-9)*")){
			
		}
	}
	public void Pass(){//gives the option to the player to play or not
		Play play = new Play();
		Scanner scan = new Scanner(System.in);
		System.out.println("Play or pass?");
		String userChoice = scan.nextLine();
		if(userChoice == "pass" || userChoice == "Pass"){
			System.out.println("You chose to pass. Next players turn");
		}
		else if(userChoice == "play" || userChoice == "Play"){
			Play();
			return;
		}
	}
	
	public static int Quit(){//allows the user to exit game
		
		System.out.println("Do you want to quit? Enter \"yes\" to exit or \"no\" to continue.");	
		System.out.println("\nUser input: ");
		Scanner scan = new Scanner(System.in);
		
		String input = scan.nextLine();
		String exitstring = "yes";
		String continuestring = "no";
		
		if (input.equals(exitstring)) {
			
			  System.exit(0);
			  
			} else if (input.equals(continuestring)){
				
				return 0;
			  
			}
			else {
				
				System.out.println("That is not a valid entry, please try again.");
				Quit();
				
			}
		return 0;

		}

}
