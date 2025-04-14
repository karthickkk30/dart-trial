import 'dart:io';

void main() {
  Car car1 = new Car('Benz', 10000);
  Car car2 = new Car('BMW', 20000);
  Car car3 = new Car('Ford', 5000);

  print('Enter your name and money u have');
  String personName = stdin.readLineSync()!;
  double money = double.parse(stdin.readLineSync()!);
  Person p = new Person(personName, money);

  while (true) {
    print('\nWelcome to Car showroom');
    print('1.Buy Car\n2.Sell Car\n3.Change Price\n4.Exit\n');
    int choice = int.parse(stdin.readLineSync()!);
    if (choice == 4) {
      print('Exitng...');
      break;
    }

    switch (choice) {
      case 1:
        print('\nList of cars');
        print('1.${car1.name}\n2.${car2.name}\n3.${car3.name}\n');
        print('Enter car number');
        int num = int.parse(stdin.readLineSync()!);
        if (num == 1) {
          p.buyCar(car1);
        } else if (num == 2) {
          p.buyCar(car2);
        } else {
          p.buyCar(car3);
        }
        break;
      case 2:
        print('\nList of cars you have');
        print(p.ownedCars);
        print('Enter car name');
        String carName = stdin.readLineSync()!;
        Car car = new Car('aH', 43234);
        if (carName == 'Benz')
          car = car1;
        else if (carName == 'BMW')
          car = car2;
        else if (carName == 'Ford') car = car3;
        p.sellCar(car);
        break;

      case 3:
        print('\nList of cars and their prices');
        print(
            '1.${car1.name} : Rs.${car1.price}\n2.${car2.name} : Rs.${car2.price}\n3.${car3.name} : Rs.${car3.price}\n');
        print('Enter name of the car and new price');
        String car_name = stdin.readLineSync()!;
        double newPrice = double.parse(stdin.readLineSync()!);
        Car car = new Car('aH', 43234);
        if (car_name == 'Benz')
          car = car1;
        else if (car_name == 'BMW')
          car = car2;
        else if (car_name == 'Ford') car = car3;

        car.changePrice(newPrice);
    }
  }
}

class Car {
  String? name;
  double? price;
  Car(String name, double price) {
    this.name = name;
    this.price = price;
  }

  void changePrice(double newPrice) {
    this.price = newPrice;
  }
}

class Person {
  String? name;
  List<String>? ownedCars = [];
  double? moneyLeft;

  Person(String name, double money) {
    this.name = name;
    this.moneyLeft = money;
  }
  void buyCar(Car car) {
    if (car.price! > moneyLeft!) {
      print('No enough money :(');
    } else {
      ownedCars?.add(car.name!);
      moneyLeft = moneyLeft! - car.price!;
      display();
    }
  }

  void sellCar(Car car) {
    ownedCars?.remove(car.name);
    moneyLeft = moneyLeft! + car.price!;
    display();
  }

  void display() {
    print('\nDetails');
    print('Name : $name\nMoney Left : Rs $moneyLeft\nOwned cars : $ownedCars');
  }
}
