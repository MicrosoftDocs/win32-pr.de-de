---
title: ADSI-Erweiterungsarchitektur
description: ADSI-Erweiterungen basieren auf dem COM-Aggregationsmodell mit mehreren Erweiterungen. Erweiterungen müssen allen COM-Regeln entsprechen. Weitere Informationen finden Sie in der COM-Spezifikation.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- Extensions ADSI , Erweiterungsarchitektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239a2562054f062464fc924a0f67c31ea3d9fab696fd23e532eab78e1dc66d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023868"
---
# <a name="adsi-extension-architecture"></a>ADSI-Erweiterungsarchitektur

ADSI-Erweiterungen basieren auf dem COM-Aggregationsmodell mit mehreren Erweiterungen. Erweiterungen müssen allen COM-Regeln entsprechen. Weitere Informationen finden Sie in der COM-Spezifikation.

Hier sehen Sie eine Übersicht über das COM-Aggregationsmodell.

![com-Aggregationsmodell](images/comagmod.png)

Ein Aggregat, auch als inneres Objekt bezeichnet, ist ein Objekt, das ein Aggregator erstellt. Ihr Erweiterungsobjekt ist ein Aggregat.

Ein Aggregator, auch als äußeres Objekt bezeichnet, ist ein Objekt, das ein Aggregat erstellt. ADSI ist ein Aggregator.

Das innere -Objekt delegiert [**sein IUnknown-Objekt**](/windows/win32/api/unknwn/nn-unknwn-iunknown) an das **IUnknown-Objekt des Aggregators.**

ADSI-Erweiterungen fügen der COM-Aggregation die folgenden Erweiterungen hinzu, um die Anforderungen zu erfüllen:

-   Ermöglicht es jedem Erweiterungswriter, ADSI-Objekte zu erweitern. Ein Erweiterungswriter kann seine Erweiterung bei ADSI registrieren und ist nicht vom Vorhandensein anderer Erweiterungen betroffen. Im COM-Aggregationsmodell muss der Aggregator über die CLSID des Aggregats verfügen. ADSI lockert diese Anforderung, indem es sich selbst als Aggregator für alle Erweiterungen verwendet. Daher befinden sich Erweiterungen auf derselben Ebene, anstatt eine Ebene geschachtelter Komponenten zu bilden.
-   Ermöglicht ein -Objekt, ein IDispatch. Die Automatisierungsunterstützung ist eines der wichtigsten Features von ADSI. Automatisierungsunterstützung wird erreicht, da ADSI die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) unterstützt. Erweiterungsautoren wird empfohlen, die **IDispatch-Schnittstelle zu** unterstützen. Es sollte jedoch nur eine **IDispatch-Schnittstelle** für ein bestimmtes Objekt geben. ADSI integriert und sammelt die vielen **IDispatch-Schnittstellen** aus verschiedenen Erweiterungen und präsentiert sie als ein konsistentes **IDispatch** für den Automation-Controller. Jede Erweiterung muss, wenn sie aggregiert wird, ihre **IDispatch-Aufrufe** an das von ADSI bereitgestellte **IDispatch** umrouten.

All diese Lösungen sind aufgrund von Diensten möglich, die der ADSI-Objekt-Manager bietet, die sich auf jedem ADSI-Anbieter befinden.

Die folgende Abbildung zeigt die Architektur des ADSI-Erweiterungsmodells.

![Adsi-Erweiterungsmodellarchitektur](images/adsiexmo.png)

ADSI unterstützt zwei Erweiterungsebenen:

-   Unterstützung für frühe Bindungen. Dies ist die erste Erweiterungsebene. Eine Erweiterung muss die Registrierung unterstützen und neue Schnittstellen implementieren. Die Erweiterungsverbraucher müssen Tools oder Skripthosts verwenden, die eine frühe Bindung unterstützen, z. B. Visual C++ , Visual Basic.
-   Unterstützung für spätes Binden. Dies geschieht, wenn eine Erweiterung alle frühen Bindungsanforderungen erfüllt und eine zusätzliche Schnittstelle implementiert, [**IADsExtension.**](/windows/desktop/api/Iads/nn-iads-iadsextension) Erweiterungs implementierer können jedes Tool verwenden, das als Automation-Controller arbeitet, z. B. den Windows-Skripthost, Active Server Pages oder HTML mit VBScript.

 

 