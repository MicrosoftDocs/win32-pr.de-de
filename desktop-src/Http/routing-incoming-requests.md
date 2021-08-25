---
title: Routing eingehender Anforderungen
description: Die HTTP-Server-API verwaltet eine Routingdatenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40feab96a913da895633bddd8e53697b6aeef959162da054da22aeeedef652a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829960"
---
# <a name="routing-incoming-requests"></a>Routing eingehender Anforderungen

Die HTTP-Server-API verwaltet eine Routingdatenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt. Die Routingtabelle wird aus der Reservierungsdatenbank erstellt und enthält Reservierungseinträge sowie aktuelle Registrierungen. Wenn eine Registrierung oder Reservierung vorgenommen wird, wird sie wie folgt in den Bucket der Routingdatenbank platziert, der dem Hosttyp entspricht:

-   \+ : Portregistrierungen werden im Bucket "Starker Platzhalter" platziert.

-   host: Portregistrierungen werden im Bucket "Explicit" platziert.

-   IP: Portregistrierungen werden im Bucket "IP-gebundener schwacher Platzhalter" platziert.

-   \* : Portregistrierungen werden im Bucket "Schwacher Platzhalter" platziert.

Diese Schritte beziehen sich auch auf die Reihenfolge, in der eingehende HTTP-Anforderungen verarbeitet werden. Zuerst werden die Platzhalterreservierungen mit starkem Platzhalter und dann die explizite Reservierung überprüft, gefolgt vom IP-gebundenen schwachen Platzhalter und dem schwachen Platzhalter. Die Suche wird beendet, wenn eine Übereinstimmung gefunden wird, sodass Registrierungen in einem der verbleibenden Buckets nicht gefunden werden.

Der Routingalgorithmus für die HTTP-Server-API sucht die beste Übereinstimmung für [urlPrefix,](urlprefix-strings.md) indem er sowohl die Registrierungseinträge als auch die Reservierungseinträge der Routingdatenbank durchsuche, beginnend mit dem Bucket mit starkem Platzhalter und dem Bucket mit schwachen Platzhaltern. Die beste Übereinstimmung innerhalb eines Buckets ist die längste Übereinstimmung im relativen URI-Teil des UrlPrefix (vorausgesetzt, es wird eine genaue Übereinstimmung für den Host-, Port- und Schemateil der URL vorausgesetzt). Nachdem eine Übereinstimmung in einem Bucket gefunden wurde, beendet der Routingalgorithmus die Suche und überspringt alle Buckets mit niedrigerer Priorität.

Betrachten Sie beispielsweise die folgenden Registrierungen (basierend auf Buckettypen in absteigender Reihenfolge der Priorität aufgeführt):

-   Registrierung: `https://+:80/vroot/` wird von Anwendung 1 registriert

-   Registrierung: `https://adatum.com:80/` wird von Anwendung 2 registriert.

-   Registrierung: `https://\*:80/` wird von Anwendung 3 registriert.

Eine eingehende Anforderung für `https://adatum.com:80/vroot/subdir/file.htm/` wird an Anwendung 1 übermittelt. Eine eingehende Anforderung für `https://adatum.com:80/default.htm/` wird an Anwendung 2 übermittelt. Eine eingehende Anforderung für `https://otheradatum.com:80/file.htm/` wird an Anwendung 3 übermittelt.

Wenn die beste Übereinstimmung ein Reservierungseintrag ist, bedeutet dies, dass die Anwendung, die die Anforderung empfangen soll, nicht ausgeführt wird. Betrachten Sie beispielsweise die folgende Registrierung und Reservierung:

-   Registrierung: `https://\*:80/vroot/` wird von Anwendung 1 registriert, Benutzer A

-   Reservierung: `https://adatum.com:80/` wurde für Benutzer B reserviert.

Eine eingehende Anforderung für wird nicht an Anwendung 1 übermittelt, da die beste Übereinstimmung zum Reservierungseintrag `https://adatum.com:80/vroot/file.htm/` für Benutzer B führt. Die Rangfolgeregeln werden in diesem Fall auf die Reservierung angewendet, die eine höhere Priorität hat. Wenn kein Prozess aktiv ist, der für Dienstanforderungen für die empfangene URL autorisiert und registriert ist, wird die Anforderung mit dem Statuscode 400 (Bad Request) abgelehnt.

 

 




