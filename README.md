# shopping-cart-program-python-
a simple command-line shopping cart program written in Python. The program allows the user to enter food items and their prices, then calculates the total cost.

foods = []
prices = []
total = 0

while True:
  food = input("enter a food to buy (q to quit): ")
  if food.lower() == "q": # makes lower case Q = q
    break
  else:
    price = float(input(f"enter the price of a {food}: $"))
    foods.append(food) # append: add a single element to the end of an existing list
    prices.append(price)

print("----- YOUR CART -----")

for food in foods:
  print(food, end=" ")

for price in prices:
  total += price # total = total + price

print()

print(f"ur total is: ${total}")
