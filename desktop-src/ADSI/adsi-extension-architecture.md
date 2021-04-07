---
title: ADSI-Erweiterungs Architektur
description: ADSI-Erweiterungen basieren auf dem com-Aggregations Modell mit mehreren Erweiterungen. Erweiterungen müssen allen com-Regeln entsprechen. Weitere Informationen finden Sie in der com-Spezifikation.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, Erweiterungs Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730288"
---
# <a name="adsi-extension-architecture"></a>ADSI-Erweiterungs Architektur

ADSI-Erweiterungen basieren auf dem com-Aggregations Modell mit mehreren Erweiterungen. Erweiterungen müssen allen com-Regeln entsprechen. Weitere Informationen finden Sie in der com-Spezifikation.

Im folgenden finden Sie eine Überprüfung des com-Aggregations Modells.

![com-Aggregations Modell](images/comagmod.png)

Ein Aggregat, das auch als Inneres Objekt bezeichnet wird, ist ein Objekt, das von einem Aggregator erstellt wird. Das Erweiterungs Objekt ist ein Aggregat.

Ein Aggregator, auch als Äußeres Objekt bezeichnet, ist ein Objekt, das ein Aggregat erstellt. ADSI ist ein Aggregator.

Das innere Objekt delegiert seine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) an die **IUnknown** des Aggregators.

ADSI-Erweiterungen fügen die folgenden Erweiterungen zu com-Aggregationen hinzu, um die Anforderungen zu erfüllen:

-   Ermöglicht jedem erweiterungswriter das Erweitern von ADSI-Objekten. Ein erweiterungswriter kann seine Erweiterung bei ADSI registrieren und nicht durch das vorhanden sein anderer Erweiterungen beeinträchtigt werden. Im com-Aggregations Modell muss der Aggregator über die CLSID des Aggregats verfügen. ADSI lockert diese Anforderung, indem er als Aggregator für alle Erweiterungen fungiert. Daher befinden sich die Erweiterungen nicht auf derselben Ebene, anstatt eine Schicht von untergeordneten Komponenten zu bilden.
-   Ermöglicht ein Objekt, ein IDispatch. Automation-Unterstützung ist eines der wichtigsten Features von ADSI. Automation-Unterstützung wird erzielt, da ADSI die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle unterstützt. Erweiterungs Schreiber wird empfohlen, die **IDispatch** -Schnittstelle zu unterstützen. Es darf jedoch nur eine **IDispatch** -Schnittstelle für ein bestimmtes Objekt vorhanden sein. ADSI integriert und sammelt die vielen **IDispatch** -Schnittstellen aus unterschiedlichen Erweiterungen und stellt Sie als eine konsistente **IDispatch** -Schnittstelle für den Automatisierungs Controller dar. Jede Erweiterung muss, wenn Sie aggregiert wird, Ihre **IDispatch** -Aufrufe an das von ADSI bereitgestellte **IDispatch** umleiten.

Diese Lösungen sind aufgrund der Dienste möglich, die der ADSI-Objekt-Manager bereitstellt, die sich auf jedem ADSI-Anbieter befinden.

Die folgende Abbildung zeigt die Architektur des ADSI-Erweiterungs Modells.

![Architektur des ADSI-Erweiterungs Modells](images/adsiexmo.png)

ADSI unterstützt zwei Ebenen der Erweiterung:

-   Unterstützung für frühe Bindung. Dies ist die erste Erweiterungs Ebene. Eine Erweiterung muss die Registrierung unterstützen und neue Schnittstellen implementieren. Die Erweiterungs Consumer müssen Tools oder Skript Hosts verwenden, die eine frühe Bindung unterstützen, z. b. Visual C++ Visual Basic.
-   Späterer Bindungs Support. Dies geschieht, wenn eine Erweiterung alle frühen Bindungs Anforderungen erfüllt und eine zusätzliche Schnittstelle ( [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)) implementiert. Erweiterungs Implementierer können jedes Tool verwenden, das als Automatisierungs Controller fungiert, wie z. b. den Windows Script Host, Active Server Seiten oder HTML mit VBScript.

 

 