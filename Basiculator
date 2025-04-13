import 'dart:io';

main() {
  print(
      '1.Addition\n2.Subtraction\n3.Multiplication\n4.Division\n5.Modulus\n6.Comparison\n7.Exit');

  while (true) {
    print('Input choice');
    int choice = int.parse(stdin.readLineSync()!);
    if (choice == 7) {
      print('Exiting....');
      break;
    }
    print('Enter two numbers one by one [0-9]');
    int a = int.parse(stdin.readLineSync()!);
    int b = int.parse(stdin.readLineSync()!);
    if(((a<0||a>9)||(b<0||b>9)))
    {
      print('Numbers not within range 0-9');
      break;
    }
    switch (choice) {
      case 1:
        print('The sum of $a and $b is ${a + b}');
        break;
      case 2:
        print('The difference of $a and $b is ${a - b}');
        break;
      case 3:
        print('The product of $a and $b is ${a * b}');
        break;
      case 4:
      if(b==0)
      {
        print('Division by zero not possible');
        break;
      }
        print('The quotient of $a and $b is ${a / b}');
        break;
        case 5: print('The modulus of $a and $b is ${a%b}');
      break;
      case 6: print('Comparison results\n');
        print('$a>$b : ${a>b}');
        print('$a<$b : ${a<b}');
        print('$a>=$b : ${a>=b}');
        print('$a<=$b : ${a<=b}');
        print('$a==$b : ${a==b}');
      break;
    }
  }
}
