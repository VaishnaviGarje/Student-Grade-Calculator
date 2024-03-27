# Student-Grade-Calculator
	public void Gradecalculator(){
		try{
			System.out.println(".......................STUDENT GRADE CALCULATOR..................");
			for (i = 0; i < Subjects.length; i++) {
				System.out.println("Enter marks of " + Subjects[i]);
				Scanner s = new Scanner(System.in);
				marks[i] = s.nextInt();
				if ( marks[i] > 100) {
					System.out.println("please enter correct marks from 1 to 100");
					return;
				}
			}

			System.out.println("------------------------------------------------------------------------------------");
			System.out.println("Marks of all Subjects");
			System.out.println("------------------------------------------------------------------------------------");

			for (int j = 0; j < Subjects.length; j++) {
				System.out.println(Subjects[j]+"\t:\t"+ marks[j]);
			}

			for (i = 0; i < marks.length; i++) {
				sum += marks[i];
			}
			System.out.println("-----------------------------------------");
			System.out.println("sum of marks=" + sum);
			System.out.println("-----------------------------------------");

			double average = sum / Subjects.length;
			System.out.println("\n-----------------------------------------");
			System.out.println("Average of sum=" + average + "%");
			System.out.println("-----------------------------------------");

			char grade;
			if (average >= 90) {
				grade = 'O';
				System.out.println("Congratulations....! You received an " + grade + " grade.Excellent performance!");
			} else if (average >= 70) {
				grade = 'A';
				System.out.println("Congratulations....! Good performance.You received an " + grade + "+ grade.!");
			} else if (average >= 60) {
				grade = 'A';
				System.out.println("Congradulations....! You received an " + grade + " grade.!");
			} else if (average >= 50) {
				grade = 'B';
				System.out.println("your performance was average.you received a " + grade + " grade.!");
			} else if (average >= 40) {
				grade = 'c';
				System.out.println("You received a " + grade + " grade.");
			} else if (average >= 35) {
				grade = 'D';
				System.out.println("You received a " + grade + " grade.");
			} else {
				System.out.println("YOU Fail");
			}
		}catch(Exception e){
			System.out.println("exception occured: "+e);
			System.out.println("plese enter valid data");
		}
		
	}
	public static void main(String[] args) {
		Task2 t=new Task2();
		t.Gradecalculator();
		}
}
