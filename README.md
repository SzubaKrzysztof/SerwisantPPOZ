Roadmap do Budowy Aplikacji Webowej do Przeglądów Sprzętu Przeciwpożarowego
Ten roadmap opisuje kroki niezbędne do stworzenia aplikacji webowej wspierającej serwisantów w przeprowadzaniu przeglądów sprzętu przeciwpożarowego, takiego jak hydranty, węże i gaśnice. Aplikacja będzie zawierać system uwierzytelniania użytkowników, wybór modułów, zarządzanie sprzętem i klientami, generowanie raportów oraz system powiadomień. Backend będzie oparty na Supabase, frontend na React, a w przyszłości planowane jest stworzenie aplikacji mobilnej na Androida z użyciem React Native.

Spis Treści
Planowanie Projektu
Stack Technologiczny
Konfiguracja Środowiska Deweloperskiego
System Uwierzytelniania
Struktura Głównej Aplikacji
Rozwój Modułów
Operacje CRUD
Zarządzanie Informacjami o Firmie
System Raportowania
System Powiadomień
Testowanie
Wdrożenie
Przyszłe Rozszerzenia
1. Planowanie Projektu
a. Definicja Wymagań
Identyfikacja Funkcjonalności: Lista wszystkich potrzebnych funkcji, takich jak logowanie, rejestracja, wybór modułów, zarządzanie sprzętem i klientami, raportowanie oraz powiadomienia.
Role Użytkowników: Określenie różnych ról użytkowników (np. Administrator, Serwisant) oraz ich uprawnień.
Modele Danych: Opracowanie modeli danych dla sprzętu, klientów, przeglądów i użytkowników.
b. Projektowanie UI/UX
Wireframy: Tworzenie wireframów dla każdego ekranu, aby zobrazować układ i przepływ użytkownika.
Doświadczenie Użytkownika: Zapewnienie intuicyjności i łatwości nawigacji aplikacji dla serwisantów.
c. Ustalanie Kamieni Milowych
Harmonogram: Opracowanie harmonogramu projektu z wyraźnymi kamieniami milowymi i terminami.
Podział Zadań: Rozbicie projektu na mniejsze zadania i przypisanie priorytetów.
2. Stack Technologiczny
Frontend
Framework: React
Język: TypeScript (zalecane dla bezpieczeństwa typów)
Zarządzanie Stanem: Redux lub Context API
Routing: React Router
Biblioteka UI: Material-UI lub Tailwind CSS dla spójnego stylu
Backend
Platforma: Supabase
Baza Danych: PostgreSQL
Uwierzytelnianie: Supabase Auth
Przechowywanie Danych: Supabase Storage dla przesyłania plików
Realtime: Supabase Realtime dla aktualizacji na żywo
Powiadomienia
Email: SendGrid lub integracja z email w Supabase
SMS: Twilio lub inny dostawca usług SMS
Raportowanie
Generowanie PDF: Biblioteki takie jak jsPDF lub PDFKit
Wdrożenie
Hosting Frontend: Vercel lub Netlify
Hosting Backend: Supabase zarządza usługami backendowymi
Kontrola Wersji
Repozytorium: GitHub lub GitLab
Przyszła Aplikacja Mobilna
Framework: React Native
3. Konfiguracja Środowiska Deweloperskiego
a. Inicjalizacja Frontend
Utworzenie Projektu React: Użyj create-react-app z TypeScript.
Instalacja Zależności: Zainstaluj potrzebne biblioteki do routingu, zarządzania stanem i stylizacji.
b. Konfiguracja Supabase
Utworzenie Projektu Supabase: Zarejestruj się i utwórz nowy projekt na Supabase.
Konfiguracja Bazy Danych: Ustaw tabele dla użytkowników, sprzętu, klientów, przeglądów itp.
Instalacja Klienta Supabase: Dodaj klienta Supabase do projektu frontendowego.
c. Kontrola Wersji
Inicjalizacja Git: Zainicjuj repozytorium Git i połącz zdalne repozytorium.
Pierwszy Commit: Dodaj początkowy kod do repozytorium i wykonaj pierwszy commit.
4. System Uwierzytelniania
a. Tworzenie Ekranów Uwierzytelniania
Ekran Powitalny: Strona startowa z przyciskami Logowania i Rejestracji.
Ekran Logowania: Formularz do wprowadzania danych logowania.
Ekran Rejestracji: Formularz do rejestracji nowych użytkowników.
b. Integracja Supabase Auth
Konfiguracja Klienta Supabase: Inicjalizacja Supabase w aplikacji React.
Implementacja Logiki Uwierzytelniania: Wykorzystanie metod Supabase Auth do rejestracji, logowania i wylogowywania użytkowników.
c. Ochrona Tras
Guardy Tras: Zapewnienie, że tylko uwierzytelnieni użytkownicy mają dostęp do głównych części aplikacji.
Przekierowania: Przekierowanie nieautoryzowanych użytkowników na ekran logowania.
5. Struktura Głównej Aplikacji
a. Dashboard
Wybór Modułu: Przycisk lub menu umożliwiające wybór różnych modułów (Hydrant, Wąż, Gaśnica).
Responsywny Design: Zapewnienie dostępności dashboardu na różnych urządzeniach.
b. Nawigacja
Sidebar lub Górna Nawigacja: Implementacja spójnej nawigacji na wszystkich ekranach.
Breadcrumbs: Opcjonalnie dla lepszej orientacji użytkownika.
6. Rozwój Modułów
a. Moduł Hydrantów
Lista Hydrantów: Wyświetlanie listy hydrantów z ich statusami.
Formularze Przeglądu: Tworzenie formularzy do rejestrowania szczegółów przeglądu.
b. Moduł Wężów
Lista Wężów: Wyświetlanie inwentarza węży i ich statusów.
Formularze Przeglądu: Formularze do przeglądów węży.
c. Moduł Gaśnic
Lista Gaśnic: Wyświetlanie gaśnic z odpowiednimi danymi.
Formularze Przeglądu: Formularze do przeglądów gaśnic.
d. Komponenty Wielokrotnego Użytku
Formularze: Tworzenie wielokrotnego użytku komponentów formularzy do dodawania/edytowania sprzętu.
Tabele: Komponenty tabel do wyświetlania list elementów.
7. Operacje CRUD
a. Dodawanie Sprzętu
Ekran Dodawania Sprzętu: Formularz do dodawania nowych hydrantów, węży lub gaśnic.
Walidacja Formularzy: Zapewnienie poprawności wprowadzanych danych.
b. Edytowanie Sprzętu
Ekran Edytowania Sprzętu: Możliwość modyfikacji istniejących danych sprzętu.
Powiązanie Danych: Wstępne wypełnienie formularzy istniejącymi danymi.
c. Zarządzanie Klientami
Dodawanie/Edycja Klientów: Formularze do dodawania lub aktualizacji informacji o klientach.
Lista Klientów: Wyświetlanie listy klientów z opcjami edycji lub usuwania.
8. Zarządzanie Informacjami o Firmie
a. Ekran Nazwy Firmy
Wyświetlanie/Edycja Nazwy Firmy: Możliwość ustawienia lub aktualizacji nazwy firmy przez administratorów.
Walidacja: Zapewnienie, że nazwa firmy spełnia wymagane kryteria.
b. Dodatkowe Informacje
Dane Kontaktowe: Opcjonalnie dodanie informacji kontaktowych i adresu firmy.
9. System Raportowania
a. Generowanie Raportów
Szablony Raportów: Projektowanie szablonów raportów przeglądów.
Integracja Danych: Uzupełnianie raportów danymi z bazy danych.
b. Generowanie PDF
Implementacja Bibliotek PDF: Wykorzystanie bibliotek do generowania plików PDF z raportami.
Opcje Pobierania i Druku: Umożliwienie użytkownikom pobierania lub drukowania raportów.
c. Przechowywanie Raportów
Zapis Raportów: Opcjonalne przechowywanie wygenerowanych raportów w Supabase Storage dla przyszłego dostępu.
10. System Powiadomień
a. Powiadomienia w Aplikacji
Nadchodzące Przeglądy: Wyświetlanie powiadomień w aplikacji o zbliżających się terminach przeglądów sprzętu.
Aktualizacje w Czasie Rzeczywistym: Wykorzystanie Supabase Realtime do natychmiastowego przesyłania powiadomień.
b. Powiadomienia Email
Integracja z Usługą Email: Użycie SendGrid lub funkcji email w Supabase.
Automatyczne Emaili: Wysyłanie emaili do klientów z informacjami o nadchodzących terminach przeglądów.
c. Powiadomienia SMS
Integracja z Usługą SMS: Integracja z Twilio lub innym dostawcą usług SMS.
Automatyczne SMS-y: Wysyłanie powiadomień SMS do klientów o nadchodzących terminach przeglądów.
d. Harmonogram Powiadomień
Zadania Harmonogramowe: Ustawienie zadań harmonogramowych do wysyłania powiadomień w odpowiednich terminach.
11. Testowanie
a. Testy Jednostkowe
Testy Frontendowe: Użycie Jest i React Testing Library do testowania komponentów React.
Testy Backendowe: Testowanie funkcji Supabase i interakcji z bazą danych.
b. Testy Integracyjne
Testy End-to-End: Użycie narzędzi takich jak Cypress do symulowania interakcji użytkowników i zapewnienia poprawnej współpracy wszystkich komponentów.
c. Testy Akceptacyjne Użytkownika
Beta Testowanie: Przeprowadzenie testów z udziałem grupy użytkowników i zbieranie opinii.
12. Wdrożenie
a. Wdrożenie Frontendu
Wybór Platformy Hostingowej: Wdrożenie aplikacji React na Vercel lub Netlify.
Ciągłe Wdrożenie: Konfiguracja CI/CD do automatycznych wdrożeń przy każdym pushu.
b. Wdrożenie Backend
Hosting w Supabase: Supabase zarządza usługami backendowymi; upewnij się, że wszystkie zmienne środowiskowe są poprawnie ustawione.
c. Konfiguracja Domeny
Domena Własna: Skonfiguruj własną domenę dla aplikacji.
d. Certyfikaty SSL
Bezpieczne Połączenia: Zapewnienie, że aplikacja korzysta z HTTPS dla bezpiecznego przesyłania danych.
13. Przyszłe Rozszerzenia
a. Aplikacja Mobilna
Rozwój w React Native: Rozpoczęcie planowania i tworzenia aplikacji na Androida z użyciem React Native.
Wspólna Baza Kodu: Wykorzystanie wspólnych komponentów i usług między aplikacją webową a mobilną tam, gdzie to możliwe.
b. Zaawansowane Funkcje
Wsparcie Offline: Umożliwienie dostępu do danych w trybie offline i synchronizacji po przywróceniu połączenia.
Dashboard Analityczny: Implementacja analityki do śledzenia trendów przeglądów i wydajności.
Kontrola Dostępu oparta na Rolach: Zwiększenie bezpieczeństwa poprzez bardziej szczegółowe uprawnienia użytkowników.
c. Skalowalność
Optymalizacja Wydajności: Ciągłe monitorowanie i poprawa wydajności aplikacji.
Optymalizacja Bazy Danych: Zapewnienie skalowalności bazy danych Supabase wraz ze wzrostem ilości danych i użytkowników.
