---
title: Hinzufügen einer Reservierung
description: Die Routingdatenbank enthält die Reservierungsliste.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac683c48748fa0e644f2f7569590b3783c521f1d10a1a5852a638a29731daf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014948"
---
# <a name="adding-a-reservation"></a>Hinzufügen einer Reservierung

Die Routingdatenbank enthält die Reservierungsliste. Die Reservierungsliste besteht aus den Benutzern, denen Der Zugriff auf den Namespace erlaubt ist, sowie der Zugriffsebene für jeden Benutzer, der unter der Reservierung aufgeführt ist. Wenn Reservierungen hinzugefügt oder gelöscht werden, wird die Routingdatenbank durchsucht, um Zugriffsberechtigungen zu bestimmen.

Zusätzlich zur Überprüfung der Benutzer-ID überprüft die HTTP-Server-API auch vor der Installation einer neuen Reservierung auf Konflikte in vorhandenen Reservierungen.

**So fügen Sie eine neue Reservierung hinzu**

1.  Wenn die Portnummer im UrlPrefix Reservierungen oder Registrierungen für ein anderes Schema als das Schema im UrlPrefix enthält, schlägt die Registrierung fehl. HTTP und HTTPS können nicht auf demselben Port unterstützt werden.
2.  Suchen Sie den entsprechenden Bucket für die Registrierung (siehe Abschnitt [Routing eingehender](routing-incoming-requests.md) Anforderungen) basierend auf dem Hosttyp. Die verbleibenden Schritte sind relativ zu diesem Bucket.
3.  Wählen Sie Reservierungseinträge mit Schema-, Host- und Portkomponenten aus, die mit dem reservierten UrlPrefix übereinstimmen. Suchen Sie hier den Eintrag mit dem längsten übereinstimmenden *relativeUri,* der nicht dem relativeUri in der Reservierung entspricht (d. h. dem *übergeordneten Knoten*). Wenn der Eintrag vorhanden ist, werten Sie die Zugriffsrechte basierend auf der diesem Eintrag zugewiesenen Zugriffssteuerungsliste aus.
4.  Wenn kein übergeordneter Knoten gefunden wurde, ist dies eine Reservierung mit einem leeren relativeUri oder *einer Stammreservierung.* Gewähren Sie Zugriffsrechte nur, wenn der Aufrufer unter den Konten LocalSystem oder Administrator registriert ist.
5.  Wenn Zugriffsrechte gewährt werden, überprüfen Sie, ob doppelte Reservierungen vorhanden sind. Wenn ein Reservierungseintrag mit demselben Schema, Port, Host und relativeUri vorhanden ist, wird ein ERROR \_ ALREADY \_ EXISTS-Code zurückgegeben.
    > [!Note]  
    > Das Aktualisieren eines vorhandenen Eintrags sollte in zwei Schritten erfolgen: Löschen Sie den Eintrag, und fügen Sie einen neuen eintrag hinzu.

     

Wenn die oben genannten Schritte erfolgreich sind, wird ein neuer Reservierungseintrag in die Reservierungsdatenbank eingegeben.

> [!Note]  
> Der neue Eintrag wird mit der angegebenen ACL erstellt und erbt keine ACLs vom *übergeordneten* Eintrag.

 

Die folgenden Beispiele veranschaulichen den Reservierungsprozess.

-   Reservierung 1: Von Administrator für Benutzer A und Benutzer C erfolgreich und wird `https://+:80/vroot/subdir/` in den Bucket "+" eingegeben.
-   Reservierung 2: `https://adatum.com:80/vroot/` Von Administrator für Benutzer B erfolgreich und wird in den Bucket "Expliziter Host" eingegeben.
-   Reservierung 3: `https://adatum.com:80/vroot/subdir/otherdir/` Nach Benutzer B für Benutzer C ist aufgrund von Reservierung 2 erfolgreich.
-   Reservierung 4: `https://+:80/vroot/subdir/otherdir/` Von Benutzer A für Benutzer E ist aufgrund von Reservierung 1 erfolgreich.
-   Reservierung 5: `https://adatum.com:80/vroot/subdir/otherdir/` Nach Benutzer A für Benutzer E schlägt fehl. Der Zugriff wurde aufgrund von Reservierung 2 verweigert.
-   Reservierung 6: `https://+:80/vroot/subdir/` Nach Administrator für Benutzer A schlägt fehl. Die Reservierung steht in Konflikt mit Reservierung 1.
-   Reservierung 7: `https://adatum.com:80/newroot/` Nach Benutzer A für Benutzer A schlägt fehl. Der Zugriff wurde aufgrund einer impliziten Stammreservierung von `https://adatum.com:80/` für LocalSystem oder Administrator verweigert.

Reservierungen können sich auf den Satz von URLs in Anforderungen auswirken, die an einen Prozess übermittelt werden, der zuvor ein UrlPrefix registriert hat. Ein Beispiel:

-   Registrierung: `https://adatum.com:80/vroot/` nach Anwendung 1 für Benutzer A.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 1 übermittelt.
-   Reservierung: `https://+:80/vroot/subdir/` für Benutzer B.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird jetzt abgelehnt.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` nach Anwendung 2 für Benutzer B.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 2 übermittelt.

 

 




