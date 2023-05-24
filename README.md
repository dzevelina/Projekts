# Projekts
# Šī darba doma ir izveidot Python kodu, kas ļauj izveidot anketu ar pieciem jautājumiem par jautrajiem faktiņiem. Katram jautājumam ir jānorāda atbilde, ko lietotājs ievada. Pēc anketas aizpildīšanas tiek aprēķināti punkti, kurus lietotājs ir nopelnījis, salīdzinot ievadītās atbildes ar pareizajām atbildēm. Galu galā tiek parādīti gan ievadītie jautājumi un atbildes, gan pareizās atbildes, kā arī punktu skaits, ko lietotājs ir ieguvis.

def izveidot_anketu():
    anketas_atbildes = []  # Tukšs saraksts, kur glabāsim atbildes
    pareizas_atbildes = [
        "22 stundas",
        "Zilonis",
        "Amazone",
        "Everests",
        "25 gadus"
    ]

    jautajumi = [
        "Cik stundas koala guļ dienā?",
        "Kāds ir vislielākais dzīvnieks pasaulē?",
        "Kā sauc pasaules lielāko upi?",
        "Kāds ir augstākais kalns pasaulē?",
        "Cik ilgi var dzīvot vidēji žirafe?"
    ]

    punkti = 0  # Sākotnēji nav iegūtu punktu

    for i, jautajums in enumerate(jautajumi):
        atbilde = input(jautajums + " ")
        anketas_atbildes.append(atbilde)

        # Salīdzina ievadīto atbildi ar pareizo atbildi un piešķir punktus
        if atbilde.lower() == pareizas_atbildes[i].lower():
            punkti += 1

    print("Paldies, ka aizpildījāt anketu!")
    print("Jūs nopelnījāt {} punktus!".format(punkti))

    print("Anketas rezultāti:")
    for i, atbilde in enumerate(anketas_atbildes):
        jautajums = jautajumi[i]
        pareiza_atbilde = pareizas_atbildes[i]
        print(jautajums + " Ievadītā atbilde: " + atbilde)
        print("Pareizā atbilde: " + pareiza_atbilde)

izveidot_anketu()
