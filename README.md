class Colors:
    RED = '\033[91m'
    GREEN = '\033[92m'
    YELLOW = '\033[93m'
    BLUE = '\033[94m'
    MAGENTA = '\033[95m'
    CYAN = '\033[96m'
    WHITE = '\033[97m'
    END = '\033[0m'
#wstep----------------

print(f' {Colors.BLUE}wybierz swoje imie:')
print('imie do wyboru -> Mikolaj')
print('imie do wyboru -> Hania')
print('imie do wyboru _> Ignacy')
#inp--------------------
wybierz_imie_swej_postaci = input('wybierz imie swej postaci:')
#postacie--------------------
a = (input) 

b = (input)

c = (input)

d = (input)
#ludwik-------------------
if wybierz_imie_swej_postaci == 'Mikolaj':
    print(f'{Colors.GREEN}Wybrane przez ciebie imie to Mikolaj. Czy chcesz usłyszec w jakiej sytaucji sie znajduje aktualnie? ')
#IFNORMACJE O LUDWIKU
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Mikolaj Gorny - tak walsnie sie nazywa dokladnie twoja postac. Pracuje ona aktualnie w ksiegowosci, lecz mysli nad zmiana pracy do firmy zajmujacej sie kryptowaluta. Czy chcesz do niej przejsc?')
    elif opcja == 'nie':
        print('Niestety podjales zla decyzje. W tej grze wazne sa szczegoly. Bedzie ci pozniej trudno podejmowac decyzje, lecz wciaz masz szanse wygrac.')
    elif opcja:
        print('Wybierz dobra opcje!!!')
#PRACA LUDWIKA
    opcja = input("Wybierz opcję (wpisz 'tak' lub 'nie'): ")
    if opcja == 'tak':
            print('Postapiles ryzykownie, gdyz ta branza jest dosc ryzykowna. ')
            print('Juz pierwszego dnia odkryles potecjal kryptowaluty ETHERIUM. Postanowiles kupic ja za wszystkie udzialy firmy, a to cie stracilo. Twoj szef ma cie za nieodpowiedzialnego, wiec cie zwolnil. Wracajac do domu spotakal cie niespodziewana sytuacja. Napadli na ciebie drilowcy. Chcesz sie bic?')

    elif opcja == 'nie':
        print('Ze smutku przez fakt, ze odrzuciles decyzje postanawiasz wczesniej wrocic do domu. Po drodze napada na ciebine trzech oseidlowych drillowcow. Zamierzasz sie bic?')
    elif opcja:
        print('Wybierz dobra opcje!!!')
#BITWA
    opcja = input(f"Wybierz opcję (wpisz 'tak' lub 'nie'):{Colors.YELLOW} ")
    if opcja == 'tak':
            from random import randint, choice
            life = 10
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


    print("-"*40)
    print("KONIEC GRY!")
    print(f"Zabiłeś {liczba_pokonanych_przeciwników} drilowcow  ")
    if liczba_pokonanych_przeciwników == 0:
        print('Porazka!!! Przegrales!!!')
    if liczba_pokonanych_przeciwników == 1:
        print('Brawoo, odtad zyjesz spokojnym  zyciem.')
#SMIERC PRZY USATWCE MIKOLAJA
    elif opcja =='nie':
        print(f'{Colors.RED}Jestes skonczony... drilowcy wgniataja cie w glebe.{Colors.RED}')
    elif opcja:
        print('Wybierz dobra opcje!!!')
#BOZENA--------------------

elif wybierz_imie_swej_postaci == 'Hania':
    print(f'{Colors.GREEN}Jestes nauczycielka w szkole, pracujesz juz w niej ponad 11lat. Dzieci powoli zaczynaja cie wykanczac. Zarabiasz niewielka kwote, aktualnie na koncie masz 127,65zlotowek. Jestes przy upadku psychiki.{Colors.RED}')
    



   
    import threading
    import time

    class Postac:
        def __init__(self, hp):
            self.hp = hp
            self.running = True

        def run(self):
            while self.running and self.hp > 0:
                time.sleep(5)
                self.trac_hp(10)

            if self.hp <= 0:
                print("Porażka - Zdrowie psychiczne spadło do zera!")

        def trac_hp(self, amount):
            self.hp -= amount
            print(f"Zdrowie psychiczne: {self.hp} HP")

        def stop(self):
            self.running = False

    moja_postac = Postac(hp=500)

    watek_postaci = threading.Thread(target=moja_postac.run)
    watek_postaci.start()


    

#----------------------------------------------------------------------------------
    
    
    print(f'{Colors.END}Pewnego razu napadaja na ciebie zamaskowani uczniowie, rzadaja od ciebie 150zloty, co zamierzasz robic? Oddasz im czy nie?')
    opcja = input("Wybierz opcję (wpisz 'oddaje' lub 'nie oddaje'): ")
    if opcja == 'oddaje':
            print(f'{Colors.RED}Nie masz takiej kwoty! Zostajesz pobita, a twoj stan psychiczny jest u schylku wytrzymalosci!')
            moja_postac.trac_hp(480)
            print(f'{Colors.END}')

    elif opcja == 'nie oddaje':
        print('Postanawiasz uciekac, niestety oni cie doganiaja. Jedyna opcja na przetrwanie jest walka...')
        from random import randint, choice
    elif opcja:
        print(f'Wybierz dobra opcje!!!{Colors.YELLOW}')

        life = 13
        zlotowki = 127,65
        def atak_torebka():
            return randint (2,3)
        def reka():
            global zlotowki
            if zlotowki < 4:
                print("-"*40)
                print("Nie masz wystarczającej ilości zlotwoek!")
                return 0
            zlotowki -= 0
            return randint(29, 29)
        def wybierz_atak():
            print('A - torebka')
            print('b/B - piescia')
            co = input().upper()
            if co == 'A':
                return atak_torebka()
            elif co == 'B':
                return reka()
            else:
                print("Nie wybrano dobrego wyboru")
            return 0

        def drilowcy():
            opponents = [
                ["zamaskowany napastnik", 100, 3, 0],
                ["zamaskowany napastnik", 199, 3, 0]
            ]
            return choice(opponents)
        liczba_pokonanych_przeciwników = 0


        while life > 0:
            opponent = drilowcy()
            print("-"*40)


            while opponent[1] > 0 and life > 0:
                print(f"Hania walczy teraz z {opponent[0]}") 
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


        print("-"*40)
        print(f"{Colors.RED}KONIEC GRY!")
        print(f"Zabiłeś {liczba_pokonanych_przeciwników} napastnikow!")
        if liczba_pokonanych_przeciwników == 0:
            print('Porazka!!! Przegralas!!!')

        elif liczba_pokonanych_przeciwników == 1:
            print('Udalo ci sie, ')
#---------------------------------------------------------
elif wybierz_imie_swej_postaci == 'Ignacy':
    print(f'Jestes Ignacy. Wszyscy sie ciebie boja. Idziesz wlasnie wyjasnic sprawe z Mackiem, ktory sie tobie ostatnio sprzeciwial.{Colors.YELLOW}')
from random import randint, choice

life = 13
zlotowki = 127.65

def atak_bronia():
    return randint(2, 3)

def reka():
    global zlotowki
    if zlotowki < 4:
        print("-" * 40)
        print("Nie masz wystarczającej ilości złotówek!")
        return 0
    zlotowki -= 4
    return randint(2, 9)

def wybierz_atak():
    print('A - bronia')
    print('B - piescia')
    co = input().upper()
    if co == 'A':
        return atak_bronia()
    elif co == 'B':
        return reka()
    else:
        print("Nie wybrano dobrego wyboru")
    return 0

def macko():
    return ["Macko", 100, 3, 0]

liczba_pokonanych_przeciwników = 0

while life > 0:
    opponent = macko()
    print("-" * 40)

    while opponent[1] > 0 and life > 0:
        print(f"Ignacy walczy teraz z {opponent[0]}")
        print(f"{opponent[0]} ma {opponent[1]} HP i zadaje Ci {opponent[2]} obrażeń")

        life -= opponent[2]
        if life <= 0:
            print(f"Masz {life} HP i {zlotowki} złotówek")
        atak = wybierz_atak()
        opponent[1] -= atak
        print(f"Zadałeś {atak} obrażeń")

    if opponent[1] <= 0:
        print('Zabiłeś przeciwnika!!!')
        liczba_pokonanych_przeciwników += 1

print("-" * 40)
print("KONIEC GRY!")
print(f"Zabiłeś {liczba_pokonanych_przeciwników} napastników!")

if liczba_pokonanych_przeciwników == 0:
    print('Porażka!!! Przegrałaś!!!')
elif liczba_pokonanych_przeciwników == 1:
    print(f'Udało ci się!{Colors.GREEN}')
    print(f'Uwaga!! To nie koniec, nadchodza jego koledzy!!!{Colors.YELLOW}')
from random import randint, choice

life = 13
zlotowki = 127.65

def atak_szybki():
    return randint(2, 3)

def atak_reka():
    global zlotowki
    if zlotowki < 4:
        print("-" * 40)
        print("Nie masz wystarczającej ilości złotówek!")
        return 0
    zlotowki -= 4
    return randint(2, 9)

def wybierz_atak():
    print('A - szybki atak')
    print('B - piescia')
    co = input().upper()
    if co == 'A':
        return atak_szybki()
    elif co == 'B':
        return atak_reka()
    else:
        print("Nie wybrano dobrego wyboru")
    return 0

def kolegowie():
    return ["Kolega", 100, 3, 0]

liczba_pokonanych_przeciwników = 0

while life > 0:
    opponent = kolegowie()
    print("-" * 40)

    while opponent[1] > 0 and life > 0:
        print(f"Ignacy walczy teraz z {opponent[0]}")
        print(f"{opponent[0]} ma {opponent[1]} HP i zadaje Ci {opponent[2]} obrażeń")

        life -= opponent[2]
        if life <= 0:
            print(f"Masz {life} HP i {zlotowki} złotówek")
        atak = wybierz_atak()
        opponent[1] -= atak
        print(f"Zadałeś {atak} obrażeń")

    if opponent[1] <= 0:
        print('Zabiłeś przeciwnika!!!')
        liczba_pokonanych_przeciwników += 1


print("-" * 40)
print("KONIEC GRY!")
print(f"Zabiłeś {liczba_pokonanych_przeciwników} kolegów!")

if liczba_pokonanych_przeciwników == 0:
    print('Porażka!!! Przegrałaś!!!')
elif liczba_pokonanych_przeciwników == 1:
    print('Udało ci się! Juz teraz tylko wypoczywac.')
