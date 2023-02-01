# Jaka to liczba?
#
# Komputer wybiera losowo liczbę z zakresu od 1 do 100.
# Gracz próbuje ją odgadnąć, a komputer go informuje,
# czy podana przez niego liczba jest: za duża, czy za mała,
# prawidłowa.

import random

print("\tWitaj w grze 'Jaka to liczba'!")
print("\nMam na myśli pewną liczbę z zakresu od 1 do 100.")
print("Spróbuj ją odgadnąć w 5 próbach.\n")

# ustaw wartości początkowe
the_number = random.randint(1, 100)
guess = int(input("Ta liczba to: "))
tries = 1

# pętla zgadywania
while guess != the_number and tries <5:

    if guess == the_number:
        break

    if guess > the_number:
        print("Za duża...")
    else:
        print("Za mała...")
    print("To Twoja ", tries, "próba. Zostały Ci ", 5 - tries, "próby!")

    tries += 1
    guess = int(input("Ta liczba to: "))

if guess == the_number:
    print("Odgadłeś! Ta liczba to ", the_number)
    print("Do odgadnięcia potrzebowałeś tylko", tries, "prób!")
    
else:
    print("Skończyły Ci się próby. Przegrałeś...")
    print("Ta liczba to ", the_number)

input("\n\nAby zakończyć program, naciśnij klawisz Enter.")

