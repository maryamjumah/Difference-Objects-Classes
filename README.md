# Difference-Objects-Classes
// Main.java
public class Main {
    public static void main(String[] args) {
        // Creating objects of Student class
        Student student1 = new Student("Alice", 2000, "Computer Science");
        Student student2 = new Student("Bob", 1999, "Mathematics");

        // Printing details of students
        System.out.println("Student 1:");
        System.out.println(student1);

        System.out.println("\nStudent 2:");
        System.out.println(student2);
    }
}
// Person.java - This is a superclass
public class Person {
    // Fields
    private String name;
    private int yearOfBirth;

    // Constructor
    public Person(String name, int yearOfBirth) {
        this.name = name;
        this.yearOfBirth = yearOfBirth;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Getter for year of birth
    public int getYearOfBirth() {
        return yearOfBirth;
    }

    // toString method to represent Person's details
    @Override
    public String toString() {
        return "Name: " + name + ", Year of Birth: " + yearOfBirth;
    }
}
// Student.java - This is a subclass of Person
public class Student extends Person {
    // Additional field specific to Student
    private String major;

    // Constructor
    public Student(String name, int yearOfBirth, String major) {
        super(name, yearOfBirth);
        this.major = major;
    }

    // Getter for major
    public String getMajor() {
        return major;
    }

    // Override toString() to include major
    @Override
    public String toString() {
        return super.toString() + ", Major: " + major;
    }
}
