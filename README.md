# hello-world
Just learning how to put out a repository
My first java program I made (that worked).
Just a little random joke generator, you can cycle through them all by typing "yes" then "no" over and over again.

import java.util.List;
import java.util.Scanner;
import java.util.Random;

class RandomJokes1 {
	
	public static void main(String[] args) {
		
		Intro intro = new Intro();
		RandomJokes1 restart = new RandomJokes1();
		intro.intro_method();
		restart.Random();
	}
	
	void Random() {
		
		String[] jokes =  {"I went to a lot of parties in high school... my parents were kind enough to invite me to my 15th, 16th, 17th, and 18th birthday celebrations.",
			"Some people just have a way with words, and other people ... uh ... not have way.",
			"My girlfriend and I often laugh about how competitive we are. But I laugh more.",
			"A computer once beat me at chess, but it was no match for me at kick boxing." };
		
		// *****
		
		
		
		// ****
		
		String[] noJokes = {"What do you call a boomerang that doesn’t come back? A stick.",
			"For Sale: Parachute. Only used once, never opened.",
			"What is faster Hot or cold? Hot, because you can catch a cold.",
			"Why did the bee get married? Because he found his honey."};
		
		
		Scanner input = new Scanner(System.in);
		String No = ("No");
		String Quit = ("Quit");
		
		RandomJokes1 restart = new RandomJokes1();
		int i = new Random().nextInt(jokes.length);
		int n = new Random().nextInt(noJokes.length);
		String joke = input.next();
		System.out.println("");
		if (joke.equalsIgnoreCase(Quit)) {
				System.out.println("Thank you for using joke central. Goodbye.");
				System.exit(0);	
			} else if (joke.equalsIgnoreCase(No)) {
				System.out.println("~~ Too bad. " + noJokes[n]);
				System.out.println("");
				System.out.println("Would you like to hear another joke?");
				System.out.println("");
				System.out.print(">");
				String joke2 = input.next(); {
					if (joke2.equalsIgnoreCase(Quit)) {
						System.out.println("Thank you for using joke central. Goodbye.");
						System.exit(0);
					} else if (joke2.equalsIgnoreCase(No)) {
						System.out.println("");
						System.out.println("Fine, I didn't want to talk to you anyway. I'm going to hang out with HAL");
						System.exit(0);
					} else {
						System.out.println("~~ " + jokes[i]);
						System.out.println("");
						System.out.println("Would you like to hear another joke?");
						System.out.println("");
						System.out.print(">");
						restart.Random();
					}
				}
			
			} else {
				System.out.println("~~ " + jokes[i]);
				System.out.println("");
				System.out.println("Would you like to hear another joke?");
				System.out.println("");
				System.out.print(">");
				restart.Random();
			}
	}
}

class Intro {
	
	void intro_method() {
	
	
		System.out.println("Hello, welcome to Randy's Joke Center!");
		System.out.println("You can exit any time by typing 'quit'");
		System.out.println("");
		System.out.println("Would you like to hear a joke?");
		System.out.println("");
		System.out.print(">");
	
	}
}
