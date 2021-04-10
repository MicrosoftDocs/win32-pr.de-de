---
title: Active Directory-Domänendienste (AD DS)
description: Microsoft Active Directory Domain Services sind die Grundlage für verteilte Netzwerke, die auf den Betriebssystemen Windows 2000 Server, Windows Server 2003 und Microsoft Windows Server 2008 erstellt werden, die Domänen Controller verwenden.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, Startseite
- Active Directory Domain Services Active Directory, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039810"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>Zweck

Microsoft Active Directory Domain Services sind die Grundlage für verteilte Netzwerke, die auf den Betriebssystemen Windows 2000 Server, Windows Server 2003 und Microsoft Windows Server 2008 erstellt werden, die Domänen Controller verwenden. Active Directory Domain Services einen sicheren, strukturierten, hierarchischen Datenspeicher für Objekte in einem Netzwerk wie z. b. Benutzer, Computer, Drucker und Dienste bereitstellen. Active Directory Domain Services Unterstützung für die Suche nach und die Arbeit mit diesen Objekten bereitstellen.

Dieses Handbuch bietet eine Übersicht über Active Directory Domain Services und Beispielcode für grundlegende Aufgaben, z. b. das Suchen nach Objekten und das Lesen von Eigenschaften, zu erweiterten Aufgaben wie der Dienst Veröffentlichung.

Windows 2000 Server und spätere Betriebssysteme stellen eine Benutzeroberfläche bereit, mit der Benutzer und Administratoren mit den Objekten und Daten in Active Directory Domain Services arbeiten können. In diesem Leitfaden wird beschrieben, wie Sie diese Benutzeroberfläche erweitern und anpassen. Außerdem wird beschrieben, wie Active Directory Domain Services erweitert wird, indem neue Objektklassen und Attribute definiert werden.

> [!Note]  
> Die folgende Dokumentation ist für Computerprogrammierer vorgesehen. Wenn Sie ein Endbenutzer versuchen, ein Druckfehler oder ein Problem mit dem Heimnetzwerk zu debuggen, finden Sie weitere Informationen in den [Microsoft Community-Foren](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Anwendungsbereich

Netzwerkadministratoren schreiben Skripts und Anwendungen, die auf Active Directory Domain Services zugreifen, um allgemeine administrative Aufgaben zu automatisieren, z. b. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerk

Unabhängige Softwarehersteller und Entwickler von Endbenutzern können Active Directory Domain Services programmieren, um Ihre Produkte und Anwendungen zu aktivieren. Dienste können sich selbst in Active Directory Domain Services veröffentlichen. Clients können Active Directory Domain Services verwenden, um Dienste zu suchen, und beide können Active Directory Domain Services verwenden, um andere Objekte in einem Netzwerk zu suchen und mit Ihnen zu arbeiten.

## <a name="developer-audience"></a>Entwicklergruppe

Anwendungen, die auf Daten in Active Directory Domain Services zugreifen, können mit der [Active Directory Dienst Schnittstellen](../adsi/active-directory-service-interfaces-adsi.md) -API, der [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) -API oder dem [System. DirectoryServices](/dotnet/api/system.directoryservices) -Namespace geschrieben werden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Active Directory Domain Services auf Domänen Controllern unter Windows 2000 und höher ausgeführt werden. Client Anwendungen können jedoch für Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 und Windows 95 geschrieben und ausgeführt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Informationen zu Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Allgemeine Informationen zu Active Directory Domain Services.

</dd> <dt>

[Verwenden von Active Directory-Domänendiensten](using-active-directory-domain-services.md)
</dt> <dd>

Active Directory Domain Services-Programmier Handbuch.

</dd> <dt>

[Active Directory Domain Services Referenz](active-directory-domain-services-reference.md)
</dt> <dd>

Active Directory Domain Services-Programmier Verweis.

</dd> </dl>

 

 