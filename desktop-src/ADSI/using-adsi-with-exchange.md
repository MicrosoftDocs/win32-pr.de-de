---
title: Verwenden von ADSI mit Exchange
description: Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten. Weitere Informationen finden Sie unter Verwaltungsaufgaben für ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI für Exchange ADSI
- ADSI für Exchange ADSI, Postfächer
- ADSI für Exchange ADSI, Postfächer, erstellen
- ADSI for Exchange ADSI ,mailboxes,deleting
- ADSI für Exchange ADSI, Postfächer, Festlegen des Sicherheitsdeskriptors auf
- ADSI für Exchange ADSI, Postfächer,Suchen des Heimservers für
- ADSI für Exchange ADSI, Abrufen und Ändern von Nachrichten
- ADSI für Exchange ADSI, Sicherheitsbeschreibungen
- ADSI für Exchange ADSI, Sicherheitsdeskriptoren, Bearbeiten
- ADSI für Exchange ADSI, Sicherheitsbeschreibungen,Einstellung
- ADSI für Exchange ADSI, Empfängercontainer
- ADSI für Exchange ADSI, Anzeigen Exchange Objekteigenschaften
- ADSI für Exchange ADSI, Empfängercontainer,benutzerdefiniert
- ADSI for Exchange ADSI ,Exchange Server
- ADSI for Exchange ADSI ,Exchange Server,viewing and modifying schema
- ADSI for Exchange ADSI ,Exchange Server,listing server version
- ADSI für Exchange ADSI, Exchange Server,Organisation und Websitename
- ADSI for Exchange ADSI ,Exchange Server,finding mailbox home server
- ADSI für Exchange ADSI, E-Mail-Adressen, Abrufen
- ADSI für Exchange ADSI, Verteilerlisten, Erstellung
- ADSI für Exchange ADSI, ausgeblendete oder gelöschte Einträge
- ADSI für Exchange ADSI, Abrufen von Verzeichnisdienständerungen
- ADSI für Exchange ADSI, Nachrichtengröße
- ADSI for Exchange ADSI , Problembehandlung
- Postfächer ADSI
- Postfächer ADSI , erstellen
- Postfächer ADSI , löschen
- Postfächer ADSI , Festlegen des Sicherheitsdeskriptors auf
- Postfächer ADSI , Suchen des Homeservers für
- messages ADSI ,getting and modifying
- Exchange Adsi
- Exchange ADSI, Postfächer
- Exchange ADSI, Postfächer, erstellen
- Exchange ADSI , Postfächer, löschen
- Exchange ADSI , Postfächer, Festlegen des Sicherheitsdeskriptors auf
- Exchange ADSI, Postfächer, Suchen des Heimservers für
- Exchange ADSI , Abrufen und Ändern von Nachrichten
- Exchange ADSI , Sicherheitsdeskriptoren
- Exchange ADSI, Sicherheitsdeskriptoren, Bearbeiten
- Exchange ADSI, Sicherheitsdeskriptoren, Einstellung
- Exchange ADSI , Empfängercontainer
- Exchange ADSI , Anzeigen Exchange Objekteigenschaften
- Exchange ADSI , Empfängercontainer, benutzerdefiniert
- Exchange ADSI , Exchange Server
- Exchange ADSI , Exchange Server, Anzeigen und Ändern des Schemas
- Exchange ADSI , Exchange Server, Serverversion auflisten
- Exchange ADSI, Exchange Server,Organisation und Websitename
- Exchange ADSI,Exchange Server,Suchen des Postfach-Homeservers
- Exchange ADSI, E-Mail-Adressen, Abrufen
- Exchange ADSI , Verteilerlisten, Erstellen
- Exchange ADSI, ausgeblendete oder gelöschte Einträge
- Exchange ADSI , Abrufen von Verzeichnisdienständerungen
- Exchange ADSI , Nachrichtengröße
- Exchange ADSI , Problembehandlung
- Sicherheitsdeskriptoren ADSI für Exchange Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f48a1015674ea8bf413cb9edbf55f0f64f6211b85bb876baeb6ab47868482ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690129"
---
# <a name="using-adsi-with-exchange"></a>Verwenden von ADSI mit Exchange

Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten. Weitere Informationen finden Sie unter [Verwaltungsaufgaben für ADSI.](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65))

Die folgenden Aufgaben finden Sie in diesem Abschnitt:

-   Erstellen einer Benutzer-URL
-   Erstellen von Active Directory-Pfaden
-   Aufzählen von Exchange 2000 Servern mit ADSI
-   Bearbeiten von Erweiterungsattributen mit ADSI
-   Hinzufügen/Entfernen eines Managerobjekts mit ADSI
-   Aufzählen Exchange Objekteigenschaften mit ADSI/ADO
-   Abrufen eines Legacynamens Exchange mit ADSI
-   Suchen des Exchange Organisationsnamens mit ADSI
-   Suchen Exchange Adresslisten mit ADSI
-   Erstellen einer Verteilerliste mit CDOEXM und ADSI
-   Festlegen der Nachrichteneinschränkung auf einem virtuellen SMTP-Server mit ADSI

Für Exchange 5.5 finden Sie die ADSI-Referenz und die Verwendungsinformationen im [ADSI-Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) Leitfaden.

Die folgenden Aufgaben finden Sie in diesem Abschnitt:

-   Anzeigen und Ändern des Exchange Server Schemas
-   Anzeigen der rohen Eigenschaften eines Exchange Objekts
-   Erstellen eines Exchange Postfachs
-   Festlegen der Sicherheitsbeschreibung für ein Exchange Postfach
-   Bearbeiten von Sicherheitsbeschreibungen und SIDs
-   Löschen eines Postfachobjekts
-   Erstellen eines benutzerdefinierten Empfängers
-   Erstellen eines Empfängercontainers
-   Abrufen des Organisations- und Standortnamens von einem Server
-   Auflisten Exchange Serverversion aller Server in der Organisation
-   Suchen des Homeservers eines Postfachs
-   Abrufen von E-Mail-Adressen
-   Zugreifen auf ausgeblendete oder gelöschte Einträge
-   Abrufen von Änderungen, die am Verzeichnisdienst vorgenommen wurden
-   Erstellen einer Verteilerliste aus den Ergebnissen einer Abfrage
-   Abrufen oder Ändern der Nachrichtengröße
-   Verwenden von LDAP-Fehlercodes zur Problembehandlung

 

 