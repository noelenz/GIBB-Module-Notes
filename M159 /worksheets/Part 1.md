# 2 Grundlagen der Netzwerkauthentisierung mit Kerberos

## 2.0 
Kerberos ist ein Authentisierungsdienst (Authentisierungsprotokoll). Unter Authentisierugn versteht man den Nachweis der eigenen Identität. Wir eine Identität überprüft, spricht man von Authentifizierung.

## 2.1

![grafik](https://github.com/user-attachments/assets/28a1a704-bf14-4185-abcc-1b77288efda5)

Diese Dienste laufen in der Regel auf entfernten Rechnern und der Zugriff erfolgt über spezielle Netzwerkprotokolle. Damit kann man also lokale Authentisierung und Netzwerkauthentisierung unterscheiden.

## 2.2 Authentifizierung mit Kerberos
Beim Prozess der Netzwerkauthentisierung bzw -authentifizierung sind mindestens 2 Teilnehmer beteiligt: Ein Client, der sich authentisieren muss, und ein Dienst, der den Client authentifizieren möchte. Diese beiden Teilnehemr können sein:
  - Anwender - Computerprogramm
  - Anwender - Anwender
  - Computerprogramm - Computerprogramm.

## Kerberos - Begriffe

### 2.3.1
Für die Kerberos-Authentisierung kommt noch ein dritter Teilnehmer hinzu, der Kerberos-Dienst. Der wird als Key Distribution Center (KDC) bezeichnet. Das KDC vermittelt die Authentisierung zwischen Client und Netzwerkdiensten. Dazu müssen alle Clients und alle Dienste ein Vertrauensverhältnis (Trust) zu ihrem KDC haben. Kerberos Dienst = Trusted Third Party.

Kerberos Authentisierung:

![grafik](https://github.com/user-attachments/assets/0589f30a-2962-4039-ac25-06101cacd307)

### 2.3.2 - Realm
Kerberos-Umgebungen teilt man in Reamls ein. Diese entsprechen Organisationen oder Teilen von Organisationen.
Jeder Anwender/Client gehört zu einem Kerberos Realm. Innerhalb dieses Realm gibt es ein KDC, dasfür die Authenitisierungsvorgänge zwischen Clients und Diensten zuständig ist. Die Kerberos-Authentisierung kann auch von Cross-Realm-Authentisierung kann auch Authentisierungsvorgänge zwischen einzelnen Realms umfassen. Hier spricht man von Cross-Realm-Authentisierung.
Jeder Kerberos-Realm besitzt einen Realm-Namen.
Gross- und Kleinschreibung spielt eine Rolle. 
In der Windows Welt entspricht eine Kerberos Realm einem Domainnamen.

### 2.3.3 - Principals
Clients und Dienste innerhalb eines Kerberos Realm werden durch Kerberos Principals

