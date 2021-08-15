---
title: Verarbeiten von Registrierungen
description: Die HTTP-Server-APIs verwenden die Routingdatenbank, um Zugriffsüberprüfungen während Registrierungen anzuwenden.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393843"
---
# <a name="processing-registrations"></a>Verarbeiten von Registrierungen

Die HTTP-Server-APIs verwenden die Routingdatenbank, um Zugriffsüberprüfungen während Registrierungen anzuwenden. Eine Registrierung für [ein UrlPrefix](urlprefix-strings.md) muss eine Reihe von Zugriffsüberprüfungen bestehen, um sicherzustellen, dass der Benutzer, der sich für den Namespace registriert, über Zugriffsrechte verfügt. Verwenden Sie die [**HttpAddUrl-Funktion,**](/windows/desktop/api/Http/nf-http-httpaddurl) um eine neue Registrierung hinzuzufügen.

**So fügen Sie eine neue Registrierung mit HttpAddUrl hinzu**

1.  Wenn die Portnummer im UrlPrefix Reservierungen oder Registrierungen für ein anderes Schema als das Schema im UrlPrefix enthält, schlägt die Registrierung fehl. HTTP und HTTPS können nicht auf demselben Port unterstützt werden.
2.  Die Registrierung wird in den entsprechenden Bucket für die Registrierung eingeslotet. Die Buckets basieren auf dem Hosttyp der URL, wie im Abschnitt Routing [eingehender Anforderungen beschrieben.](routing-incoming-requests.md) Die folgenden Schritte sind relativ zu diesem bestimmten Bucket.
3.  Wenn ein doppelter Registrierungseintrag vorhanden ist, geben Sie einen Fehlercode zurück.
4.  Wählen Sie Reservierungseinträge mit Schema-, Host- und Portkomponenten aus, die denen von UrlPrefix entspricht. Suchen Sie aus diesen den Eintrag mit der längsten **relativeUri-Übereinstimmung.** Wenn der Eintrag vorhanden ist, überprüfen Sie die Berechtigungen basierend auf der ACL, die diesem Eintrag zugeordnet ist, und geben Sie erfolg zurück. Wenn der Eintrag nicht vorhanden ist, geben Sie einen ERROR \_ ALREADY \_ EXISTS-Code zurück.

Die folgenden Beispiele veranschaulichen den Prozess zum Installieren einer Registrierung in der Routingdatenbank. Die Reservierungen 1 und 2 sind in der Routingdatenbank vorhanden.

-   Reservierung 1: `https://+:80/vroot/subdir/` für Benutzer A und Benutzer C. Diese Reservierung wird im Bucket "+" platziert.
-   Reservierung 2: `https://adatum.com:80/vroot/` für Benutzer B. Diese Reservierung wird im Bucket "Expliziter Host" platziert.
-   Registrierung: `https://+:80/vroot/subdir/` Nach Benutzer B schlägt aufgrund von Reservierung 1 fehl.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` Nach Benutzer B ist aufgrund von Reservierung 2 erfolgreich.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` Von Benutzer C schlägt aufgrund der expliziteren Reservierung 2 fehl. Die Reservierung mit starkem Platzhalter hat im Kontext der expliziten Reservierung oder Registrierung keine Bedeutung.
-   Registrierung: `https://+:80/vroot/subdir/` Nach Benutzer A ist aufgrund von Reservierung 1 erfolgreich.
-   Registrierung: `https://adatum.com:80/vroot/anotherdir/` Nach Benutzer B ist aufgrund von Reservierung 2 erfolgreich.

Die Zugriffsüberprüfung für die Registrierung umfasst keine Überprüfungen auf Delegierungsberechtigungen. Es gibt keine Zugriffsüberprüfungen basierend auf Reservierungen (siehe [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). Die einzige Anforderung zum Löschen einer Registrierung ist, dass der aufrufende Prozess die Registrierung erstellt haben muss.

 

 




