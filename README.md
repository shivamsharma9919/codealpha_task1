# codealpha_task1
import java.util.*;
public class studentgradetraker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Step 1: Get the number of students
        System.out.print("Enter the number of students: ");
        int numberOfStudents = scanner.nextInt();

        // Step 2: Create an array to hold grades
        double[] gradesArray = new double[numberOfStudents];

        // Step 3: Create an ArrayList to hold grades
        ArrayList<Double> gradesList = new ArrayList<>();

        // Step 4: Input grades
        for (int i = 0; i < numberOfStudents; i++) {
            System.out.print("Enter grade for student " + (i + 1) + ": ");
            double grade = scanner.nextDouble();
            gradesArray[i] = grade; // Store in array
            gradesList.add(grade); // Store in ArrayList
        }

        // Step 5: Calculate average, highest, and lowest scores
        double sum = 0;
        double highest = gradesArray[0];
        double lowest = gradesArray[0];

        for (double grade : gradesArray) {
            sum += grade;
            if (grade > highest) {
                highest = grade;
            }
            if (grade < lowest) {
                lowest = grade;
            }
        }

        double average = sum / numberOfStudents;

        // Step 6: Display results
        System.out.println("Average grade: " + average);
        System.out.println("Highest grade: " + highest);
        System.out.println("Lowest grade: " + lowest);

        // Optional: Display all grades from ArrayList
        System.out.println("All grades: " + gradesList);

        scanner.close();

    }
}
