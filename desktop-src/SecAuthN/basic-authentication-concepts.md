---
description: Bei einem Client-/Serveranwendungsmodell handelt es sich bei Clients um Programme, die im Namen von Benutzern agieren, die etwas tun müssen.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Grundlegende Authentifizierungskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d28aa1da3555561740dfd119603a42268ebf86056842788f7dbb1c473fe60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141313"
---
# <a name="basic-authentication-concepts"></a>Grundlegende Authentifizierungskonzepte

Bei einem Client-/Serveranwendungsmodell handelt es sich bei Clients um Programme, die im Namen von Benutzern agieren, die etwas tun müssen. Dies kann das Öffnen und Verwenden einer Datei, der Zugriff auf ein Postfach, das Abfragen einer Datenbank oder das Drucken eines Dokuments sein. Server sind Programme, die Dienste für Clients bereitstellen, z. B. Dateispeicher, E-Mail-Verarbeitung, Abfrageverarbeitung und Druckspooling. Clients initiieren Aktionen, Server reagieren. In der Regel lauscht ein Server an einem Kommunikationsport, der darauf wartet, dass Clients eine Verbindung herstellen und den Dienst anfordern.

Im Kerberos-Protokollmodell beginnt jede Client/Server-Verbindung mit der Authentifizierung. Client und Server wiederum durchlaufen schrittweise eine Reihenfolge von Aktionen, um für die Teilnehmer auf beiden Seiten der Verbindung die Echtheit des anderen Teilnehmers zu überprüfen. Wenn die Authentifizierung erfolgreich war, wird das Setup für die Sitzung abgeschlossen, und es wird eine sichere Client-/Serversitzung erstellt.

Das Kerberos-Protokoll nutzt Folgendes:

-   [Schlüsselauthentifizierung](key-authentication.md)
-   [Authenticator Nachrichten](authenticator-messages.md)
-   [Schlüsselverteilung](key-distribution.md)
-   [Sitzungstickets](session-tickets.md)
-   [Ticketgewährungstickets](ticket-granting-tickets.md)

 

 



