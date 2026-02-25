'''Simple Program to calculate NRR'''

while True:
    print("Program to calculate NRR after Zimbabwe Match of India")
    forrunsIndia, againstrunsIndia, foroversIndia, againstoversIndia = 111, 187, 20, 20
    a = int(input("Is India is batting first? Enter 1 for yes & 2 for no. = ", ))
    if a == 1:
        print(f"Enter India's Score or expected score =  ")
        indscore = int(input())
        print(f"Enter Zimbabwe's Score or expected score =  ")
        zimscore = int(input())
        NrrIndia = (((indscore + forrunsIndia) / (foroversIndia + 20)) - ((zimscore + againstrunsIndia)) / (
                    againstoversIndia + 20))
        print(f"India's NRR after win against Zimbabwe will be =  ", f"{NrrIndia:.3f}")
    elif a == 2:
        print("Enter Zimbabwe's Score or expected score = ")
        zimscore = int(input())
        print("Enter number of overs for India to achieve target = ")
        indovers = float(input())
        NrrIndia = (((zimscore + 1) + forrunsIndia) / (indovers + 20)) - (
                    (zimscore + againstrunsIndia) / (againstoversIndia + 20))
        print(f"India's NRR after win against Zimbabwe will be =  ", f"{NrrIndia:.3f}")
    else:
        print("Invalid input, Please Try again ")
        continue
    print("\n__")
    retry = input("Do you want to calculate another scenario? (type 'y' for yes, 'n' to quit): ")
    if retry.lower() != 'n':
        continue
    else:
        print("Thanks for using the NRR Calculator. Goodbye!")
        break
