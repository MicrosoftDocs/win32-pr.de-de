---
title: Routing eingehender Anforderungen
description: Die HTTP-Server-API verwaltet eine Routing Datenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391189"
---
# <a name="routing-incoming-requests"></a>Routing eingehender Anforderungen

Die HTTP-Server-API verwaltet eine Routing Datenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt. Die Routing Tabelle wird aus der Reservierungs Datenbank erstellt und enthält Reservierungs Einträge sowie aktuelle Registrierungen. Wenn eine Registrierung oder Reservierung durchgeführt wird, wird Sie in den Bucket der Routing Datenbank eingefügt, der dem Hosttyp entspricht:

-   \+ : Port Registrierungen werden in den Bucket "starke Platzhalter" eingefügt.

-   Host: Port Registrierungen werden in den "expliziten" Bucket eingefügt.

-   IP: Port Registrierungen werden in den Bucket "IP-gebundene schwache Platzhalter" eingefügt.

-   \* : Port Registrierungen werden in den Bucket "schwache Platzhalter" eingefügt.

Diese Schritte beziehen sich auch auf den Auftrag, bei dem eingehende HTTP-Anforderungen verarbeitet werden. Die starken Platzhalter Reservierungen werden zuerst geprüft, dann wird die explizite Reservierung geprüft, gefolgt vom IP-gebundenen schwachen Platzhalter und dem schwachen Platzhalter. Die Suche wird beendet, wenn eine Entsprechung gefunden wird, damit Registrierungen in einem der verbleibenden Bucket nicht gefunden werden.

Der HTTP-Server-API-Routing Algorithmus sucht die beste Entsprechung für das [URLPrefix](urlprefix-strings.md) durch das Durchsuchen der Registrierungseinträge und der Reservierungs Einträge der Routing Datenbank, beginnend mit dem großen Platzhalter Bucket und endende mit dem schwachen Platzhalter Bucket. Die beste Entsprechung innerhalb eines Bucket ist die längste Entsprechung im relativen URI-Teil des URLPrefix-Werts (vorausgesetzt eine genaue Entsprechung für den Host, den Port und die Schema Teile der URL). Wenn eine Entsprechung in einem Bucket gefunden wird, beendet der Routing Algorithmus die Suche und überspringt alle Bucket mit niedrigerer Priorität.

Betrachten Sie z. b. die folgenden Registrierungen (in absteigender Reihenfolge der Priorität basierend auf Bucket-Typen aufgeführt):

-   Registrierung: `https://+:80/vroot/` wird von Anwendung 1 registriert

-   Registrierung: `https://adatum.com:80/` wird von Anwendung 2 registriert

-   Registrierung: `https://\*:80/` wird von Anwendung 3 registriert.

Eine eingehende Anforderung für `https://adatum.com:80/vroot/subdir/file.htm/` wird an Anwendung 1 übermittelt. Eine eingehende Anforderung für `https://adatum.com:80/default.htm/` wird an Anwendung 2 übermittelt. Eine eingehende Anforderung für `https://otheradatum.com:80/file.htm/` wird an Anwendung 3 übermittelt.

Wenn die beste Entsprechung ein Reservierungs Eintrag ist, bedeutet dies, dass die Anwendung, die die Anforderung empfangen sollte, nicht ausgeführt wird. Sehen Sie sich beispielsweise die folgende Registrierung und Reservierung an:

-   Registrierung: `https://\*:80/vroot/` wird von Anwendung 1 registriert, Benutzer A

-   Reservierung: wurde `https://adatum.com:80/` für Benutzer B reserviert.

Eine eingehende Anforderung für `https://adatum.com:80/vroot/file.htm/` wird nicht an Anwendung 1 übermittelt, da die beste Entsprechung zum Reservierungs Eintrag für Benutzer B führt. Die Rang Folge Regeln werden in diesem Fall auf die Reservierung angewendet, die eine höhere Priorität hat. Wenn kein Prozess aktiv ist, der autorisiert und bei Dienst Anforderungen für die empfangene URL registriert ist, wird die Anforderung mit dem Statuscode 400 (ungültige Anforderung) zurückgewiesen.

 

 




