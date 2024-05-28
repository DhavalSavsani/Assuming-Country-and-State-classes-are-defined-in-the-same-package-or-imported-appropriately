# Assuming-Country-and-State-classes-are-defined-in-the-same-package-or-imported-appropriately



public class Person {
    private String name;
    private Country c1;
    private State s2;
    private int salary;
    private int age;

    // Constructor to initialize all fields
    public Person(String name, Country c1, State s2, int salary, int age) {
        this.name = name;
        this.c1 = c1;
        this.s2 = s2;
        this.salary = salary;
        this.age = age;
    }

    // Getters and Setters
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getSalary() {
        return salary;
    }

    public void setSalary(int salary) {
        this.salary = salary;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    // Override toString method to provide a string representation of the Person object
    @Override
    public String toString() {
        return "Person [name=" + name + ", country=" + c1 + ", state=" + s2 + ", salary=" + salary + ", age=" + age + "]";
    }

    // Main method to demonstrate the usage of the Person class
    public static void main(String[] args) {
        Country country = new Country("USA");
        State state = new State("California");
        Person person = new Person("John Doe", country, state, 50000, 30);

        System.out.println(person);
    }
}

// Example of Country class
class Country {
    private String cname;

    public Country(String name) {
        this.cname = name;
    }

    @Override
    public String toString() {
        return cname;
    }
}

// Example of State class
class State {
    private String sname;

    public State(String name) {
        this.sname = name;
    }

    @Override
    public String toString() {
        return sname;
    }
}
