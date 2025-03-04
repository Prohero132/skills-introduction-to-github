#this 1st python
print("The Data of food wasted in terms of(tons) 2021-2024")
stack =[1.3]
print("2021 (bilions)",stack)
stack =[1.05]
print("2022 (bilions)",stack)
stack =[1.2]
print("2023 (bilions)",stack)
stack =[1.03]
print("2024 (bilions)",stack)
print("total of food waste is around 5b tons of food")

#This is 2nd python
print("Steps to ensure good food product")
stack =[1]
print(stack,"check the products environment")
stack =[2]
print(stack,"check for expiration date")
stack =[3]
print(stack,"finding the food whether if it's risk of shortage or sufficient")
#This is 3rd python
import random

def monitor_crop_health():
    temperature = random.uniform(20, 35)  # Degrees Celsius
    humidity = random.uniform(40, 80)  # Percentage

    alert = ""
    if temperature > 32:
        alert += "Warning: High temperature detected!\n"
    if humidity < 50:
        alert += "Warning: Low humidity detected!\n"

    return f"Temperature: {temperature:.2f}°C, Humidity: {humidity:.2f}%\n{alert}"

print(monitor_crop_health())
#4th python
from datetime import datetime

class FoodItem:
    def __init__(self, name, quantity, expiry):
        self.name, self.quantity = name, int(quantity)
        self.expiry = datetime.strptime(expiry, "%Y-%m-%d")

    def status(self):
        days_left = (self.expiry - datetime.today()).days
        return "Expired" if days_left < 0 else f"{days_left} days left"

class FoodInventory:
    def __init__(self):
        self.items = []

    def add(self, name, qty, expiry):
        self.items.append(FoodItem(name, qty, expiry))
        print(f"✅ {qty} of {name} added (Expires: {expiry})")

    def show(self):
        for i in self.items:
            print(f"- {i.name}: {i.quantity} ({i.status()})")

    def check_low_stock(self, threshold=5):
        low_stock = [i for i in self.items if i.quantity <= threshold]
        print("\n⚠️ Low Stock:" if low_stock else "\n✅ All items stocked.")
        for i in low_stock:
            print(f"- {i.name}: {i.quantity} left!")

# Example Usage
inventory = FoodInventory()
inventory.add("Rice", 10, "2025-06-10")
inventory.add("Milk", 2, "2025-03-05")
inventory.add("Eggs", 12, "2025-03-10")

inventory.show()
inventory.check_low_stock()
#java 1
class FoodSecurity:
    def __init__(self, food_supply, population):
        self.food_supply = food_supply
        self.population = population

    def check_security(self):
        food_per_person = self.food_supply / self.population
        if food_per_person >= 2:  # Assuming 2 units of food per person is sufficient
            return "Food supply is sufficient."
        elif 1 <= food_per_person < 2:
            return "Food supply is moderate. Risk of shortages."
        else:
            return "Food supply is insufficient! Risk of hunger."

# Example usage
food_supply = 5000  # Example total food units
population = 2500   # Example total population

fs = FoodSecurity(food_supply, population)
print(fs.check_security())
