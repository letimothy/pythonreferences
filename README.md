#print
print()

#variable
lol = "laugh out loud"

#cases
print(lol.title())
print(lol.upper())
print(lol.lower())

#adding tabs and new line
print("\tOne\nTwo\n\tThree")

#stripping white space temporarily
white_space = "   white space    "
print(white_space + "!")
print(white_space.rstrip() + "!")
print(white_space.lstrip() + "!")
print(white_space.strip() + "!")

#stripping white space permanently
white_space = white_space.strip()
print(white_space + "!")

#avoiding type erros with str()
age = 25
age_statement = "I am " + str(age)
print(age_statement)

#lists, inserting news items
climbing_brands = ['Evolv']
#append adds to end of list
climbing_brands.append('La Sportiva')
#insert, into a specifc position
climbing_brands.insert(0, 'Scarpe')
print(climbing_brands)
#changing a value when you know the position
climbing_brands[0] = 'Scarpa'

#printing first in list
print(climbing_brands[0])

#print last in list
print(climbing_brands[-1])

print("null")
#deleting from list
del climbing_brands[-1] #use del for position
climbing_brands.remove('Evolv') #use .remove() when you don't know the position but know the name/value
print(climbing_brands)
climbing_brands.append('La Sportiva')
climbing_brands.insert(-1, 'Evolv')

#popping
print(climbing_brands)
myshoes = climbing_brands.pop()
print(climbing_brands)
print("I own a pair of " + myshoes.title() + "'s")
	#you can also pop from any position, eg. climbing_brands.pop(1)

#organizing lists, permanently
climbing_brands.sort()
print(climbing_brands)

climbing_brands.sort(reverse=True)
print(climbing_brands)

#organizing lists, temporarily
gear_climbing = ['shoes', 'chalk', 'brush', 'quickdraws', 'file']
print(sorted(gear_climbing))

gear_climbing.sort()
gear_climbing.reverse()
print(gear_climbing)

#finding the length of a list
print(len(gear_climbing))
print("I have " + str((len(gear_climbing))) + " pieces of climbing equipment.")

#looping
colors = ['red', 'blue', 'green', 'black', 'brown']
for color in colors:
	print(color.title() + ", is it your favorite color?")
	print("Why is " + color.title() + " your favorite color?")
#this code reads: for every color in the list of colors, print the color

#another example of looping
pizzas = ['cheese', 'pepperoni', 'ham', 'hawaiian', 'sausage']
for pizza in pizzas:
	print("I like " + pizza + " pizza.")

#using range()
#printing out all values in a range
for value in range(1,3):
	print(value)

#making a list froma a range of numbers
numbers = list(range(1,6))
print(numbers)

#skiping numbers through range()
evens = list(range(2,15,2))
print(evens)
#range is 2-15, adds 2 to that value til 15

#example for squares, from 1 to 10
squares = []
for value in range(1,11):
	square = value**2 #** represents exponents
	squares.append(square)
print(squares)


#simple stats
print('Simple Stats')

digits = list(range(2,10))
print(digits)
print(min(digits))
print(max(digits))
print(sum(digits))

#list comprehensions
squares = [x**2 for x in range (1,11)]
print(squares)

#slicing a list
print(pizzas)
print(pizzas[0:4])
print(pizzas[:3]) #begins at the beginning
print(pizzas[2:]) #begins at third item in list
print(pizzas[-2:]) #gives the last two items in list
print(pizzas[:-2]) #gives first 3 items of list

#looping with a slice
for pizza in pizzas[:3]:
	print(pizza.title())

#copying a list
my_foods = pizzas[:]
#writing my_foods = pizzas, would connect the two variables
friends_foods = my_foods[:]
print(friends_foods)

newfood = ['spinich', 'buffalo']
friends_foods.append(newfood) #appending a list because we cannot append more than one variable in a statement

print(friends_foods)

#example
clothes = ['shirts', 'pants', 'shoes', 'shorts', 'tanks']
print('I own exactly three articles of')

for x in clothes[-3:]: #printing the last 3
	print(x)

#appending a variable through a single append, and a list loop
clothes.append('jeans')
clotheslist = 'underwear', 'hats'
for a in clotheslist:
	clothes.append(a)

print('After last weekend though, I now own 5 of')
for clothesthing in clothes:
	print(clothesthing)

#endexample

#tuples, values that cannot change. basically use parentheses instead of brackets
rectangle = (500, 200)
print('The dimensions of the rectangle are ' + str(rectangle[0]) + ' by ' + str(rectangle[1]) + ".")
for sides in rectangle:
	print(sides)

#style guide
	#4 spaces per tab, make sure your tab is inserting spaces
	#line length should be less than 80 characters
	#limit comments to 72 characsters per line
	#use blank lines! but not excessively

#IF AND ELSE YALL
cars = ['bmw', 'audi', 'toyota', 'honda']
	#this will print bmw as BMW, and all others as 'title()d'
for car in cars:
	if car == 'bmw':
		print(car.upper())
	else:
		print(car.title())
	#car == 'bmw' is asking if the values match?

#case matters
car = 'Audi'
print(car == 'audi')
	#when you don't care about case
print(car.lower() == 'audi')

age = 18
if age >= 21:
	print("You old enough, boy!")
else:
	print("Maybe next year!")

#inequality, when you want to know if two values are NOT equal
pizza_topping = 'salami'
if pizza_topping != 'mushroom':
	print('Not the topping I wanted, bro')
	#if pizza topping is not 'salami', the print will happen

#math comparisons
age = 21
print(age < 20)
print(age > 15)
print(age <= 21)
print(age >= 20)

#checking conditions
age1 = 22
age2 = 24
	#and
print(age1 >= 21 and age2 >= 21)
	#or
print(age1 >= 24 or age2 >= 1)

#if blank is not in the list, then:
banned = ['jack', 'michael', 'sam']
user = 'john'
if user not in banned:
	print(user.title() + ", you ain't banned baby.")

#if-elif-else chain
age = 5

if age < 2:
	stage = "baby"
elif age < 4:
	stage = 'toddler'
elif age < 20:
	stage = 'teenager'
elif age < 65:
	stage = 'adult'

print('You are currently a ' + str(stage) + '.')

#using multiple ifs
drinks = ['beer', 'soda']

if 'beer' in drinks:
	print('Beer coming out!')
if 'soda' in drinks:
	print('Soda coming out!')
if 'milk' in drinks:
	print('Milk coming out!')

#ctrl + H = FIND/REPLACE

#lists and if statements
topping = ['cheese', 'tomato', 'salami', 'pineapple']

for requested in topping:
	if requested == 'cheese':
		print("Sorry, we are out of cheese!")
	else:
		print("Adding " + requested + " to your pizza!")

print("\nYour pizza is complete!")

#checking if a list is empty
topping = []

if topping:
	for requested in topping:
		print("Adding " + requested + " to your pizza.") 
	print("Pizza is done!")
else:
	print("Are you sure you want a plain pizza?")
	#when there is an item in the list, python will run the if statement -- if the list is empty, python will run the ELSE statement
	
