---
title: Verarbeiten von Registrierungen
description: Die HTTP-Server-APIs verwenden die Routing Datenbank, um während der Registrierungen Zugriffs Überprüfungen anzuwenden.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e02d2511d9967454d5cbddd93b2c0380d1172
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474608"
---
# <a name="processing-registrations"></a>Verarbeiten von Registrierungen

Die HTTP-Server-APIs verwenden die Routing Datenbank, um während der Registrierungen Zugriffs Überprüfungen anzuwenden. Eine Registrierung für ein [URLPrefix](urlprefix-strings.md) muss eine Reihe von Zugriffs Überprüfungen bestehen, um sicherzustellen, dass der Benutzer, der sich für den Namespace registriert, über Zugriffsrechte verfügt. Verwenden Sie die [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion, um eine neue Registrierung hinzuzufügen.

**So fügen Sie eine neue Registrierung mit httpaddurl hinzu**

1.  Wenn die Portnummer im URLPrefix über Reservierungen oder Registrierungen für ein Schema verfügt, das sich von dem Schema im URLPrefix unterscheidet, schlägt die Registrierung fehl. HTTP und HTTPS können nicht auf demselben Port unterstützt werden.
2.  Die Registrierung wird in den entsprechenden Bucket für die Registrierung eingecheckt. Die Bucket basieren auf dem Hosttyp der URL, wie im Abschnitt [Routing eingehender Anforderungen](routing-incoming-requests.md) beschrieben. Die folgenden Schritte sind relativ zu diesem speziellen Bucket.
3.  Wenn ein doppelter Registrierungs Eintrag vorhanden ist, wird ein Fehlercode zurückgegeben.
4.  Wählen Sie Reservierungs Einträge mit Schema, Host und Port Komponenten aus, die denen des URLPrefix entsprechen. Suchen Sie in diesem Abschnitt den Eintrag mit der längsten **relativeUri** -Entsprechung. Wenn der Eintrag vorhanden ist, überprüfen Sie die Berechtigungen anhand der ACL, die diesem Eintrag zugeordnet ist, und geben Sie Erfolg zurück. Wenn der Eintrag nicht vorhanden ist, geben Sie einen Fehlercode ein, der \_ bereits \_ vorhanden ist.

In den folgenden Beispielen wird der Prozess zum Installieren einer Registrierung in der Routing Datenbank veranschaulicht. Die Reservierungen 1 und 2 sind in der Routing Datenbank vorhanden.

-   Reservierung 1: `https://+:80/vroot/subdir/` für Benutzer A und Benutzer C. Diese Reservierung wird in den Bucket "+" eingefügt.
-   Reservierung 2: `https://adatum.com:80/vroot/` für Benutzer B. Diese Reservierung wird in den Bucket "Expliziter Host" eingefügt.
-   Registrierung: `https://+:80/vroot/subdir/` nach Benutzer B tritt aufgrund von Reservierung 1 ein Fehler auf.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` nach Benutzer B ist aufgrund von Reservierung 2 erfolgreich.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` Benutzer C schlägt aufgrund der expliziten Reservierung 2 fehl. Die Reservierung für starke Platzhalter hat im Kontext der expliziten Reservierung oder Registrierung keine Bedeutung.
-   Registrierung: `https://+:80/vroot/subdir/` Benutzer A ist aufgrund von Reservierung 1 erfolgreich.
-   Registrierung: `https://adatum.com:80/vroot/anotherdir/` nach Benutzer B ist aufgrund von Reservierung 2 erfolgreich.

Bei der Zugriffs Überprüfung für die Registrierung sind keine Prüfungen auf Delegierungs Berechtigungen enthalten. Es gibt keine Zugriffs Überprüfungen, die auf Reservierungen basieren (siehe [**httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). Die einzige Anforderung zum Löschen einer Registrierung ist, dass der aufrufende Prozess die Registrierung erstellt haben muss.

 

 




