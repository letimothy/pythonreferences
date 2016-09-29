# pythonreferences
This .py file is my personal reference for python commands.

Begin:

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

#lists
climbing_brands = ['Evolv']
climbing_brands.append('La Sportiva')
climbing_brands.insert(0, 'Scarpe')
print(climbing_brands)

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
