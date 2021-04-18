---
title: Verwenden von ADSI mit Exchange
description: Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten. Weitere Informationen finden Sie unter Verwaltungsaufgaben für ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI für Exchange ADSI
- ADSI für Exchange ADSI, Postfächer
- ADSI für Exchange ADSI, Postfächer, erstellen
- ADSI für Exchange ADSI, Postfächer, löschen
- ADSI für Exchange ADSI, Postfächer, Festlegen der Sicherheits Beschreibung für
- ADSI für Exchange ADSI, Postfächer, Suche nach Home Server für
- ADSI für Exchange ADSI, das erhalten und Ändern von Nachrichten
- ADSI für Exchange ADSI, Sicherheits Deskriptoren
- ADSI für Exchange ADSI, Sicherheits Deskriptoren, Bearbeitung
- ADSI für Exchange ADSI, Sicherheits Deskriptoren, festlegen
- ADSI für Exchange ADSI, Empfänger Container
- ADSI für Exchange ADSI, Anzeigen von Exchange-Objekteigenschaften
- ADSI für Exchange ADSI, Empfängers Container, Custom
- ADSI für Exchange ADSI, Exchange Server
- ADSI für Exchange ADSI, Exchange Server, anzeigen und Ändern des Schemas
- ADSI für Exchange ADSI, Exchange Server, Auflisten der Server Version
- ADSI für Exchange ADSI, Exchange Server, Organisation und Website Name
- ADSI für Exchange ADSI, Exchange Server, Suche nach Mailbox Home Server
- ADSI für Exchange ADSI, e-Mail-Adressen, Abrufen
- ADSI für Exchange ADSI, Verteilerlisten, erstellen
- ADSI für Exchange ADSI, verborgene oder gelöschte Einträge
- ADSI für Exchange ADSI, Abrufen von Verzeichnisdienst Änderungen
- ADSI für Exchange ADSI, Nachrichtengröße
- ADSI für Exchange ADSI, Problembehandlung
- Postfächer ADSI
- Postfächer ADSI, erstellen
- Postfächer ADSI, löschen
- Postfächer ADSI, Festlegen der Sicherheits Beschreibung für
- Postfächer ADSI, Suche nach Home Server für
- Nachrichten ADSI, Getting und Modifizierung
- Exchange ADSI
- Exchange ADSI, Postfächer
- Exchange ADSI, Postfächer, erstellen
- Exchange ADSI, Postfächer, löschen
- Exchange ADSI, Postfächer, Festlegen der Sicherheits Beschreibung für
- Exchange ADSI, Postfächer, Suche nach Home Server für
- Exchange ADSI, das erhalten und Ändern von Nachrichten
- Exchange ADSI, Sicherheits Deskriptoren
- Exchange ADSI, Sicherheits Deskriptoren, bearbeiten
- Exchange ADSI, Sicherheits Deskriptoren, festlegen
- Exchange ADSI, Empfänger Container
- Exchange ADSI, Anzeigen von Exchange-Objekteigenschaften
- Exchange ADSI, Empfänger Container, Benutzer definiert
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, anzeigen und Ändern des Schemas
- Exchange ADSI, Exchange Server, Auflisten der Server Version
- Exchange ADSI, Exchange Server, Organisation und Website Name
- Exchange ADSI, Exchange Server, Suchen des Postfachs Home Server
- Exchange ADSI, e-Mail-Adressen, Abrufen
- Exchange ADSI, Verteilerlisten, erstellen
- Exchange ADSI, verborgene oder gelöschte Einträge
- Exchange ADSI, Abrufen von Verzeichnisdienst Änderungen
- Exchange ADSI, Nachrichtengröße
- Exchange ADSI, Problembehandlung
- Sicherheits Deskriptoren ADSI für Exchange-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337255"
---
# <a name="using-adsi-with-exchange"></a>Verwenden von ADSI mit Exchange

Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten. Weitere Informationen finden Sie unter [Verwaltungsaufgaben für ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).

Die folgenden Aufgaben finden Sie in diesem Abschnitt:

-   Erstellen einer Benutzer-URL
-   Active Directory Pfade werden aufgebaut.
-   Auflisten von Exchange 2000-Servern mit ADSI
-   Bearbeiten von Erweiterungs Attributen mit ADSI
-   Hinzufügen/Entfernen eines Manager-Objekts mit ADSI
-   Auflisten von Exchange-Objekteigenschaften mit ADSI/ADO
-   Abrufen eines definierten Legacy namens von Exchange mit ADSI
-   Suchen des Namens der Exchange-Organisation mit ADSI
-   Suchen von Exchange-Adresslisten mit ADSI
-   Erstellen einer Verteilerliste mit CDOEXM und ADSI
-   Festlegen der Nachrichten Einschränkung auf einem virtuellen SMTP-Server mithilfe von ADSI

Die ADSI-Referenz und die Verwendung von Informationen für Exchange 5,5 finden Sie im [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) Guide.

Die folgenden Aufgaben finden Sie in diesem Abschnitt:

-   Anzeigen und Ändern des Exchange Server-Schemas
-   Anzeigen der roheigenschaften eines Exchange-Objekts
-   Erstellen eines Exchange-Postfachs
-   Festlegen der Sicherheits Beschreibung für ein Exchange-Postfach
-   Manipulieren von Sicherheits Deskriptoren und SIDs
-   Löschen eines Post Fach Objekts
-   Erstellen eines benutzerdefinierten Empfängers
-   Erstellen eines Empfänger Containers
-   Die Organisation und der Standort Name werden von einem Server erhalten.
-   Auflisten der Exchange Server-Version aller Server in der Organisation
-   Suchen des Basis Servers eines Postfachs
-   Abrufen von e-Mail-Adressen
-   Zugreifen auf verborgene oder gelöschte Einträge
-   Abrufen von Änderungen, die an den Verzeichnisdienst vorgenommen wurden
-   Erstellen einer Verteilerliste aus den Ergebnissen einer Abfrage
-   Erhalten oder Ändern der Nachrichtengröße
-   Verwenden von LDAP-Fehlercodes zum Beheben von Problemen

 

 