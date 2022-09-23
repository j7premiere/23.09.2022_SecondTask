### Task 7 kyu

[Task link](https://www.codewars.com/kata/542c0f198e077084c0000c2e)

Count the number of divisors of a positive integer n.

Random tests go up to n = 500000.
Examples (input --> output)

4 --> 3 (1, 2, 4)
5 --> 2 (1, 5)
12 --> 6 (1, 2, 3, 4, 6, 12)
30 --> 8 (1, 2, 3, 5, 6, 10, 15, 30)

### My solution

```Java

public class FindDivisor {

    public long numberOfDivisors(int n) {

        int counter = 0;
        for (int i = 1; i < n + 1; i++) {

            if (n % i == 0) {
                counter++;
            }
        }
        return counter;
    }
}

```

### Favourite solution from code-wars

```Java

public class FindDivisor {

  public long numberOfDivisors(int n) {
    if(n == 0) return 0;
    long divisors =2; // every positive integer has 1 and integer (n) itself as divisors
    for(int i=2;i<=Math.sqrt(n);i++){
      if(n % i == 0){
        divisors++;
        if(i != (n / i)){
          divisors++;
        }
      }
    }
    
    return divisors;
  }

}

```

I really like this solution because it uses math!

# Have a nice day!