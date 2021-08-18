---
title: Architektur von Active Directory-Dienstschnittstellen
description: Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell. In diesem Abschnitt werden COM-Objektdarstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory-Dienstschnittstellenarchitektur ADSI
- ADSI ADSI , Informationen, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afbc212edbea6491de4cae89f2c8b7c873019b6d5678c5bf1d5b531f519260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024083"
---
# <a name="active-directory-service-interfaces-architecture"></a>Architektur von Active Directory-Dienstschnittstellen

Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell. In diesem Abschnitt werden COM-Objektdarstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.

In der folgenden Abbildung des Objektmodells enthält ein Systemobjekt der obersten Ebene ein Namespace-Objekt für jeden installierten ADSI-Anbieter.

![Namespaces-Containerobjekt](images/ds2top.png)

Jedes der Namespace-Objekte ist selbst ein Container, der die Stammknoten der obersten Ebene jedes Servers, jeder Domäne oder jeder anderen Art von Verzeichnissystemobjekten enthält, die in jedem Verzeichnisdienst als Stamm definiert sind.

ADSI stellt eine Reihe vordefinierter Objekte und Schnittstellen bereit, sodass Clientanwendungen mithilfe eines einheitlichen Methodensatzes mit Verzeichnisdiensten interagieren können. ADSI bietet jedoch möglicherweise nicht zugriff auf alle Funktionen eines Verzeichnisdiensts. Um den vollständigen Featuresatz jedes Verzeichnisdiensts besser nutzen zu können, stellt ADSI ein Schemamodell bereit, mit dem Verzeichnisdienstanbieter und Softwarehersteller von Drittanbietern Features über die in ADSI bereitgestellten Schnittstellen hinaus erweitern können.

Die Stammknotencontainerobjekte, die sich in jedem Namespace-Objekt des Anbieters befinden, enthalten ein ADSI-Schemacontainerobjekt. Dieses Objekt enthält die Definition aller Features für diesen Anbieter. Weitere Informationen finden Sie unter [ADSI-Schemamodell.](adsi-schema-model.md)

Dieser Abschnitt schließt folgende Themen ein:

-   [Active Directory-Dienstschnittstellenobjekte](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md)
-   [Anbieter von Active Directory-Dienstschnittstellen](active-directory-service-interfaces-provider.md)
-   [ADSI-Schemamodell](adsi-schema-model.md)

 

 




