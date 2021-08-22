---
title: Verwenden von Active Directory-Domänendiensten
description: Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory-Verzeichnisdienst verwenden oder veröffentlichen.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory mit
- Active Directory Domain Services Active Directory mit
- 'Active Directory-Beispiele: Active Directory'
- Active Directory Domain Services Active Directory-Beispiele
- Active Directory-Beispiele
- Active Directory Active Directory , Beispiele finden Sie Active Directory Domain Services Beispiele.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e1ef5428242e6d83fcb0c517c91abaee24de8181689a3aa1922eafea4d76703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024538"
---
# <a name="using-active-directory-domain-services"></a>Verwenden von Active Directory-Domänendiensten

Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory-Verzeichnisdienst verwenden oder veröffentlichen.

> [!Note]  
> Die folgende Dokumentation ist für Computerprogrammierer. Wenn Sie versuchen, einen Active Directory-Startdruckfehler zu beheben, sehen Sie sich den folgenden Vorschlag [auf](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) den Microsoft-Communityseiten an: Wenn dies nicht hilft, probieren Sie diese Empfehlungen von [TechNet aus.](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint)

 

Active Directory Domain Services sind mit Lightweight Directory Access Protocol 3.0 kompatibel, das durch RFC 2251 und andere RFCs definiert ist. Jeder der folgenden API-Sätze kann für den Zugriff auf Active Directory Domain Services. Jeder API-Satz hat Vor- und Nachteile, die von der Programmiersprache, der Programmierumgebung und der beabsichtigten Ausführungsmethode abhängen. Die meisten Beispiele in diesem Leitfaden verwenden ADSI, das von Sprachen wie C und C++ unterstützt wird, sowie automatisierungskonforme Sprachen wie Microsoft Visual Basic und Visual Basic Scripting Edition.

Weitere Informationen zu bestimmten Active Directory Domain Services finden Sie unter:

-   [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

In diesem Abschnitt werden die folgenden Themen erläutert:

-   [Binden an Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Suchen in Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Erstellen und Löschen von Objekten in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Verschieben von Objekten](moving-objects.md)
-   [Lesen und Schreiben von Attributen von Objekten in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Steuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Erweitern des Schemas](extending-the-schema.md)
-   [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md)
-   [Verwalten von Benutzern](managing-users.md)
-   [Verwalten von Gruppen](managing-groups.md)
-   [Nachverfolgen von Änderungen](tracking-changes.md)
-   [Dienstveröffentlichung](service-publication.md)
-   [Dienstanmeldungskonten](service-logon-accounts.md)
-   [Gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md)
-   [Sichern und Wiederherstellen von Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Speichern dynamische Daten](storing-dynamic-data.md)
-   [Anwendungsverzeichnispartitionen](application-directory-partitions.md)
-   [Erkennen des Betriebsmodus einer Domäne](detecting-the-operation-mode-of-a-domain.md)

 

 