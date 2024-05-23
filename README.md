# basic_program
# reverse the order of given string
public static String reverseWords(String str)
{
  if (str == null || str.isEmpty()) {
    return str;
  }
  String[] words = str.split(" ");
  StringBuilder reversed = new StringBuilder();
  for (int i = words.length - 1; i >= 0; i--) 
{
    reversed.append(words[i]);
    if (i > 0) 
{
      reversed.append(" ");
    }
  }
  return reversed.toString();
}

# 50th number of fibinocci
public class Fibonacci 
{

  public static long fibonacci(int n) 
{
    if (n <= 1) 
{
      return n;
 }
    long a = 0;
    long b = 1;
    long c = 0;

    for (int i = 2; i <= n; i++) 
{
      c = a + b;
      a = b;
      b = c;
  }

    return c;
  }

  public static void main(String[] args) 
{
    int n = 50;
    long result = fibonacci(n);
    System.out.println("The 50th Fibonacci number is: " + result);
  }
}

# n is prime number
public classisPrime {

  public static boolean isPrime(int num) {
    if (num <= 1) {
      return false;
    }
    if (num <= 3) {
      return true;
    }
    // Only check for divisibility by 2 and 3 for even numbers.
    if (num % 2 == 0 || num % 3 == 0) {
      return false;
    }
    for (int i = 5; i * i <= num; i += 6) {
      if (num % i == 0 || num % (i + 2) == 0) {
        return false;
      }
    }
    return true;
  }

  public static void main(String[] args) {
    int number = 11;
    if (isPrime(number)) {
      System.out.println(number + " is a prime number");
    } else {
      System.out.println(number + " is not a prime number");
    }
  }
}
