# Aplicație JavaSpringBoot/JavaFX
**Autor**: Marin Valentin-Gabriel 432B

## Introducere
Aplicația prezentată este dezvoltată utilizând Java Spring Boot pentru backend și JavaFX pentru frontend, cu CSS pentru stilizare. Aceasta gestionează o relație de tip N:M între două entități: clienți și posturi TV. Proiectul îmbină avantajele unei arhitecturi moderne bazate pe Spring Boot, oferind un backend robust și scalabil, cu o interfață grafică prietenoasă și ușor de utilizat dezvoltată cu JavaFX.

## Tehnologii utilizate
- **Java Spring Boot**: Framework-ul Spring Boot este folosit pentru a dezvolta backend-ul aplicației. Acesta oferă o configurare rapidă, suport pentru REST API-uri și integrare facilă cu MySQL.
- **JavaFX și CSS**: JavaFX este utilizat pentru a crea o interfață grafică modernă și responsivă. CSS este folosit pentru a personaliza design-ul elementelor din aplicație.
- **MySQL**: Baza de date utilizată este MySQL, iar conexiunea cu aplicația a fost realizată folosind biblioteca mysql-connector.

## Descrierea aplicației
Aplicația gestionează relația N:M dintre două entități principale:
- **Clienți** - reprezentați prin atributele: nume, prenume și email.
- **Posturi TV** - fiecare având un nume și o descriere.

Funcționalitățile aplicației includ:
- CRUD (Create, Read, Update, Delete) pentru tabelele `clienti` și `posturitv`.
- Asocierea și dezasocierea entităților `clienti` și `posturitv` printr-o tabelă intermediară `clienti_posturi`.

## Diagrama bazei de date
Diagrama bazei de date reprezintă relația N:M dintre `clienti` și `posturitv` prin intermediul tabelei `clienti_posturi`. Aceasta a fost generată utilizând MySQL Workbench și poate fi accesată prin fișierul `MySQL_Diagram.html` din folderul resurse.

## Structura folderului aplicației
Structura completă a proiectului poate fi găsită în folderul resurse, sub denumirea `Structura_Proiect_Java.html`.

## Părți importante din cod

### Funcționalitățile CRUD:

#### Listare Client:
- Metoda `getAllClients()` obține lista tuturor clienților din backend printr-o cerere HTTP de tip GET.
- Construiește cererea HTTP și o trimite către backend pentru a obține răspunsul.
- Verifică statusul răspunsului HTTP și gestionează erorile.

#### Adăugare Client:
- Metoda `handleAdauga()` preia datele introduse de utilizator, validează datele și creează un obiect Client.
- Se apelează serviciul `ClientService` pentru adăugarea clientului în baza de date.
- Gestionarea excepțiilor și informarea utilizatorului.

#### Editare Client:
- Metoda `handleEdit(Client client)` deschide o fereastră pentru editarea unui client existent.
- Datele clientului sunt pre-umplute în formularul de editare.

#### Ștergere Client:
- Metoda `deleteClient(int id)` șterge un client din backend printr-o cerere HTTP de tip DELETE.
- Se trimite cererea către server și se verifică răspunsul.
- Gestionarea erorilor în cazul unui răspuns necorespunzător.

## Manual de instalare și utilizare

### Instalare JDK21:
1. Descarcti fișierul `jdk-21-windows-x64.exe` de pe siteul oficial JDK.
2. Rulați instalatorul și urmați pașii indicați.
3. Adăugați JDK 21 în PATH:
   - Deschideți setările de mediu (System Properties -> Environment Variables).
   - În variabila `Path`, adăugați calea către folderul bin al JDK (ex.: `C:\Program Files\Java\jdk-21\bin`).

### Instalare Maven:
1. Localizați folderul `Maven_Installer` din resurse.
2. Copiați folderul `apache-maven` în `C:\Program Files`.
3. Adăugați Maven în PATH:
   - În Environment Variables, adăugați calea către bin din folderul Maven (ex.: `C:\Program Files\apache-maven\bin`).

### Instalare Jackson:
1. Localizați folderul `jackson_Installer` din resurse.
2. Copiați fișierele Jackson în `C:\Program Files\Java`.
3. Adăugați Jackson în PATH:
   - În Environment Variables, adăugați calea către fișierele Jackson.

### Instalare JavaFX:
1. Localizați folderul `JavaFX_Installer` din resurse.
2. Copiați folderul `javafx-sdk` în `C:\Program Files\Java`.
3. Adăugați JavaFX în PATH:
   - În Environment Variables, adăugați calea către bin din folderul JavaFX.

### Instalare MySQL:
1. Descărcați și instalați MySQL Server 8.0.40 din folderul resurse sau de pe site-ul oficial MySQL.
2. Urmați pașii din asistentul de instalare:
   - Selectați „Server only” dacă nu aveți nevoie de alte componente MySQL.
   - Configurați serverul cu un nume de utilizator și parolă sigure.

### Configurare MySQL:
1. Deschideți MySQL Workbench sau orice alt client MySQL.
2. Conectați-vă la server utilizând credențialele configurate în timpul instalării.
3. Creați o nouă bază de date și importați fișierul `db.sql` din folderul resurse.
4. Configurați fișierul `application.properties` din folderul backend:
   - Înlocuiți valorile cu datele tale pentru baza de date, utilizator MySQL și parolă.

### Rulare aplicație:
1. După ce ați verificat pașii de mai sus, rulați aplicația utilizând executabilul furnizat.
2. Dacă aplicația întâmpină probleme, verificați:
   - Serverul MySQL este pornit.
   - Datele din fișierul `application.properties` sunt corecte.
   - Variabilele de mediu (Path) sunt configurate corespunzător.

## Bibliografie
- Java SE Development Kit 21 Documentation, [Online]. Available: https://docs.oracle.com/en/java/javase/21/.
- Spring Boot Documentation, [Online]. Available: https://spring.io/projects/spring-boot.
- JavaFX Documentation, [Online]. Available: https://openjfx.io/.
- MySQL Documentation, [Online]. Available: https://dev.mysql.com/doc/.
- IEEE Conference Templates, [Online]. Available: https://www.ieee.org/conferences/publishing/templates.html.
- FasterXML, "Jackson Library Documentation," [Online]. Available: https://github.com/FasterXML/jackson.
- Apache Software Foundation, "Apache Maven Project Documentation," [Online]. Available: https://maven.apache.org/.
