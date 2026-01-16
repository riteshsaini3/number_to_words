# number_to_words
def number_to_words(n):
     ones = ["", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"]
     teens = ["ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "eighteen", "nineteen"]
     tens = ["", "", "twenty", "thirty", "forty", "fifty", "sixty", "seventy", "eighty", "ninety"]

if n == 0:
   return "Zero"

words = ""

if n >= 1000:
  words += ones[n // 1000] + "thousand"
  n = n % 10

elif n >= 20:
  words += tens[n // 10] + " "
  n = n % 10

elif n >= 10:
  word += teens[n - 10] + " "
  n = 0

if n > 0:
  words += ones[n] + " "

return words.strip()

num = int(input("Enter any number: "))
print("spelling:", number_to_words(num))