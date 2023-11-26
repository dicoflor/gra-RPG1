print('wybierz swoje imie:')
print('imie do wyboru -> Maciek')
print('imie do wyboru -> Hania')
#--------------------
postac= input('wybierz imie swej postaci:')

#-------------------
if postac == 'Maciek':
    print('Wybrane przez ciebie imie to Maciek. Czy ma on zjesc sniadanie?')
        #--------------------------------------------------------
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Maciek je sniadanie ')
    elif opcja == 'nie':
        print('Maciek nie je sniadania ')
    #------------------------------------------------------------------
    print('Czy Maciek ma umyc zeby ')
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Maciek myje zeby i idzie do szkoly  ')


    elif opcja == 'nie':
        print('Maciek nie myje zebow i idzie do szkoly ')


    print("Maciek w drodze do szkoly spotyka gangsterow i jest skazany na bojke z nimi")  
    from random import randint, choice

    life = 100
    zlotowki = 40

    def punch_attack():
        return randint(10, 10)

    def escape():
        global zlotowki
        if zlotowki < 4:
            print("-" * 40)
            print("Nie masz wystarczającej ilości zlotwoek!")
            return 0
        zlotowki -= 4
        return randint(29, 29)

    def choose_attack():
        print('A - z piesci')
        print('B - ucieczka')
        action = input().upper()
        if action == 'A':
            return punch_attack()
        elif action == 'B':
            return escape()
        else:
            print("Nie wybrano dobrej akcji")
        return 0

    def generate_opponent():
        opponents = [
            ["x", 20, 3, 0],
            ["y", 15, 3, 0]
        ]
        return choice(opponents)

    liczba_pokonanych_przeciwnikow = 0

    while life > 0:
        opponent = generate_opponent()
        print("-" * 40)

        while opponent[1] > 0 and life > 0:
            print(f"Ludwik walczy teraz z {opponent[0]}") 
            print(f"Przeciwnik ma {opponent[1]} HP i zadaje Ci {opponent[2]} obrażeń")

            life -= opponent[2]
            if life <= 0:
                print(f"Masz {life} HP i {zlotowki} zlotowek")

            attack_damage = choose_attack()
            opponent[1] -= attack_damage
            print(f"Zadałeś {attack_damage} obrażeń")

        if opponent[1] <= 0:
            print('Zabiłeś przeciwnika!!!')
            liczba_pokonanych_przeciwnikow += 1

    print("-" * 40)
    print("KONIEC GRY!")
    print("Maciek wygrawa walke i udaje sie dalej szkoly ")
    print("Maciek ma dzis sprawdzian z matematyki i sie na niego nie nauczyl . Czy ma sciagac czy nie ?")

    opcja = input("Wybierz opcje (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
        print('Maciek sciaga caly sprawdzian i dostaje 5 ')

    elif opcja == 'nie':
        print('Maciek nie sciaga i jest uczciwy i dostaje 1')




#HANIA-------------------------------------------------------------------------------------------------------------
elif postac == 'Hania':
    print('Wybrane przez ciebie imie to Hania . Czy ma on zjesc sniadanie?')
        #--------------------------------------------------------
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Hania  je sniadanie i mam mniej czasu na dotarcie do szkoly ')
    elif opcja == 'nie':
        print('Hania  nie je sniadania i ma wiecej czasu na droge do szkoly  ')
    #------------------------------------------------------------------
    print('Czy Hania  ma zrobic makijaz od szkoly ')
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Hania  robi makijaz i ladnie wyglada   i idzie do szkoly  ')


    elif opcja == 'nie':
        print('Hania  nie robi makijazu  i idzie do szkoly ')
    
    print("Hania idzie na autobus ktorym jedzie bezposredniod do szkoly, jednakze w drodze na autobus spotyka drillowcow z ktorymi musi sie byc ale wie ze przegra niezaleznie od decyzji ktora podejmie  ")
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    #-----------------------------------------------------------------------------
    if opcja == 'tak':
                    from random import randint, choice
                    life = 50
                    zlotowki = 4
                    def atak_piescia():
                        return randint (3,5)
                    def ucieczka():
                        global zlotowki
                        if zlotowki < 4:
                            print("-"*40)
                            print("Nie masz wystarczającej ilości zlotwoek!")
                            return 0
                        zlotowki -= 0
                        return randint(29, 29)
                    def wybierz_atak():
                        print('A - z piesci')
                        print('b/B - ucieczka')
                        co = input().upper()
                        if co == 'A':
                            return atak_piescia()
                        elif co == 'B':
                            return ucieczka()
                        else:
                            print("Nie wybrano dobrej akcji")
                        return 0

                    def drilowcy():
                        opponents = [
                            ["Malik Montana", 100, 3, 0],
                            ["Drillowiec", 100, 3, 0]
                            ]
                        return choice(opponents)
                    liczba_pokonanych_przeciwników = 0


                    while life > 0:
                        opponent = drilowcy()
                        print("-"*40)


                    while opponent[1] > 0 and life > 0:
                        print(f"Ludwik walczy teraz z {opponent[0]}") 
                        print(f"Przeciwnik ma {opponent[1]} HP i zadaje Ci {opponent[2]} obrażeń")

                    life -= opponent[2]
                    if life <= 0:

                        print(f"Masz {life} HP i {zlotowki} zlotowek")
                        atak = wybierz_atak()
                        opponent[1] -= atak
                        print(f"Zadałeś {atak} obrażeń")


                    if opponent[1] <= 0:
                        print('Zabiłeś przeciwnika!!!')
                        liczba_pokonanych_przeciwników += 1
    elif opcja == 'nie':
         print('nie chcialas sie bic z drilowcami lecz jednak oni cie zauwazyli i cie bardzo mocno pobili i ')
    
    print("-"*40)
    print("KONIEC GRY!")    
