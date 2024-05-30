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

