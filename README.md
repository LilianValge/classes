# classes
```java
// MAIN
public class Main {
    public static void main(String[] args) {
        var book = new Book("The Hobbit", "J.R.R. Tolkien", 310);

        System.out.println(book.title);
        System.out.println(book.author);
        System.out.println(book.pageCount);

        var book2 = new Book();
        System.out.println(book2.title);
        System.out.println(book2.author);
        System.out.println(book2.pageCount);
    }
}

//A book, that has it's author, and book title to it.
// We create a book, and then we print out the values of the book in a fancy way.


// ----------------------------
// BOOK
public class Book{
    public String title;
    public String author;
    public int pageCount;

    public Book(String title, String author, int pageCount){
      this.title = title;
      this.author = author;
      this.pageCount = pageCount;
    }

    public Book(){
      this.title = "Unknown";
      this.author = "Unknown";
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        var child = new Child("Nelli", 2, "blonde", true);

        System.out.println(child.name);
        System.out.println(child.age);
        System.out.println(child.hairColour);
        System.out.println(child.isGirl);

        var child2 = new Child("Ralf", 0, "blonde", false);
        System.out.println(child2.name);
        System.out.println(child2.age);
        System.out.println(child2.hairColour);
        System.out.println(child2.isGirl);
    }
}

//-------------------
public class Child {
  
    public String name;
    public int age;
    public String hairColour;
    public boolean isGirl;
  

  public Child(String name, int age, String hairColour, boolean isGirl) {
    this.name = name;
    this.age = age;
    this.hairColour = hairColour;
    this.isGirl = isGirl;
    
  }
    
  public Child() {
    this.name = "";
    this.age = 0;
    this.hairColour = "";
    this.isGirl = false;

    
    
  }
}

```
```java
public class Main {
    public static void main(String[] args) {
        var square1 = new Square(3);
        var square1Perimeter = square1.getPerimeter();
        System.out.println(square1Perimeter);

        var square2 = new Square(4);
        System.out.println(square2.getPerimeter());

        var square3 = new Square(100);
        var square3Perimeter = square3.getPerimeter();
        System.out.println(square3Perimeter);

        var square4 = new Square(1);
        var square4Perimeter = square4.getPerimeter();
        System.out.println(square4Perimeter);
    }
}
//-----------------------

public class Square{
  public int sideLength; //sideLength = 7
  // new Square(7); 
  public Square(int sideLength){
    this.sideLength = sideLength;
  }

  public int getPerimeter(){
    return sideLength * 4;
  }
}
```
```java
public class Main {
    public static void main(String[] args) {
        var fork = new Fork(4, "Silver");

        System.out.println("The fork made out of " + fork.material + " has " +  fork.spikeCount + " spikes in total. And the sharpness is " + fork.sharpness);

        System.out.println("The fork is made out of " + fork.material);

        System.out.println("The fork has " + fork.spikeCount + " spikes in total.");

        System.out.println("And the sharpness is " + fork.sharpness);

        // we will create a stabbing machine. 

        for(int i = 0; i < 100; i++){
            fork.stab();
        }
        System.out.println("The sharpness after 100 stabs is " + fork.sharpness);
    }
}
//-----------------------
//Fork has 3 or 4  spikes
//Fork has a material (silver, or plastic, wood)
//Fork has sharpness in the spikes. 0
//A fork can stab and whenever a fork stabs, it gets more dull
//Sharpness is gonna decrease by 0.1

public class Fork {
  public int spikeCount;
  public String material;
  public int sharpness = 1000;

  public Fork(int spikeCount, String material) {
    this.spikeCount = spikeCount;
    this.material = material;
 
  }
  // sharpness decreases with every stab

  public void stab() {
    sharpness = sharpness - 1; // 1000 to 999 etc
  }
}

```
```java
public class Main {
    public static void main(String[] args) {
        var cake = new Cake(12, "Cheesecake");

        System.out.println("I have " + cake.type + " in my fridge waiting for me. In total it is divided in " +  cake.slices + " slices and one slice will be eaten in " + cake.biteCount + " bites.");



        for(int i = 0; i < 7; i++){
            cake.bites();
        }
        System.out.println("After I have taken 7 bites of one slice, there will be only " + cake.biteCount + " bite left" );
    }
}

public class Cake {
  public int slices;
  public String type;
  public int biteCount = 8;

  public Cake(int slices, String type) {
    this.slices = slices;
    this.type = type;
 
  }

  public void bites() {
    biteCount = biteCount - 1;
  }
}
```
