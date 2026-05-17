# PE Opdracht 2 - Verstraeten Jameson DVOA

Ik heb gekozen voor **Filament Shield** plug-in. 
Ik heb deze plug-in gekozen omdat deze in veel projecten kan gebruikt worden en in de echte wererld authorisatie enorm belangrijk is.
Met deze plug-in is er een volledig functgioneel, rolgebaseerd authorisatiesysteem (RBAC) ingewerkt in een ticket support systeem.


### Complexiteit

Qua complexiteit van deze plug-in vervolt deze plug-in de high complexity requirement omdat:
* Spatie dependency en database migraties: Voordat Shield werkt heeft het Spatie nodig en Spatie heeft een database architectuur nodig met tabellen voor de roles, permissions, etc.
* CLI commandos: Moet gebruik maken van artisan commando's zoals "php artisan shield:setup", "php artisan shield:install", "php artisan shield:generate --all", "php artisan shield:super-admin", etc.
* Databasesegregaties: Shield regelt perfect welke acties een rol mag uitvoeren maar het regelt niet uit de doos welke specifieke rijen een gebruiker mag zien.

---

### Testomgeving & Logins

Hier zijn alle logins en permissions voor de aangemaakte rollen te testen:

Superadmin login:
email: admin@support.com
password: admin
Perms: alles

>Alle wachtwoorden voor alle andere accounts zijn "password".
IT Tech: tech1@test.com
Perms: View en update alle tickets.

Standard Employee: emp@test.com , emp2@test.com
Perms: View en maak eigen tickets.

Department Manager: manager@test.com
Perms: View alle Departementen
view en update alle tickets voor zijn gelinkte departement. 
View en maak eigen tickets.

Facilities team: facilities@test.com
Perms: view en update alle tickets voor zijn gelinkte departement. 
View en maak eigen tickets.