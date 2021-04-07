---
title: Verwenden von Active Directory Dienst Schnittstellen
description: Mit Active Directory Service Interfaces (ADSI) können Client Anwendungen von Verzeichnisdiensten einen Satz von Schnittstellen für die Kommunikation mit einem beliebigen Namespace verwenden, der eine ADSI-Implementierung bereitstellt.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Verwenden von Active Directory Dienst Schnittstellen ADSI
- ADSI ADSI, using
- Active Directory Dienst Schnittstellen ADSI, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855235"
---
# <a name="using-active-directory-service-interfaces"></a>Verwenden von Active Directory Dienst Schnittstellen

Mit Active Directory Service Interfaces (ADSI) können Client Anwendungen von Verzeichnisdiensten einen Satz von Schnittstellen für die Kommunikation mit einem beliebigen Namespace verwenden, der eine ADSI-Implementierung bereitstellt. ADSI-Clients verwenden die klar definierten Active Directory Dienst Schnittstellen anstelle der Netzwerk spezifischen API-Aufrufe, um einen einfacheren Zugriff auf die Dienste für einen Namespace zu erhalten.

Active Directory Dienst Schnittstellen entsprechen den Component Object Model (com) und unterstützen com-Standard Features.

ADSI bietet Schnittstellen, die mit der Automatisierung für namens gebundene Controller wie Java, Microsoft Visual Basic Development System und Visual Basic Scripting Edition (VBScript) kompatibel sind. ADSI kann auch eine Schnittstelle bereitstellen, mit der die Leistung für Schnittstellen optimiert werden kann, die nicht mit der Automatisierung kompatibel sind und in sprach Umgebungen wie C und C++ verwendet werden können.

ADSI bietet auch die nicht Automatisierungs Schnittstellen [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), um die Verwaltung von Verzeichnis Objekten und Abfragen zu unterstützen.

Außerdem stellt ADSI einen eigenen OLE DB Anbieter bereit, sodass alle Clients, die bereits OLE DB verwenden, einschließlich derjenigen, die ActiveX Data Objects verwenden, Verzeichnisdienste direkt abfragen können.

Webanwendungen, die Active Server Seiten verwenden, können auch den Zugriff auf Verzeichnisdienste über ADSI programmieren.

ADSI-Clients können alle ADSI-Anbieter an einem Standort Programm gesteuert ermitteln und die gleichen Schnittstellen für die Kommunikation mit den einzelnen Namespaces verwenden. Wenn zusätzliche Anbieter installiert sind, können die ADSI-Clients auch ohne Neukompilieren mit den neuen Namespaces kommunizieren.

In diesem Programmier Handbuch wird beschrieben, wie ADSI funktioniert, und es werden Informationen zum Ausführen bestimmter Aufgaben in ADSI bereitstellt. Die folgenden Themen werden erörtert:

-   [Binden an ein ADSI-Objekt](binding-to-an-adsi-object.md)
-   [Erstellen und Löschen von Objekten](creating-and-deleting-objects.md)
-   [Zugreifen auf und Bearbeiten von Daten mit ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Verwenden des ADSI-Schemas](using-the-adsi-schema.md)
-   [Sammlungen und Gruppen](collections-and-groups.md)
-   [Auflisten von ADSI-Objekten](enumerating-adsi-objects.md)
-   [Such Active Directory](searching-active-directory.md)
-   [ADSI-Sicherheitsmodell](adsi-security-model.md)
-   [ADSI-Erweiterungen](adsi-extensions.md)
-   [Verwenden von ADSI mit Exchange](using-adsi-with-exchange.md)
-   [ADSI Utility-Schnittstellen](adsi-utility-interfaces.md)
-   [Programmieren von ADSI mit Java/com](programming-adsi-with-javacom.md)

 

 




