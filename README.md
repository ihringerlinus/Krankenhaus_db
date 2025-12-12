# Krankenhaus_db
Voraussetzungen:

Software:
Python
PostgreSQL ≥ 14
pgAdmin 4

Python Packages
pip install psycopg2 faker

PostgreSQL Setup:
Host: localhost
Port: 5432
Database: krankenhaus
User: postgres
Password: postgres
Diese Parameter sind im Code fix gesetzt und müssen ggf. angepasst werden.

Notebook-Struktur:
Das Projekt besteht aus mehreren Jupyter Notebooks mit klarer Trennung der Verantwortlichkeiten:
1:Database Setup Notebook
    Zweck:
        Drop aller Tabellen
        Create Tables 
        Befüllung der Datenbank mit Fake-Daten
        Wichtig:
        Muss immer zuerst ausgeführt werden
        Enthält faker-basierte Seed-Daten

2️: Use Case – Personalabfragen
    Zweck:
    Abfragen für Ärzte & Pflegekräfte
    
3️: Use Case – Verwaltungsabfragen
    Zweck:
    Administrative / organisatorische SQL-Abfragen

Zentrale Parameter:
Zentrale Paramenter sind immer am Anfang des Notebooks hard gecoded können aber angepasst werden
z.B. für das Personalabfragen jupiter note book:
ARZT_ID = 1
PFLEGEKRAFT_ID = 1
TODAY = '2025-12-12'

Alle Abfragen passen sich automatisch an diese Werte an.

Ausführung:
PostgreSQL starten
Datenbank krankenhaus erstellen
Database Setup Notebook komplett ausführen
Danach beliebige Use-Case-Notebooks starten
