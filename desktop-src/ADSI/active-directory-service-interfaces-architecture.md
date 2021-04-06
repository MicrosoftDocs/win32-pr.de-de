---
title: Architektur von Active Directory-Dienst Schnittstellen
description: Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell. In diesem Abschnitt werden COM-Objekt Darstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory Dienst Schnittstellen Architektur ADSI
- ADSI ADSI, Info, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707494"
---
# <a name="active-directory-service-interfaces-architecture"></a>Architektur von Active Directory-Dienst Schnittstellen

Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell. In diesem Abschnitt werden COM-Objekt Darstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.

In der folgenden Objektmodell Abbildung enthält ein Systemobjekt der obersten Ebene ein Namespace Objekt für jeden installierten ADSI-Anbieter.

![Namespaces-Container Objekt](images/ds2top.png)

Jedes der Namespace-Objekte ist selbst ein Container, der die Stamm Knoten der obersten Ebene jedes Servers, der Domäne oder alle anderen Arten von Verzeichnis System Objekten enthält, die in jedem Verzeichnisdienst als Stämme definiert sind.

ADSI stellt einen Satz vordefinierter Objekte und Schnittstellen bereit, damit Client Anwendungen mit Verzeichnisdiensten interagieren können, indem Sie einen einheitlichen Satz von Methoden verwenden. ADSI bietet jedoch möglicherweise keinen Zugriff auf alle Funktionen eines Verzeichnis Dienstanbieter. Um den vollständigen Featuresatz der einzelnen Verzeichnisdienste besser nutzen zu können, stellt ADSI ein Schema Modell bereit, das von Verzeichnis Dienstanbietern und Drittanbieter-Softwareanbietern zum Erweitern von Features über die in ADSI bereitgestellten Schnittstellen hinaus verwendet werden kann

Die Stamm Knoten Container-Objekte, die sich innerhalb des Namespace Objekts eines Anbieters befinden, enthalten ein ADSI-Schema Container Objekt. Dieses Objekt enthält die Definition aller Features für diesen Anbieter. Weitere Informationen finden Sie unter [ADSI-Schema Modell](adsi-schema-model.md).

Dieser Abschnitt schließt folgende Themen ein:

-   [Active Directory von Dienst Schnittstellen Objekten](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md)
-   [Anbieter für Active Directory-Dienst Schnittstellen](active-directory-service-interfaces-provider.md)
-   [ADSI-Schema Modell](adsi-schema-model.md)

 

 




