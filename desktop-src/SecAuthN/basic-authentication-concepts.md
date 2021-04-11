---
description: In einem Client-/Serveranwendungsmodell sind Clients Programme, die im Auftrag von Benutzern agieren, die etwas erledigt haben.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Grundlegende Authentifizierungs Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130429"
---
# <a name="basic-authentication-concepts"></a>Grundlegende Authentifizierungs Konzepte

In einem Client-/Serveranwendungsmodell sind Clients Programme, die im Auftrag von Benutzern agieren, die etwas erledigt haben. Dabei kann es sich um das Öffnen und Verwenden einer Datei, das Zugreifen auf ein Postfach, das Abfragen einer Datenbank oder das Drucken eines Dokuments handeln. Server sind Programme, die Dienste für Clients bereitstellen, z. b. Dateispeicher, e-Mail-Verarbeitung, Abfrage Verarbeitung und Druck Spoolvorgang. Von Clients wird eine Aktion initiiert, die Server antwortet. Ein Server lauscht in der Regel an einem Kommunikationsport, der darauf wartet, dass Clients eine Verbindung herstellen und Dienst anfordern.

Im Kerberos-Protokollmodell beginnt jede Client/Server-Verbindung mit der Authentifizierung. Client und Server wiederum durchlaufen schrittweise eine Reihenfolge von Aktionen, um für die Teilnehmer auf beiden Seiten der Verbindung die Echtheit des anderen Teilnehmers zu überprüfen. Wenn die Authentifizierung erfolgreich war, wird das Setup für die Sitzung abgeschlossen, und es wird eine sichere Client-/Serversitzung erstellt.

Das Kerberos-Protokoll verwendet Folgendes:

-   [Schlüssel Authentifizierung](key-authentication.md)
-   [Authenticator-Meldungen](authenticator-messages.md)
-   [Schlüsselverteilung](key-distribution.md)
-   [Sitzungs Tickets](session-tickets.md)
-   [Tickets mit Ticket Gewährung](ticket-granting-tickets.md)

 

 



