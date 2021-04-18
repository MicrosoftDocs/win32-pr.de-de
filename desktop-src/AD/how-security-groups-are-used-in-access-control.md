---
title: Verwendung von Sicherheitsgruppen in Access Control
description: Die Sicherheits-ID (SID) ist der Objekt Bezeichner des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Verwendung von Sicherheitsgruppen in Access Control
- Zugriffs Steuerung, Sicherheitsgruppen, die in verwendet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337753"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Verwendung von Sicherheitsgruppen in Access Control

Die Sicherheits-ID (SID) ist der Objekt Bezeichner des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird. Der Name des Benutzers oder der Gruppe wird nicht als eindeutiger Bezeichner innerhalb des Systems verwendet. Die SID wird im **objectSID** -Attribut von Benutzer Objekten und Sicherheitsgruppen Objekten gespeichert. Der Active Directory Server generiert die **objectSID** , wenn der Benutzer oder die Gruppe erstellt wird. Das System stellt sicher, dass die SIDs innerhalb einer Gesamtstruktur eindeutig sind. Beachten Sie, dass es sich bei **objectGUID** um den eindeutigen Bezeichner eines Benutzers, einer Gruppe oder eines beliebigen anderen Verzeichnis Objekts handelt. Die SID ändert sich, wenn ein Benutzer oder eine Gruppe in eine andere Domäne verschoben wird. die **objectGUID** bleibt unverändert.

Wenn einem Benutzer oder einer Gruppe die Berechtigung für den Zugriff auf eine Ressource, z. b. ein Drucker oder eine Dateifreigabe, erteilt wird, wird die SID des Benutzers oder der Gruppe zum Zugriffs Steuerungs Eintrag (Access Control Entry, ACE) hinzugefügt, der die gewährte Berechtigung in der freigegebenen Zugriffs Steuerungs Liste (DACL) der Ressource definiert. In Active Directory Domain Services verfügt jedes Objekt über ein **ntSecurityDescriptor** -Attribut, das eine DACL speichert, die den Zugriff auf das jeweilige Objekt oder die Attribute für dieses Objekt definiert. Weitere Informationen zum Festlegen der Zugriffs Steuerung für Objekte in Active Directory Domain Services finden [Sie Untersteuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Wenn sich ein Benutzer bei einer Windows 2000-Domäne anmeldet, generiert das Betriebssystem ein Zugriffs Token. Dieses Zugriffs Token wird verwendet, um zu bestimmen, auf welche Ressourcen der Benutzer zugreifen darf. Das Benutzer Zugriffs Token enthält die folgenden Daten:

-   Benutzer-SID.
-   SIDs aller globalen und universellen Sicherheitsgruppen, in denen der Benutzer Mitglied ist.
-   SIDs aller nellen globalen und universellen Sicherheitsgruppen.

Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.

Wenn der Benutzer versucht, auf Ressourcen auf einem Computer zuzugreifen, nimmt der Dienst, über den der Benutzer auf die Ressource zugreift, die Identität des Benutzers an, indem ein neues Zugriffs Token basierend auf dem Zugriffs Token erstellt wird, das zum Zeitpunkt der Benutzeranmeldung erstellt wurde. Dieses neue Zugriffs Token enthält auch die folgenden SIDs:

-   SIDs für alle lokalen Domänen Gruppen in der Zieldomäne, in der der Benutzer Mitglied ist.
-   SIDs für alle lokalen Computer Gruppen auf dem Zielcomputer, in denen der Benutzer Mitglied ist.

Der Dienst verwendet dieses neue Zugriffs Token, um den Zugriff auf die Ressource auszuwerten. Wenn eine SID im Zugriffs Token in einem ACEs in der DACL angezeigt wird, erteilt der Dienst dem Benutzer die Berechtigungen, die in diesen ACEs angegeben sind.

 

 




