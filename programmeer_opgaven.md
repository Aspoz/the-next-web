# Programmeeropgaven

(bedoeld voor studenten van jaar 2 en hoger)

Oefenen met functies:

## Les 1

## Fizzbuzz
Dit zou als een test kunnen worden gebruikt, als je dit niet binnen 5 minuten kunt oplossen in een programmeertaal naar keuze, dan niet geschikt voor app programmeren. 

Write a program that prints the numbers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".

```ruby
(1..100).each do |i|
  x = ''
  x << 'Fizz' if i%3==0
  x << 'Buzz' if i%5==0
  puts x=='' ? i : x
end
```

## Valuta converter
Maak een functie die een bedrag van euros omzet naar dollars

func euroToDollars (euros: Float) -> Float

## Omdraaien
Maak een functie die de inhoud van een array omdraait 

func reverse (toReverse: [Int]) -> [Int]

```ruby
numbers = [4,7,1,3,8,6,9,2]

def reverse a
  return a if a.size < 2
  reverse(a.drop(1)) + a.first(1)
end

p numbers
p reverse numbers
```

## Minimum en maximum
Maak een functie die uit een lijst van getallen het grootste en kleinste getal teruggeeft

func minAndMax (numbers: [Int]) -> (min: Int, max: Int)

```ruby
numbers = [4,7,1,3,8,6,9,2]

def min_max a_n
  min=max=a_n.[0]
  a_n.each do |n|
    min = n if n < min
    max = n if n > max
  end
  [min,max]
end

puts min_max numbers
```

## Faculteit
Faculteit is in de wiskunde in begrip dat gebruikt wordt als volgt: 
- De faculteit van 0 is 0
- De faculteit van 1 is 1
- De faculteit van 2 is 2 * 1 = 2
- De faculteit van 3 is 3 * 2 * 1 = 6
- De faculteit van 4 is 4 * 3 * 2 * 1 = 24
- De faculteit van 5 is 5 * 4 * 3 * 2 * 1 = 120

Maak een functie faculteit
func faculteit (number: Int) -> Int

```ruby
def faculteit n
  return n if n < 2
  n * faculteit(n-1)
end

puts faculteit 5
```
