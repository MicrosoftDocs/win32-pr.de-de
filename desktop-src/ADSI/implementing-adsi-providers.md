---
title: Implementieren von Active Directory Dienst Schnittstellen Anbietern
description: Bei Active Directory Service Interfaces (ADSI) handelt es sich um COM-Schnittstellen, mit denen Verzeichnisdienst Objekte in Verzeichnisdienst Clients verfügbar gemacht werden. Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Client Basis auf den Satz von ADSI-Client Anwendungen.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementieren von Active Directory Dienst Schnittstellen Anbieter ADSI
- Implementieren von ADSI-Anbietern ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707415"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementieren von Active Directory Dienst Schnittstellen Anbietern

Bei Active Directory Service Interfaces (ADSI) handelt es sich um COM-Schnittstellen, mit denen Verzeichnisdienst Objekte in Verzeichnisdienst Clients verfügbar gemacht werden. Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Client Basis auf den Satz von ADSI-Client Anwendungen.

Wie bei jeder com-Implementierung können Sie in vielen Sprachen einen ADSI-Anbieter schreiben. Die ADSI-COM-Schnittstellen werden als duale Schnittstellen definiert, die sowohl Lauf Zeit-als auch Kompilierzeit-Namensauflösung ermöglichen. Sie können von Automatisierungs kompatiblen Sprachen wie z. b. Visual Basic, Visual Basic Scripting Edition sowie den mehr Leistungs-und Effizienz bewussten Sprachen wie C und C++ aufgerufen werden. ADSI-Clients enthalten auch Webanwendungen, die Active Server Seiten und Verwaltungs-Snap-Ins über die Microsoft Management Console verwenden.

Da ADSI einen eigenen OLE DB Anbieter bereitstellt, ermöglicht die Implementierung der durch [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) definierten Suchfunktionen auch, dass ADSI-Clients ihren Verzeichnisdienst nach Daten Abfragen können.

Alle Verzeichnisdienst Objekte können über ein generisches ADSI-Objekt dargestellt werden, das [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)unterstützt. ADSI stellt die Bausteine bereit, die für die Darstellung der Features und Dienste eines beliebigen Verzeichnis Diensts erforderlich sind.

Außerdem stellen die ADSI-metaschnittstellen gängige Objekte dar, die von Verzeichnis Administratoren verwendet werden. Sie ordnen die Eigenschaften der metaschnittstellen den Eigenschaften zu, die vom Verzeichnisdienst unterstützt werden. Die Programmierung von ADSI-Clients mit den Active Directory-Dienst Schnittstellen erhält Zugriff auf Ihren Verzeichnisdienst, sobald der Anbieter installiert und das System neu gestartet wird.

Wenn Ihr Verzeichnisdienst eine Schema Darstellung unterstützt, wird der Namespace durch Unterstützung der Schema Verwaltungs Schnittstellen direkt für Verzeichnisdienst Browser zugänglich gemacht. Wenn Sie Ihre Features über das Schema veröffentlichen, können Clients ihren Verzeichnisdienst Online Abfragen und die von Ihnen angebotenen Dienste nutzen. Aufgrund der Online Schema Verfügbarkeit und des Vorteile der COM-Schnittstelle können Sie weiterhin neue Features für Ihre Client Software zur Verfügung stellen und gleichzeitig Versionen unterstützen.

 

 




