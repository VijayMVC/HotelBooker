# HotelBooker
Hotel room booking system on the Android platform using Spring framework.

Done:

- [S/A] logowanie użytkownika [oauth2]
- [A] możliwość sprecyzowania terminu oraz ilości miejsc w pokoju (do wyszukiwania) (domyślnie system szuka pokoju na najbliższą noc dla 2 osób)
- [S] wystawienie Api umożlwiającego pobieranie listy hotelów (Hotele na sztywno zapisane w bazie danych, wysyłana jest informacja o hotelach/pokojach)
- [S/ A] możliwość sprecyzowania terminu oraz ilości miejsc w pokoju (do wyszukiwania) (domyślnie system szuka pokoju na najbliższą noc dla 2 osób)
- [A] wyświetlenie znalezionych wyników jako listView
- [S/A] Wyświetlenie informacji o wybranym pokoju (ilość miejsc, standard, usługi hotelowe, udogodnienia itp)
- [S/A] (new) Możliwość rezerwacji pokoju
- [S/A] wyszukanie hotelu w danym mieście
- [S/A] Sprawdzenie swoich rezerwacji
- [S/A] obsługa rezerwacji wybranego pokoju (oczekuje na weryfikację, oczekuje na wpłatę, zarezerwowane)
- [I] przygotowanie bootStrapa pod interferjs użytkownika
- [I] logowanie dla obsługi hotelu (oauth2)
- [I] możliwość zmiany stanów zamówień klientów
- [I] możliwość edytowania informacji o hotelu (opis/lokalizacja)
- [S/A] rejestracja dla użytkownika
- [I] możliwość konfiguracji pokojów, terminów, informacji o pokoju (ilość miejsc, standard, usługi hotelowe, udogodnienia, opis, lokalizacja)
- [S/A/I] galeria zdjęć Hotelu
- [S/A/I} system ocen/opinii pokoju
- [S] wysyłanie mailów z potwierdzeniem rezerwacji
- [S/A] możliwość aulowania zamówienia

!!!!!!!!!!!!!!!!MUST HAVE REQUIREMENTS DONE !!!!!!!!!!!!!!!!

Corner of hope:
- [A] wyświetlenie hotelów na mapie z pozycją w obrębie X Km 
- [A] uumozliwienie konfiguracji promienia wyszukiwania hotelów
- [I] wykorzystanie netSocketów do aktualizacji danych o zamówieniach
- [S/A] notyfikacja MQTT o zmianie stanu rezerwacji
- [A] filtrowanie list/hoteli (np. tylko tam, gdzie basen, czy tylko pokoje w konkretnym hotelu)
- [S/A] możliwość dodania hotelu do ulubionych


Improvements:
- Add room groups (Allow to add multiple room with same type), priority: Must Have [DONE]
- add drawer lay to filter
- refactor NetworkServiceImpl class

S - Serwer, A - Android, I - Interface




Założenia:

Założenia Android:
- logowanie/rejestracja dla użytkownika
- po zalogowaniu użytkownik widzi mapę z zaznaczonymi hotelami na mapie w obrębie X km od swojej aktualnej lokalizacji
- domyślnie system szuka pokoju na najbliższą noc dla 2 osób,
- możliwość podania innego terminu / ilosci osób
- możliwość przejrzenia listy hotelów, jako listView
- po kliknięciu na pin na mapie lub element na liście, użytkownik może otworzyć widok hotelu, gdzie może sprawdzić dostępność pokojów w danym terminie
- na osobnym widoku możliwe jest sprawdzenie statusu swoich rezerwacji (oczekuje na weryfikację, oczekuje na wpłatę, zarezerwowane)
- możliwość anulowania rezerwacji
- wyświetlanie informacji o pokoju (ilość miejsc, standard, usługi hotelowe, udogodnienia itp)

Opcjonalne:
- możliwość oceny hotelu
- opinie o hotelu
- notyfikacja MQTT o zmianie stanu rezerwacji
- galeria zdjęć hotelu
- filtrowanie list/hoteli (np. tylko tam gdzie basen)
- możliwość dodania hotelu do ulubionych
- wyszukanie hotelu w danym miescie

Założenia interface webowy
- Interface webowy, zrealizowany za pomocą jsp, Thymeleaf lub angular 2 (jeszcze nie zdecydowałem)
- interface kierowany do recepcji hotelu,
- jeden hotel = jedno konto = kilka pokojów
- możliwość konfiguracji pokojów, terminów, informacji o pokoju (ilość miejsc, standard, usługi hotelowe, udogodnienia, opis, lokalizacja)
- możliwość zmiany stanów zamówień klientów

Opcjonalne:
- wykorzystanie net socketów
- wysyłanie mailów z potwierdzeniem rezerwacji.

Założenia serwer:
- uwierzytelnianie za pomocą oauth2,
- Realizuje powyższe wymagania
- Spring Framework / Spring MVC
- JPA2 (Hibernate), postgress