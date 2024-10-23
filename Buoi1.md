# Java Buổi 1

## Mục lục
- [Java Buổi 1](#java-buổi-1)
  - [Mục lục](#mục-lục)
  - [I. Các khái niệm cơ bản](#i-các-khái-niệm-cơ-bản)
    - [I.1. Java là gì ?](#i1-java-là-gì-)
    - [I.2. Lí do ra đời của Java](#i2-lí-do-ra-đời-của-java)
    - [I.3. Cách Java hoạt động](#i3-cách-java-hoạt-động)
    - [I.4. Cấu trúc cơ bản của Java](#i4-cấu-trúc-cơ-bản-của-java)
    - [I.5. Khái niệm Package](#i5-khái-niệm-package)
  - [II. Syntax cơ bản trong Java](#ii-syntax-cơ-bản-trong-java)
    - [II.1. Khai báo biến nguyên thủy](#ii1-khai-báo-biến-nguyên-thủy)
    - [II.2. Vòng lặp](#ii2-vòng-lặp)
    - [II.3. Cấu trúc rẽ nhánh](#ii3-cấu-trúc-rẽ-nhánh)
    - [II.4. Mảng trong Java](#ii4-mảng-trong-java)
  - [III. Tổng quan về Class và Object](#iii-tổng-quan-về-class-và-object)
    - [III.1. Class](#iii1-class)
    - [III.2. Object](#iii2-object)
    - [III.3. Từ khóa this](#iii3-từ-khóa-this)
    - [III.4. Constructors](#iii4-constructors)
    - [III.5. Access modifier](#iii5-access-modifier)
    - [III.6. Getter và Setter](#iii6-getter-và-setter)
    - [III.7. Static](#iii7-static)

## I. Các khái niệm cơ bản

### I.1. Java là gì ?

- **Java** là một một ngôn ngữ lập trình **hiện đại, bậc cao, hướng đối tượng, bảo mật và mạnh mẽ** và là một **Platform**. 

- **Platform**: Bất cứ **môi trường phần cứng** hoặc **phần mềm** nào mà trong đó có một **chương trình chạy**, thì được hiểu như là một Platform. Với **môi trường runtime riêng** cho mình (JRE) và **API**, **Java** được gọi là **Platform**.

### I.2. Lí do ra đời của Java

- **Java** được sử dụng với mục đích là một ngôn ngữ lập trình chuyên về **hướng đối tượng**, có khả năng phát triển theo nhiều hướng như mobile apps, web apps, desktop apps, games, ...

### I.3. Cách Java hoạt động

- Trong Java, mọi ứng dụng đều phải **khớp** với **tên lớp**, **tên lớp** phải khớp với **tên file**.
- Tên file phải có đuôi **.java**
- Trình biên dịch hiện có sẽ dịch mã sang một file có đuôi **.class** để thực hiện các câu lệnh.

### I.4. Cấu trúc cơ bản của Java

```java
public class Main {
  public static void main(String[] args) {
    // code
  }
}
```

### I.5. Khái niệm Package

- Một **Package** trong Java được sử dụng để **nhóm các class** liên quan, giống như **một thư mục trong một tệp các thư mục**.
- Dùng để tránh xung đột tên và một mã có thể duy trì tốt hơn.
- Package được chia làm 2 loại: **Built-in Packages** và **User-defined Packages**.

## II. Syntax cơ bản trong Java

### II.1. Khai báo biến nguyên thủy

- Syntax khai báo biến:

```java
type variableName = value;
```
- Hằng số (không thể thay đổi giá trị, nếu cố tình thay đổi sẽ báo lỗi)
```java
final type variableName = value;
```

- Các kiểu dữ liệu phổ biến trong Java:

| Kiểu dữ liệu | Ý nghĩa                            | Size    | Giới hạn                                                | Ví dụ  |
| ------------ | ---------------------------------- | ------- | ------------------------------------------------------- | ------ |
| **boolean**  | True/False                         | 1 bit   | True/False                                              | false  |
| **byte**     | số nguyên                          | 1 byte  | -128 -> 127                                             | 1      |
| **short**    | số nguyên                          | 2 bytes | -32,768 -> 32,767                                       | 15     |
| **int**      | số nguyên                          | 4 bytes | -2,147,483,648 -> 2,147,483,647                         | 20     |
| **long**     | số nguyên **(sau biến phải có L)** | 8 bytes | -9,223,372,036,854,775,808 -> 9,223,372,036,854,775,807 | 15000L |
| **float**    | số thực                            | 4 bytes | tối đa 7 chữ số sau dấu phẩy                            | 6.7    |
| **double**   | số thực                            | 8 bytes | tối đa 15 chữ số sau dấu phẩy                           | 15.5   |
| **char**     | kí tự                              | 2 bytes | kí tự đơn hoặc trong bảng mã ASCII                      | c      |

### II.2. Vòng lặp

- Vòng lặp while:
```java
while (condition) {
  // code
}
```

- Vòng lặp do-while:
```java
do {
  // code
}
while (condition);
```

- Vòng lặp for:
```java
for (Init; Condition; Update) {
  // code
}
```

### II.3. Cấu trúc rẽ nhánh

- if - else - else if:

```java
if (condition1) {
  // code nếu condition 1 đúng
} else if (condition2) {
  // code nếu condition 1 sai và condition 2 đúng
} else {
  // code nếu cả 2 condition đều sai
}
```
- switch - case:
```java
switch(expression) {
  case x:
    // code
    break;
  case y:
    // code
    break;
  default:
    // code
}
```

- toán tử 3 ngôi:

```java
variable = (condition) ? expressionTrue :  expressionFalse;
```

### II.4. Mảng trong Java

- Khai báo: 
```java
<datatype>[] <array_name>;
VD: String[] CLB = {"ProPTIT", "ABCDXYZ"};
```
- Tạo mảng:
```java
int num = new int[100];
```
- Truy xuất phần tử trong mảng:
```java
int n = num[55];
```
- In ra kích thước mảng:
```java
int[] arr = new int[50];
System.out.println(arr.length);
```

## III. Tổng quan về Class và Object

### III.1. Class

- Mọi thứ trong Java đều được liên kết với các **lớp và đối tượng**, cùng với các **thuộc tính** của nó và **methods**. Ví dụ: trong cuộc sống thực, một chiếc xe hơi là một **đối tượng**(object). Chiếc xe có các **thuộc tính**, chẳng hạn như trọng lượng và màu sắc, và các **methods**, chẳng hạn như ổ đĩa và phanh.

- Một **Class** giống như một **hàm tạo Object**, hoặc một **"bản thiết kế"** để tạo các đối tượng.

- Syntax
```java
public class Main {
  int x = 5;
  //methods
}
```

### III.2. Object

- Được tạo ở trong **1 Class**, có thể chứa các thành phần như **methods** và **attributes** (thuộc tính) để tạo ra các kiểu dữ liệu hữu ích. Đối tượng xác định **hành vi** của lớp. Khi bạn gửi tin nhắn đến một đối tượng, bạn bắt buộc phải **gọi đối tượng** hoặc **thực hiện** một trong các phương thức của nó.

- Syntax

```java
<class_name> <object_name> = new <class_name>;
VD:
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

### III.3. Từ khóa this

- Xét ví dụ sau:

```java
public class Main {
  int x;

  // Constructor with a parameter
  public Main(int x) {
    this.x = x;
  }

  // Call the constructor
  public static void main(String[] args) {
    Main myObj = new Main(5);
    System.out.println("Value of x = " + myObj.x);
  }
}
```
- this **truy cập** đến **đối tượng hiện tại** trong một **phương thức** hoặc **hàm tạo.**

- Việc sử dụng phổ biến nhất của this là **loại bỏ sự nhầm lẫn giữa các thuộc tính class** và **các tham số** có cùng tên (vì một thuộc tính class bị che khuất bởi một phương thức hoặc tham số constructor). Nếu bạn bỏ qua this trong ví dụ trên, đầu ra sẽ là "0" thay vì "5".

- this cũng có thể được sử dụng để:

  - Gọi hàm tạo lớp hiện tại
  - Gọi phương thức class hiện tại
  - Trả về đối tượng class hiện tại
  - Chuyển một đối số trong lệnh gọi phương thức
  - Chuyển một đối số trong lệnh gọi hàm tạo

### III.4. Constructors

- Một **constructor** trong Java là một **method** (phương thức) **đặc biệt** được sử dụng để **khởi tạo các đối tượng**. **Constructor** được gọi khi một đối tượng của một lớp được tạo. Nó có thể được sử dụng để **đặt giá trị ban đầu** cho thuộc tính đối tượng.

- VD:

```java 
// Create a Main class
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  public static void main(String[] args) {
    Main myObj = new Main(); // Create an object of class Main (Sẽ gọi constructor luôn)
    System.out.println(myObj.x); // Print the value of x
  }
}

// Outputs 5
```

- **Note:** Constructor_name phải **khớp** với **tên Class** và nó **không có kiểu trả về** (void).
- Tham số của 1 constructor: Các constructors cũng có thể lấy các tham số, được sử dụng để **khởi tạo** thuộc tính.
- VD:
```java
public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myName = new Main(2024, "Hieu");
    System.out.println(myName.modelYear + " " + myName.modelName);
  }
}

// Outputs 2024 Hieu
```

### III.5. Access modifier

- Dùng để **hạn chế phạm vi** hay **đặt cấp độ truy cập** cho class, thuộc tính, phương thức và constructor.
- Có 2 loại Modifiers:

  - **Access modifier:** kiểm soát cấp độ truy cập
  - **Non-access modifier:** không kiểm soát cấp độ truy cập, nhưng cung cấp chức năng khác
- Các phạm vi truy cập chính:

| Modifier  | Mô tả                                                                          |
| --------- | ------------------------------------------------------------------------------ |
| **public**    | có thể truy cập từ **bất kỳ đâu** (dùng được cho class)                             |
| **private**   | các biến, phương thức chỉ có thể truy cập **trong class**                          |
| **default **  | chỉ có thể sử dụng ở **cùng 1 package** (dùng được cho class)                      |
| **protected** | chỉ có thể sử dụng ở các class trong **cùng 1 package** và các **class con** của chúng |

### III.6. Getter và Setter

- **Getter**: truy xuất giá trị của một biến thành viên riêng tư (private)

- **Setter**: thiết lập (gán giá trị) cho một biến thành viên riêng tư (private)

- Cả 2 đều dùng để đảm bảo tính **đóng gói** trong Java

- VD:
```java
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
public class Main {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.setName("John"); // Set the value of the name variable to "John"
    System.out.println(myObj.getName());
  }
}

// Outputs "John"

// Nếu chạy như này sẽ bị lỗi:

public class Main {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.name = "John";  // error vì name đang ở private
    System.out.println(myObj.name); // error 
  }
}
}
```

### III.7. Static

- **Static** là một công cụ **non-access modifier** được sử dụng cho các **phương thức và thuộc tính**. Các phương thức / thuộc tính tĩnh **có thể được truy cập** mà **không cần** tạo một đối tượng của một lớp.

- VD:
```java
public class Main {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods có thể tạo khi không tạo Object trước");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods phải tạo sau khi tạo Object");
  }

  // Main method
  public static void main(String[ ] args) {
    myStaticMethod(); // Call the static method
    // myPublicMethod(); This would output an error

    Main myObj = new Main(); // Create an object of Main
    myObj.myPublicMethod(); // Call the public method
  }
}
```