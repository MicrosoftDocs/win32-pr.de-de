---
title: Was ist ein Benutzer?
description: Benutzerkonten werden als Objekte in Active Directory Domain Services erstellt und gespeichert.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- Was ist ein Benutzer Active Directory
- Benutzer Active Directory, was ist ein Benutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c59b2ea46474860268f327bcd03d2ba67ecea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707505"
---
# <a name="what-is-a-user"></a>Was ist ein Benutzer?

Benutzerkonten werden als Objekte in Active Directory Domain Services erstellt und gespeichert. Benutzerkonten können von Menschen oder Programmen wie z. b. System Diensten verwendet werden, um sich an einem Computer anzumelden. Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es mit den im Benutzerobjekt des Benutzers auf dem Active Directory Server gespeicherten Daten verglichen wird. Wenn das Kennwort authentifiziert ist, d. h., das Kennwort entspricht dem im Benutzerobjekt gespeicherten Kennwort, erstellt das System ein Zugriffs Token. Ein Zugriffstoken ist ein Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt. Die Daten in einem Token enthalten die Sicherheitsidentität und die Gruppenmitgliedschaften des Benutzerkontos, das dem Prozess oder Thread zugeordnet ist. Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.

Jeder Benutzer oder jede Anwendung, die auf Ressourcen in einer Windows-Domäne zugreift, muss über ein Konto auf dem Active Directory Server verfügen. Windows verwendet dieses Benutzerkonto, um zu überprüfen, ob der Benutzer oder die Anwendung über die Berechtigung zum Verwenden einer Ressource verfügt.

Ein Benutzerkonto kann für Folgendes verwendet werden:

-   Ermöglichen Sie es Benutzern, sich bei einem Computer anzumelden und auf Ressourcen basierend auf der Identität des Benutzerkontos zuzugreifen.
-   Aktivieren Sie Programme und Dienste, die in einem bestimmten Sicherheitskontext ausgeführt werden.
-   Verwalten des Benutzer Zugriffs auf freigegebene Ressourcen, z. b. Objekte und deren Eigenschaften, Netzwerkfreigaben, Dateien, Verzeichnisse, Drucker Warteschlangen usw.

Gruppen können Mitglieder enthalten, bei denen es sich um Verweise auf Benutzer und andere Gruppen handelt. Gruppen können auch verwendet werden, um den Zugriff auf freigegebene Ressourcen zu steuern. Beim Zuweisen von Berechtigungen für Ressourcen, z. b. Dateifreigaben, Drucker usw., sollten Administratoren diese Berechtigungen einer Gruppe anstelle der einzelnen Benutzer zuweisen. Die Berechtigungen werden der Gruppe einmal und nicht mehrmals für jeden einzelnen Benutzer zugewiesen. Dies vereinfacht die Wartung und Verwaltung eines Netzwerks.

## <a name="users-compared-to-contacts"></a>Benutzer im Vergleich zu Kontakten

Sowohl Benutzer als auch Kontakte können zur Darstellung von Menschen verwendet werden. Ein Benutzer ist jedoch ein Sicherheits Prinzipal. ein Kontakt ist nicht.

Ein Benutzer kann verwendet werden, um einem menschlichen Benutzer die Anmeldung und den Zugriff auf freigegebene Ressourcen zu ermöglichen.

Ein Kontakt wird nur für Verteilerliste und e-Mail-Zwecke verwendet. Ein Kontakt kann jedoch die meisten Daten enthalten, die in einem Benutzerobjekt gespeichert sind, wie z. b. Adresse, Telefonnummern usw., da sowohl der Benutzer als auch der Kontakt vom **classSchema** -Objekt der Person abgeleitet werden. Ein Kontakt hat keinen Sicherheitskontext. Daher kann ein Kontakt nicht verwendet werden, um den Zugriff auf freigegebene Ressourcen zu steuern, und kann nicht zum Anmelden an einem Computer verwendet werden.

## <a name="users-compared-to-computers"></a>Benutzer im Vergleich zu Computern

Die Computer Objektklasse erbt von der Benutzerobjekt Klasse. Ein Computer Objekt stellt einen Computer dar. der Computer und die lokalen Dienste des Computers benötigen jedoch häufig Zugriff auf das Netzwerk und freigegebene Ressourcen. Wenn der Computer auf freigegebene Ressourcen zugreift, nicht der Benutzer, der am Computer angemeldet ist, benötigt er ein Zugriffs Token, genauso wie ein Benutzer, der als Benutzer angemeldet ist. Wenn ein Computer auf das Netzwerk zugreift, wird ein Zugriffs Token verwendet, das die Sicherheits-ID für das Computer Konto des Computers und die Gruppen enthält, denen das Konto angehört.

Ein Dienst kann im Kontext von "LocalSystem" oder einem bestimmten Dienst Konto ausgeführt werden. Auf Computern mit Windows 2000 verwendet ein Dienst, der im Kontext des Kontos "LocalSystem" ausgeführt wird, die Anmelde Informationen des Computers.

 

 




