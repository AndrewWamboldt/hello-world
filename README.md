import java.util.Scanner;

public class HW1 {

	public static void main(String[] args) {
		Scanner stdIn = new Scanner(System.in);
		final String lincolnGettysburg = "Fourscore and seven years ago our fathers brought forth,"
				+ " on this continent, a new nation, conceived in liberty, and dedicated"
				+ " to the proposition that all men are created equal. Now we are engaged"
				+ " in a great civil war, testing whether that nation, or any nation so"
				+ " conceived, and so dedicated, can long endure. We are met on a great"
				+ " battle-field of that war. We have come to dedicate a portion of that"
				+ " field, as a final resting-place for those who here gave their lives,"
				+ " that that nation might live. It is altogether fitting and proper that"
				+ " we should do this. But, in a larger sense, we cannot dedicate, we"
				+ " cannot consecrate—we cannot hallow—this ground. The brave men, living"
				+ " and dead, who struggled here, have consecrated it far above our poor"
				+ " power to add or detract. The world will little note, nor long remember"
				+ " what we say here, but it can never forget what they did here. It is"
				+ " for us the living, rather, to be dedicated here to the unfinished work"
				+ " which they who fought here have thus far so nobly advanced. It is rather"
				+ " for us to be here dedicated to the great task remaining before us—that"
				+ " from these honored dead we take increased devotion to that cause for"
				+ " which they here gave the last full measure of devotion—that we here"
				+ " highly resolve that these dead shall not have died in vain—that this"
				+ " nation, under God, shall have a new birth of freedom, and that government"
				+ " of the people, by the people, for the people, shall not perish from the earth."
				+ " ---Abraham Lincoln";
		;
		final String washingtonRetirement = "The great events on which my resignation"
				+ " depended having at length taken place; I have now the honor of offering"
				+ " my sincere Congratulations to Congress and of presenting myself before"
				+ " them to surrender into their hands the trust committed to me, and to claim"
				+ " the indulgence of retiring from the Service of my Country.  Happy in the"
				+ " confirmation of our Independence and Sovereignty, and pleased with the"
				+ " opportunity afforded the United States of becoming a respectable Nation,"
				+ " I resign with satisfaction the Appointment I accepted with diffidence. A"
				+ " diffidence in my abilities to accomplish so arduous a task, which however"
				+ " was superseded by a confidence in the rectitude of our Cause, the support"
				+ " of the Supreme Power of the Union, and the patronage of Heaven."
				+ " The Successful termination of the War has verified the most sanguine"
				+ " expectations, and my gratitude for the interposition of Providence, and"
				+ " the assistance I have received from my Country-men, encreases with every"
				+ " review of the momentous Contest.  While I repeat my obligations to the"
				+ " Army in general, I should do injustice to my own feelings not to acknowledge"
				+ " in this place the peculiar Services and distinguished merits of the Gentlemen"
				+ " who have been attached to my person during the War. It was impossible"
				+ " the choice of confidential Officers to compose my family should have"
				+ " been more fortunate. Permit me Sir, to recommend in particular those,"
				+ " who have continued in Service to the present moment, as worthy of the"
				+ " favorable notice and patronage of Congress I consider it an indispensable"
				+ " duty to close this last solemn act of my Official life, by commending the"
				+ " Interests of our dearest Country to the protection of Almighty God, and"
				+ " those who have the superintendence of them, to his holy keeping.  Having"
				+ " now finished the work assigned me, I retire from the great theatre of"
				+ " Action; and bidding an Affectionate farewell to this August body under"
				+ " whose orders I have so long acted, I here offer my Commission, and take"
				+ " my leave of all the employments of public life. ---George Washington";
		final String louLuckiestManAlive = "Fans, for the past two weeks you have been reading"
				+ " about the bad break I got. Yet today I consider myself the luckiest man on"
				+ " the face of this earth. I have been in ballparks for 17 years and have"
				+ " never received anything but kindness and encouragement from you fans."
				+ " Look at these grand men. Which of you wouldn’t consider it the highlight"
				+ " of his career just to associate with them for even one day? Sure, I’m lucky."
				+ " Who wouldn’t consider it an honor to have known Jacob Ruppert? Also,"
				+ " the builder of baseball’s greatest empire, Ed Barrow? To have spent six"
				+ " years with that wonderful little fellow, Miller Huggins? Then to have spent"
				+ " the next nine years with that outstanding leader, that smart student of"
				+ " psychology, the best manager in baseball today, Joe McCarthy? Sure, I’m lucky."
				+ " When the New York Giants, a team you would give your right arm to beat, and"
				+ " vice versa, sends you a gift — that’s something. When everybody down to the"
				+ " groundskeepers and those boys in white coats remember you with trophies - that’s"
				+ " something. When you have a wonderful mother-in-law who takes sides with you in"
				+ " squabbles with her own daughter - that’s something. When you have a father and"
				+ " a mother who work all their lives so you can have an education and build your"
				+ " body - it’s a blessing. When you have a wife who has been a tower of strength"
				+ " and shown more courage than you dreamed existed — that’s the finest I know."
				+ " So I close in saying that I may have had a tough break, but I have an awful"
				+ " lot to live for. ---Lou Gehrig";
		String speechText = "";
		String speech;
		String choice;
		int characters;
		int sentences;
		int x = 0; // breaks out of speech loop
		int y = -1; // breaks out of indent loop

		System.out.println("Please select a speech to format. Choices are Gettysburg, Washington, or Lou: ");
		speech = stdIn.nextLine();

		while (speech.isEmpty()) {
			System.out.println(
					"Invalid entry, Please select a speech to format. Choices are Gettysburg, Washington, or Lou: ");
			speech = stdIn.nextLine();
		}

		if (speech.contains("Gettysburg") || speech.contains("gettysburg")) {
			System.out.println(speech + " Is in my memory.");
			speechText = lincolnGettysburg;
		}

		else if (speech.contains("Washington") || speech.contains("washington")) {
			System.out.println(speech + " Is in my memory.");
			speechText = washingtonRetirement;
		} // checks for if initially the choices are picked and bypasses the do loop
		else if (speech.toLowerCase().contains("lou")) {
			System.out.println(speech + " Is in my memory.");
			speechText = louLuckiestManAlive;
		}

		else if (!speech.contains("Gettysburg") || !speech.contains("gettysburg") || !speech.contains("Washington")
				|| !speech.contains("washington") || !speech.contains("Lou") || !speech.contains("lou")) {

			do {

				System.out.println(
						"Invalid entry, Please select a speech to format. Choices are Gettysburg, Washington, or Lou: ");

				speech = stdIn.nextLine();

				if ("washington".equals(speech) || "lou".equals(speech) || "gettysburg".equals(speech)
						|| "Lou".equals(speech) || "Washington".equals(speech) || "Gettysburg".equals(speech)) {
					x++;
				}
				// User validation for entry ^^

			} while (x == 0);
		}

		System.out.println("Please enter number of indents per first line, Between 0-2:");
		choice = stdIn.nextLine();

		while (choice.isEmpty()) {
			System.out.println("Invalid entry, Please enter the number of indents per first line, Between 0-2:");
			choice = stdIn.nextLine();
		}
		if (choice.contains("1") || choice.contains("2") || choice.contains("0")) {
			System.out.println(choice + " is a valid number.");
		}

		else if (!(choice.contains("1")) || (!choice.contains("2")) || (!choice.contains("0"))) {
			do {
				System.out.println("No Actually... Please enter number of indents per first line, Between 0-2:");
				choice = stdIn.nextLine();
				if ("1".equals(choice) || "2".equals(choice) || "0".equals(choice)) {
					y++;
				}
			} while (y == -1);
			System.out.println(choice + " is a valid number.");
		}

		System.out.println("Please enter number of characters allowed per line, between 30-120:");
		characters = stdIn.nextInt();

		if (characters >= 30 && characters <= 120) {
			System.out.println(characters + " is a valid number");
		} else if (characters <= 29 || characters >= 121) {
			do {
				System.out.println("The number entered is not within range. Please enter a number between 30-120:");
				characters = stdIn.nextInt();
				System.out.println(characters + " Is a valid number");
			} while (characters < 30 || characters > 120);

		}

		System.out.println("Please enter number of sentances per paragraph, between 3-8:");
		sentences = stdIn.nextInt();

		if (sentences >= 3 && sentences <= 8) {
			System.out.println(sentences + " is a valid number");
		} else if (sentences <= 2 || sentences >= 9) {
			do {
				System.out.println("The number you have entered is not in ranges, please select a number between 3-8:");
				sentences = stdIn.nextInt();

			} while (sentences < 3 || sentences > 8);
			System.out.println(sentences + " is a valid number");
		}

		// if (speech.contains("Gettysburg") ||(speech.contains("gettysburg"))) {
		int charCount = 0;
		int sentCount = 0;
		String line = "";
		boolean newparagraph = true;
		String[] arr = speechText.split(" ");
		// for (String s : arr) {

		for (int i = 0; i < arr.length;) {
			String s = arr[i];
			if (s.startsWith("---")) {

				System.out.println(s);
				i++;
			} else {
				if (s.length() + line.length() < characters) {
					if (s.contains(".") || s.contains("?") || s.contains("!")) {
						++sentCount;
					}
					if (sentCount == 0 && line.length() == 0) {
						line += "        ";

					} else if (line.length() > 0) {
						line += " ";
					}

					line += s;
					// System.out.println(sentCount);
					i++;

				}

				else {
					System.out.println(line);

					line = "";
				}
			}
		}

	}

}


