# OOP_task
class BankAccount:
    def __init__(self, account_number, balance):
        self.__account_number = account_number
        self.__balance = balance

    def get_account_number(self):
        return self.__account_number

    def get_balance(self):
        return self.__balance

    def deposit(self, amount):
        self.__balance += amount

    def withdraw(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
        else:
            print("Insufficient funds.")
            

    haris = BankAccount("1234567890", 1000)
    alam = BankAccount("1234567810", 2000)
    yaqoob = BankAccount("1234567811", 500)

  #          ---------------------------------------------
  
  
from account import haris


print("Account Number:", haris.get_account_number())  
print("Balance:", haris.get_balance())  


haris.deposit(500)
print("Balance after deposit:", haris.get_balance())  

haris.withdraw(200)
print("Balance after withdrawal:", haris.get_balance())  

haris.withdraw(2000)


#------------------------------------------------------------


class Vehicle:
    def __init__(self, name, num_of_wheel, colour, brand):
        self.name = name
        self.num_of_wheel = num_of_wheel
        self.colour = colour
        self.brand = brand
    
    def drive(self):
        print(f"The {self.name} {self.num_of_wheel} {self.colour} {self.brand} is driving.")

    def stop(self):
        print(f"The {self.name} {self.num_of_wheel} {self.colour} {self.brand} has stopped.")

    car = Vehicle("Car", "Four", "Red", "Toyota")
    bike = Vehicle("Bike","Two", "Blue","Yamaha")
    truck = Vehicle("Truck","Eight","Copper", "Caterpillar")
    jeep = Vehicle("Jeep","Four","Black","Mitubishi")
    
    
    from Vehicle import Vehicle 
    
    class Electric_vehicle(Vehicle):
        def __init__(self, name, num_of_wheel, colour, brand, bat_capacity):
            super().__init__(name, num_of_wheel,colour,brand)
            self.bat_capacity = bat_capacity
    
        def charge(self):
            print(f"The {self.name} {self.colour} {self.brand} is charging.")


electric_car = Electric_vehicle("elec_car", "Four", "Black", "Tesla", "100 KWh")

electric_car.charge()
