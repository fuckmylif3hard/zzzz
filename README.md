# 

public class Dog {
	private String name;
	private String race;
	private int age;
	private double weight;
	private double taillength; 
	private String tax = "tax";	
	Dog(String name, String race, int age, double weight){
	}
	public void setDog(String name, String race, int age, double weight) {
	}
	public String getRace() {
		return race;
	}
	public int getAge() {
		return age;
	}
	public double getWeight() {
		return weight;
	}
	public String getName() {
		return name;
	}

	public double getTaillength() {  

		if (race.equals(tax)) {  
			taillength = 3.7;      
		}else {  
			taillength = age*weight/10;  
		}  
		return taillength;  
	}  
	public String toString() {  
		return name+" "+race+" "+age+" år "+weight+" kg "+"svans= "+taillength;  

	}  

}  


import java.util.ArrayList;
import java.util.Scanner;

public class Kennel {
	
	
		private String readString() {
			String s = keyboard.nextLine();
			return keyboard.nextLine();
			
		}
		
		private int readInt() {
			int i = keyboard.nextInt();
			keyboard.nextLine();
			return i;
		}
		
		private double readDouble() {
			double d = keyboard.nextInt();
			keyboard.nextLine();
			return d;
		}
		
		
	
	
	
	private void setUp() {

	}
	
	
	private Scanner keyboard = new Scanner(System.in);
	private ArrayList<Dog> dogList = new ArrayList<Dog>();
		
	
	private void runCommandLoop() {
		

		while(true) {
			System.out.print("Command> ");
			String cmd = keyboard.nextLine().toLowerCase();									
			switch (cmd) {
			case "registrera hund":
					System.out.println("Vad heter hunden? ");
					String name = keyboard.nextLine();
					System.out.println(name);
					System.out.println("Vad har hunden för ras? ");
					String race = keyboard.nextLine();					
					System.out.println("Hur gammal är hunden? ");
					int age = Integer.parseInt(keyboard.nextLine());		
					System.out.println("Hur mycket väger hunden? ");
					double weight = Integer.parseInt(keyboard.nextLine());
					Dog dog1 = new Dog(name, race, age, weight);
					dogList.add(dog1);
				break;					
					
					
			case "2":
				System.out.println(dogList);
				break;
			case "exit":
				return;				
			default:
				System.out.println("Wrong command!");

			}

		}

	}

	
	
	
	
	
	
	
	private void closeDown() {
		keyboard.close();

	}

	private void run() {
		setUp();
		runCommandLoop();
		closeDown();
	}

	public static void main(String[] args) {
		Kennel kennelprogram = new Kennel();
		kennelprogram.run();

	}
}

