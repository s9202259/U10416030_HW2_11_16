//U10416030 陳子勤

import java.util.ArrayList;
import java.util.Scanner;

public class RepeatAdditionQuiz {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int number1 = (int)(Math.random()*10);		//隨機生成的兩個題目數字
		int number2 = (int)(Math.random()*10);
		int inputNumber;
		
		System.out.println("what is " + number1 + " + " + number2 + " ?");
		inputNumber = input.nextInt();
		
		Calculate cal = new Calculate();
		
		while (inputNumber != number1 + number2) {		//判定輸入的數字是否正確，以及是否有重複
			if(cal.alreadyEnter(String.valueOf(inputNumber))) {
				System.out.println("You already enter " + inputNumber 
						+ ", please enter again");
				inputNumber = input.nextInt();
			}
			else {
				cal.addArray(String.valueOf(inputNumber));
				System.out.println("Wrong answer, please enter again:");
				inputNumber = input.nextInt();
			}
			
		}
		System.out.println("You got it!");
	}
}

class Calculate {
	
	private ArrayList<String> alreadyEnter = new ArrayList<String>();		//儲存輸入過的數字
	Calculate() {
	}
	
	public boolean alreadyEnter(String a) {		//判定輸入的數字有沒有重複
		if (alreadyEnter.contains(a)) {
			return true;
		}
		else return false;
	}
	
	public void addArray(String a) {		//將輸入的數字存進ArrayList裡面
		alreadyEnter.add(a);
	}
}
