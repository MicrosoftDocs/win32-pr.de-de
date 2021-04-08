---
title: Verwenden von Active Directory-Domänendiensten
description: Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory Verzeichnisdienst verwenden oder veröffentlichen.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory mit
- Active Directory Domain Services Active Directory mit
- Active Directory Beispiele Active Directory
- Active Directory Domain Services Beispiele Active Directory
- Beispiele Active Directory
- Active Directory Active Directory finden Sie in den Beispielen Active Directory Domain Services Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734545"
---
# <a name="using-active-directory-domain-services"></a>Verwenden von Active Directory-Domänendiensten

Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory Verzeichnisdienst verwenden oder veröffentlichen.

> [!Note]  
> Die folgende Dokumentation ist für Computerprogrammierer vorgesehen. Wenn Sie versuchen, einen Active Directory Druckfehler zu beheben, lesen Sie den [folgenden Vorschlag](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) auf den Microsoft Community-Seiten. Wenn dies nicht hilfreich ist, testen Sie diese Empfehlungen von [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Active Directory Domain Services sind mit dem Lightweight Directory Access Protocol 3,0 kompatibel, das von RFC 2251 und anderen RFCs definiert wird. Alle folgenden API-Sätze können für den Zugriff auf Active Directory Domain Services verwendet werden. Jeder API-Satz hat vor-und Nachteile, die von der Programmiersprache, der Programmierumgebung und der vorgesehenen Ausführungs Methode abhängen. Die Mehrzahl der Beispiele in dieser Anleitung verwenden ADSI, das von Sprachen wie C und C++ unterstützt wird, sowie von Automatisierungs kompatiblen Sprachen wie Microsoft Visual Basic und Visual Basic Scripting Edition.

Weitere Informationen zu bestimmten Active Directory Domain Services Technologien finden Sie unter:

-   [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

In diesem Abschnitt werden die folgenden Themen behandelt:

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
-   [Dienst Anmeldekonten](service-logon-accounts.md)
-   [Gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md)
-   [Sichern und Wiederherstellen von Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Speichern von dynamische Daten](storing-dynamic-data.md)
-   [Anwendungsverzeichnis Partitionen](application-directory-partitions.md)
-   [Erkennen des Betriebsmodus einer Domäne](detecting-the-operation-mode-of-a-domain.md)

 

 