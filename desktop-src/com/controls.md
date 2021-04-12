---
title: Steuerelemente (com)
description: Steuerelemente
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339997"
---
# <a name="controls-com"></a>Steuerelemente (com)

Bei einem ActiveX-Steuerelement handelt es sich in Wirklichkeit nur um einen anderen Begriff für das OLE-Objekt. Anders ausgedrückt: ein Steuerelement ist zumindest ein COM-Objekt, das die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützt und auch selbst registriert wird. Über [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) kann ein Container die Gültigkeitsdauer des Steuer Elements verwalten und den vollständigen Umfang der Funktionalität eines Steuer Elements auf der Grundlage der verfügbaren Schnittstellen dynamisch ermitteln. Dadurch kann ein Steuerelement so wenig Funktionalität implementieren, wie es benötigt, anstatt eine große Anzahl von Schnittstellen zu unterstützen, die tatsächlich nichts Unternehmen. Kurz gesagt, diese minimale Anforderung für nichts mehr als **IUnknown** ermöglicht es, dass alle Steuerelemente so einfach wie möglich sind.

Kurz gesagt, außer [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und Selbstregistrierung gibt es keine anderen Anforderungen an ein Steuerelement. Es gibt jedoch Konventionen, die berücksichtigen sollten, was die Unterstützung einer Schnittstelle in Bezug auf Funktionen bedeutet, die für den Container durch das Steuerelement bereitgestellt werden. In diesem Abschnitt wird dann beschrieben, was es bedeutet, dass ein Steuerelement eine Schnittstelle unterstützt, sowie Methoden, Eigenschaften und Ereignisse, die ein Steuerelement als Baseline bereitstellen sollte, wenn es eine Gelegenheit zum unterstützen von Methoden, Eigenschaften und Ereignissen hat.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Selbstregistrierung für Steuerelemente](self-registration-for-controls.md)
-   [Was bedeutet Unterstützung für eine Schnittstelle](what-support-for-an-interface-means.md)
-   [Persistenzschnittstellen](persistence-interfaces.md)
-   [Optionale Methoden in Steuerungs Schnittstellen](optional-methods-in-control-interfaces.md)
-   [Class Factory-Optionen](class-factory-options.md)
-   [Verfügbar machen von Eigenschaften über IDispatch](properties.md)
-   [Verfügbar machen von Methoden über IDispatch](exposing-methods-through-idispatch.md)
-   [Ereignisse in Steuerelementen](events-in-controls.md)
-   [Eigenschaftenseiten](property-pages.md)
-   [Ambient-Eigenschaften für Steuerelemente](ambient-properties-for-controls.md)
-   [Verwenden der Container-Funktionalität](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelement-und Steuerelement Container](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




