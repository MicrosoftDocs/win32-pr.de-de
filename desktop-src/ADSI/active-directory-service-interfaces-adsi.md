---
title: Active Directory Service Interfaces
description: Einführung in Active Directory Services-Schnittstellen mit Links zu verschiedenen Handbüchern.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Active Directory Dienst Schnittstellen (siehe ADSI)
- ADSI ADSI, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039605"
---
# <a name="active-directory-service-interfaces"></a>Active Directory Service Interfaces

## <a name="purpose"></a>Zweck

Active Directory Service Interfaces (ADSI) ist ein Satz von COM-Schnittstellen, die für den Zugriff auf die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern verwendet werden. ADSI wird in einer verteilten Computerumgebung verwendet, um einen einzelnen Satz von Verzeichnisdienst Schnittstellen für die Verwaltung von Netzwerkressourcen zu präsentieren. Administratoren und Entwickler können ADSI-Dienste verwenden, um die Ressourcen in einem Verzeichnisdienst aufzulisten und zu verwalten, unabhängig davon, welche Netzwerkumgebung die Ressource enthält.

ADSI ermöglicht allgemeine Verwaltungsaufgaben, z. b. das Hinzufügen neuer Benutzer, das Verwalten von Druckern und das Auffinden von Ressourcen in einer verteilten Computerumgebung.

> [!Note]  
> Die folgende Dokumentation ist für Computerprogrammierer vorgesehen. Wenn Sie ein Endbenutzer versuchen, ein Druckfehler oder ein Problem mit dem Heimnetzwerk zu debuggen, finden Sie weitere Informationen in den [Microsoft Community-Foren](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Anwendungsbereich

Netzwerkadministratoren können mit ADSI häufige Aufgaben automatisieren, z. b. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerkressourcen.

Unabhängige Software Hersteller und Entwickler von Endbenutzern können ADSI als "Verzeichnis Aktivierung" für Ihre Produkte und Anwendungen verwenden. Dienste können sich selbst in einem Verzeichnis veröffentlichen, Clients können das Verzeichnis zum Suchen der Dienste verwenden, und beide können das Verzeichnis verwenden, um andere Objekte zu suchen und zu bearbeiten, die von Interesse sind. Da Active Directory Dienst Schnittstellen unabhängig von den zugrunde liegenden Verzeichnisdiensten sind, können Verzeichnis aktivierte Produkte und Anwendungen in mehreren Netzwerk-und Verzeichnis Umgebungen erfolgreich ausgeführt werden.

## <a name="developer-audience"></a>Entwicklergruppe

Sie können in vielen Sprachen ADSI-Client Anwendungen schreiben. Für die meisten administrativen Aufgaben definiert ADSI Schnittstellen und Objekte, auf die von Automatisierungs kompatiblen Sprachen wie Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) und Java aus zugegriffen werden kann, um die leistungsstärker und effizientere Sprache wie C und C++ zu erhalten. Eine gute Grundlage bei der com-Programmierung ist für den ADSI-Programmierer von nutzen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Active Directory wird auf Windows Server-Domänen Controllern ausgeführt. Allerdings können Client Anwendungen mit ADSI in Windows geschrieben und ausgeführt werden. Außerdem benötigen Entwickler das Platform Software Development Kit (SDK), das auch auf der MSDN-Website verfügbar ist. Verwenden Sie das MMC-Snap-in "Active Directory-Benutzer und-Computer", um den Inhalt Active Directory zu untersuchen. Dieses Snap-in ersetzt das adsvw-Tool, das für vorherige Versionen von Windows verfügbar war.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Informationen zu ADSI](about-adsi.md)
</dt> <dd>

Allgemeine Informationen zu ADSI.

</dd> <dt>

[Verwenden von ADSI](using-adsi.md)
</dt> <dd>

Programmier Handbuch für die Verwendung von ADSI.

</dd> <dt>

[ADSI-Schnellstart-Tutorials](adsi-quick-start-tutorials.md)
</dt> <dd>

Verwenden von ADSI mit Automation zum Verwalten von Verzeichnissen.

</dd> <dt>

[ADSI-Referenz](adsi-reference.md)
</dt> <dd>

Dokumentation zu ADSI-Schnittstellen und-Methoden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Component Object Model](../com/the-component-object-model.md)
</dt> <dt>

[COM-Clients und-Server](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 