---
title: Verwendung von Sicherheitsgruppen in Access Control
description: Die Sicherheits-ID (SID) ist die Objekt-ID des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Verwendung von Sicherheitsgruppen in Access Control
- Zugriffssteuerung, in verwendete Sicherheitsgruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8e14d4d8c371d07619d93f4a6d06318f91e7ec011a4c4fe6d436074ac8ff94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188131"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Verwendung von Sicherheitsgruppen in Access Control

Die Sicherheits-ID (SID) ist die Objekt-ID des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird. Der Name des Benutzers oder der Gruppe wird nicht als eindeutiger Bezeichner im System verwendet. Die SID wird im **objectSid-Attribut** von Benutzerobjekten und Sicherheitsgruppenobjekten gespeichert. Der Active Directory-Server generiert **die objectSid,** wenn der Benutzer oder die Gruppe erstellt wird. Das System stellt sicher, dass die SIDs in einer Gesamtstruktur eindeutig sind. Beachten Sie, dass **objectGuid** der eindeutige Bezeichner eines Benutzers, einer Gruppe oder eines anderen Verzeichnisobjekts ist. Die SID ändert sich, wenn ein Benutzer oder eine Gruppe in eine andere Domäne verschoben wird. **objectGuid bleibt** unverändert.

Wenn einem Benutzer oder einer Gruppe die Berechtigung für den Zugriff auf eine Ressource , z. B. einen Drucker oder eine Dateifreigabe, erteilt wird, wird die SID des Benutzers oder der Gruppe dem Zugriffssteuerungseintrag (ACE) hinzugefügt, der die erteilte Berechtigung in der DACL (Discretionary Access Control List) der Ressource definiert. In Active Directory Domain Services verfügt jedes Objekt über ein **nTSecurityDescriptor-Attribut,** das eine DACL speichert, die den Zugriff auf dieses bestimmte Objekt oder diese Attribute für dieses Objekt definiert. Weitere Informationen zum Festlegen der Zugriffssteuerung für Objekte in Active Directory Domain Services finden Sie unter Steuern des Zugriffs auf Objekte [in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Wenn sich ein Benutzer bei einer Windows 2000-Domäne anmeldet, generiert das Betriebssystem ein Zugriffstoken. Dieses Zugriffstoken wird verwendet, um zu bestimmen, auf welche Ressourcen der Benutzer zugreifen darf. Das Benutzerzugriffstoken enthält die folgenden Daten:

-   Benutzer-SID.
-   SIDs aller globalen und universellen Sicherheitsgruppen, denen der Benutzer mitglied ist.
-   SIDs aller geschachtelten globalen und universellen Sicherheitsgruppen.

Jeder Prozess, der im Auftrag dieses Benutzers ausgeführt wird, verfügt über eine Kopie dieses Zugriffstokens.

Wenn der Benutzer versucht, auf Ressourcen auf einem Computer zu zugreifen, wird vom Dienst, über den der Benutzer auf die Ressource zutritt, die Identität des Benutzers angenommen, indem ein neues Zugriffstoken basierend auf dem Zugriffstoken erstellt wird, das zum Zeitpunkt der Benutzeranmeldung erstellt wurde. Dieses neue Zugriffstoken enthält auch die folgenden SIDs:

-   SIDs für alle lokalen Domänengruppen in der Zieldomäne, der der Benutzer mitglied ist.
-   SIDs für alle lokalen Computergruppen auf dem Zielcomputer, zu denen der Benutzer gehört.

Der Dienst verwendet dieses neue Zugriffstoken, um den Zugriff auf die Ressource zu bewerten. Wenn eine SID im Zugriffstoken in ACEs in der DACL angezeigt wird, erteilt der Dienst dem Benutzer die in diesen ACEs angegebenen Berechtigungen.

 

 




