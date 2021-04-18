---
title: Hinzufügen einer Reservierung
description: Die Routing Datenbank enthält die Reservierungsliste.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104517201"
---
# <a name="adding-a-reservation"></a>Hinzufügen einer Reservierung

Die Routing Datenbank enthält die Reservierungsliste. Die Reservierungsliste besteht aus den Benutzern, denen der Zugriff auf den Namespace gestattet ist, sowie der Zugriffsebene für jeden Benutzer, der unter der Reservierung aufgeführt ist. Wenn Reservierungen hinzugefügt oder gelöscht werden, werden die Routing Datenbanken durchsucht, um die Zugriffsberechtigungen zu bestimmen.

Zusätzlich zum Überprüfen der Benutzer-ID prüft die HTTP-Server-API auch, ob in vorhandenen Reservierungen vor der Installation einer neuen Reservierung Konflikte auftreten.

**So fügen Sie eine neue Reservierung hinzu**

1.  Wenn die Portnummer im URLPrefix über Reservierungen oder Registrierungen für ein Schema verfügt, das sich von dem Schema im URLPrefix unterscheidet, schlägt die Registrierung fehl. HTTP und HTTPS können nicht auf demselben Port unterstützt werden.
2.  Suchen Sie den entsprechenden Bucket für die Registrierung (siehe Abschnitt [Routing eingehender Anforderungen](routing-incoming-requests.md) ), basierend auf dem Hosttyp. Die restlichen Schritte sind relativ zu diesem Bucket.
3.  Wählen Sie Reservierungs Einträge mit Schema-, Host-und Port Komponenten aus, die dem zu Reservier enden URLPrefix entsprechen. Suchen Sie den Eintrag mit dem längsten übereinstimmenden *relativeUri* , der nicht gleich dem relativeUri in der Reservierung ist (d. h. dem über *geordneten Knoten*). Wenn der Eintrag vorhanden ist, überprüfen Sie die Zugriffsrechte basierend auf der ACL, die diesem Eintrag zugewiesen ist.
4.  Wenn kein übergeordneter Knoten gefunden wurde, handelt es sich hierbei um eine Reservierung mit einer leeren relativeUri-oder *root-Reservierung*. Erteilen Sie Zugriffsrechte nur, wenn der Aufrufer unter den LocalSystem-oder Administrator Konten registriert ist.
5.  Wenn Zugriffsrechte gewährt werden, überprüfen Sie, ob doppelte Reservierungen vorhanden sind. Wenn ein Reservierungs Eintrag mit demselben Schema, Port, Host und relativeUri vorhanden ist, wird ein \_ Fehler \_ zurückgegeben.
    > [!Note]  
    > Das Aktualisieren eines vorhandenen Eintrags sollte in zwei Schritten ausgeführt werden: Löschen Sie den Eintrag, und fügen Sie einen neuen Eintrag hinzu.

     

Wenn die oben genannten Schritte erfolgreich ausgeführt wurden, wird ein neuer Reservierungs Eintrag in die Reservierungs Datenbank eingegeben.

> [!Note]  
> Der neue Eintrag wird mit der angegebenen ACL erstellt und erbt keine ACLs vom über *geordneten* Eintrag.

 

In den folgenden Beispielen wird der Reservierungsprozess veranschaulicht.

-   Reservierung 1: `https://+:80/vroot/subdir/` vom Administrator für Benutzer A und Benutzer C ist erfolgreich und wird in den Bucket "+" eingegeben.
-   Reservierung 2: `https://adatum.com:80/vroot/` vom Administrator für Benutzer B ist erfolgreich und wird in den Bucket "Expliziter Host" eingetragen.
-   Reservierung 3: `https://adatum.com:80/vroot/subdir/otherdir/` von Benutzer B für Benutzer C ist aufgrund von Reservierung 2 erfolgreich.
-   Reservierung 4: `https://+:80/vroot/subdir/otherdir/` Benutzer A für Benutzer E ist aufgrund von Reservierung 1 erfolgreich.
-   Reservierung 5: `https://adatum.com:80/vroot/subdir/otherdir/` Benutzer A für Benutzer E schlägt fehl. Der Zugriff wurde aufgrund von Reservierung 2 verweigert.
-   Reservierung 6: `https://+:80/vroot/subdir/` der Administrator für Benutzer A schlägt fehl. Die Reservierung steht in Konflikt mit Reservierung 1.
-   Reservierung 7: `https://adatum.com:80/newroot/` von Benutzer a für Benutzer a schlägt fehl. Der Zugriff wurde aufgrund einer impliziten Stamm Reservierung von `https://adatum.com:80/` für "LocalSystem" oder "Administrator" verweigert.

Reservierungen können den Satz von URLs in Anforderungen beeinflussen, die an einen Prozess übermittelt wurden, der zuvor ein URLPrefix registriert hat. Ein Beispiel:

-   Registrierung: `https://adatum.com:80/vroot/` von Anwendung 1 für Benutzer A.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 1 übermittelt.
-   Reservierung: `https://+:80/vroot/subdir/` für Benutzer B.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird jetzt abgelehnt.
-   Registrierung: `https://adatum.com:80/vroot/subdir/` von Anwendung 2 für Benutzer B.
-   Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 2 übermittelt.

 

 




