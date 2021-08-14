---
title: Steuerelemente (COM)
description: Steuerelemente
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fb125988ad73c997772f1a07a170833b6cb36837437632aed46ba3ac0298fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919640"
---
# <a name="controls-com"></a>Steuerelemente (COM)

Ein ActiveX Steuerelement ist eigentlich nur ein weiterer Begriff für OLE-Objekt oder genauer gesagt COM-Objekt. Anders ausgedrückt: Ein Steuerelement ist zumindest ein COM-Objekt, das die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) unterstützt und sich selbst registriert. Mit [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) kann ein Container die Lebensdauer des Steuerelements verwalten und dynamisch den vollständigen Umfang der Funktionalität eines Steuerelements basierend auf den verfügbaren Schnittstellen ermitteln. Dadurch kann ein Steuerelement so wenig Funktionalität implementieren, wie es benötigt, anstatt eine große Anzahl von Schnittstellen zu unterstützen, die eigentlich nichts tun. Kurz gesagt ermöglicht diese minimale Anforderung für nichts anderes als **IUnknown,** dass jedes Steuerelement so einfach wie möglich ist.

Kurz gesagt, außer [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und selbstregistrierung gibt es keine anderen Anforderungen für ein Steuerelement. Es gibt jedoch Konventionen, die befolgt werden sollten, was die Unterstützung einer Schnittstelle in Bezug auf die Funktionalität bedeutet, die dem Container vom -Steuerelement bereitgestellt wird. In diesem Abschnitt wird dann beschrieben, was es bedeutet, dass ein Steuerelement eine Schnittstelle tatsächlich unterstützt, sowie Methoden, Eigenschaften und Ereignisse, die ein Steuerelement als Baseline bereitstellen sollte, wenn es Gelegenheit hat, Methoden, Eigenschaften und Ereignisse zu unterstützen.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Selbstregistrierung für Steuerelemente](self-registration-for-controls.md)
-   [Was bedeutet Die Unterstützung für eine Schnittstelle?](what-support-for-an-interface-means.md)
-   [Persistenzschnittstellen](persistence-interfaces.md)
-   [Optionale Methoden in Steuerelementschnittstellen](optional-methods-in-control-interfaces.md)
-   [Klassenfactoryoptionen](class-factory-options.md)
-   [Verfügbarmachen von Eigenschaften über IDispatch](properties.md)
-   [Verfügbarmachen von Methoden über IDispatch](exposing-methods-through-idispatch.md)
-   [Ereignisse in Steuerelementen](events-in-controls.md)
-   [Eigenschaftenseiten](property-pages.md)
-   [Umgebungseigenschaften für Steuerelemente](ambient-properties-for-controls.md)
-   [Verwenden der Funktionalität des Containers](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX Steuerungs- und Steuerungscontainerrichtlinien](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




