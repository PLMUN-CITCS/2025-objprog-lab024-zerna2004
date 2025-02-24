# **2025-OBJPROG-LAB024**
Week 05 - Methods in Java

Laboratory # 24 - Week 05 - Guided Coding Exercise 3: Constructors and (Discussion on) Deconstructors

## **Instructions**

### **Step 1.1: Accept the Assignment**

   1. Click on the assignment link provided by your instructor.
   2. GitHub Classroom will create a **private repository** under your GitHub account.
   3. After the repository is created, click **"Go to Repository"** to view your assignment.

---

### **Step 1.2: Setup your Git Environment**
Only perform this if this is the first time you will setup your Git Environment

   1. Create a GitHub Account:
   ```bash
   https://github.com/signup?source=login
   ```
      
   2. Download and Install Git on your Laptop/Desktop:
   ```bash
   https://git-scm.com/downloads
   ```
   
   3. Create a Folder in your Laptop/Desktop
   4. Right-click anywhere in the created folder and select "Open Git Bash Here".
   5. In the Git Bash Terminal, set your git name, perform command:
   ```bash
   git config --global user.name "Your Name"
   ```
   
   6. In the Git Bash Terminal, set your git email, perform command:
   ```bash
   git config --global user.email "your.email@example.com"
   ```
   
   7. Create your SSH Key, just follow the instructions, no need to provide filename and passphrase. In the Git Bash Terminal, perform command:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   
   8. Copy your SSH Keys into clipboard. In the Git Bash Terminal, perform command:
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```
   
   9. Log in to your GitHub account.
   10. In the upper-right corner of GitHub, click your profile picture and select Settings.
   11. In the left sidebar, click on SSH and GPG keys.
   12. Click the New SSH key button.
   13. In the Title field, give the key a recognizable name (e.g., "My Windows Laptop").
   14. In the Key field, CTRL + V or paste the keys copied into your clipboard. Save the key.
   15. Go Back to terminal, use command:
   ```bash
   ssh -T git@github.com
   ```

### **Step 2: Clone the Repository to Your Local Machine**

   1. On your repository page, click the green **"Code"** button.
   2. Copy the repository URL (choose HTTPS for simplicity).
   3. Open your terminal (or Git Bash, Command Prompt, or PowerShell) and run:
   
   ```bash
   git clone <git_repo_url>
   ```
   
   4. Navigate into the cloned folder:
   
   ```bash
   cd <git_cloned_folder>
   ```

### **Step 3: Complete the Assignment**

**Laboratory # 24 - Week 05 - Guided Coding Exercise 3: Constructors and (Discussion on) Deconstructors**

   **Objective:**
   - Understand and use access modifiers (public, private, protected).
   - Define methods and attributes within a class.

   **File Naming Convention:**
   - `PersonDemo.java`

   **Desired Output:**
   ```txt
   Name: Bob, Age: 30
   Name: Unknown, Age: 0
   ```

   **Notable Observations:**
   - The Person class has two constructors: a parameterized constructor and a default constructor.
   - When you create a Person object using new Person("Bob", 30), the parameterized constructor is called, and the object's name and age are initialized with the provided values.
   - When you create a Person object using new Person(), the default constructor is called, and the object's name is set to "Unknown" and age to 0.

   **Java Programming Best Practices:**
   - Provide both a default constructor and parameterized constructors for flexibility in creating objects.
   - Use the this keyword inside constructors to refer to the object's instance variables.
   - Keep constructors concise and focused on initializing attributes.
      
   **Step-by-Step Instructions:**

   1. Create the BankAccount Class
      - Create a new Java file named `PersonDemo.java`.
      - Define a class called `Person`.
      ```Java      
      class Person {
          // Code will go here
      }
      ```
            
   2. Add Attributes with Access Modifiers
      - Inside the Person class, declare two instance variables (attributes):
         - name of type String
         - age of type int
      ```Java
      class Person {
          String name;
          int age;
      }
      ```

   3. Create a Parameterized Constructor
      - Inside the Person class, create a constructor. This is a special method that has the same name as the class and is used to initialize the object's attributes when it's created.
      - The constructor should take two parameters: a String for the name and an int for the age.
      - Inside the constructor, use the this keyword to refer to the object's instance variables and assign the parameter values to them.
      ```Java
      class Person {
          //... (attributes)...
      
          public Person(String name, int age) {
              this.name = name;
              this.age = age;
          }
      }
      ```

   4. Create a Default Constructor
      - Inside the Person class, create another constructor, but this time with no parameters. This is called a default constructor.
      - Inside the default constructor, initialize the name attribute to "Unknown" and the age attribute to 0.
      ```Java
      class Person {
          //... (attributes and parameterized constructor)...
      
          public Person() {
              this.name = "Unknown";
              this.age = 0;
          }
      }
      ```

   5. Add a displayPerson Method
      - Inside the Person class, create a method named displayPerson.
      - This method should not return any value (void).
      - Inside the displayPerson method, add a println statement to print the person's name and age in the format: "Name: [name], Age: [age]"
      ```Java
      class Person {
          //... (attributes and constructors)...
      
          public void displayPerson() {
              System.out.println("Name: " + name + ", Age: " + age);
          }
      }
      ```

   6. Create the main Method
      - In the same file (PersonDemo.java), outside the Person class, create the main method. This is where your program will start running.
      ```Java
      public class PersonDemo {
          public static void main(String[] args) {
              // Code will go here
          }
      }
      ```

   7. Create Person Objects
      - Inside the main method, create an object of the Person class named person1. Use the parameterized constructor and provide the name "Bob" and age 30 as arguments.
      ```Java
      Person person1 = new Person("Bob", 30);
      ```
      - Create another Person object named person2 using the default constructor (no arguments).
      ```Java
      Person person2 = new Person();
      ```

   8. Call the displayPerson Method
      - In the main method, call the displayPerson() method on both person1 and person2 objects.
      ```Java
      person1.displayPerson();
      person2.displayPerson();
      ```

   9. Compile and Run
       - Save the file as `PersonDemo.java`.
       - Compile the code using `javac PersonDemo.java` in your terminal or command prompt.
       - Run the compiled code using `java PersonDemo`.

   **Conclusion**
   This exercise demonstrated the use of constructors in Java. Constructors are special methods used to initialize objects when they are created. They allow you to set the initial values of an object's attributes, ensuring that the object is in a valid state when it's first used. Java also has automatic garbage collection, which means you don't need to worry about manually deallocating memory for objects. The JVM takes care of cleaning up unused objects, making memory management easier for developers.

### **Step 4: Push Changes to GitHub**
Once you've completed your changes, follow these steps to upload your work to your GitHub repository.

1. Check the status of your changes:
   Open the terminal and run:
   
   ```bash
   git status
   ```
   This command shows any modified or new files.
   
2. Stage the changes:
   Add all modified files to staging:
   
   ```bash
   git add .
   ```
   
3. Commit your changes:
   Write a meaningful commit message:
   
   ```bash
   git commit -m "Submitting OBJPROG Week 05 - Laboratory # 24"
   ```
   
4. Push your changes to GitHub:
   Upload your changes to your remote repository:
   
   ```bash
   git push origin main
   ```
