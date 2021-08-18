---
title: Benutzeroberflächenautomatisierung-Unterstützung für Drag & Drop
description: In diesem Thema werden die Steuerelementmuster beschrieben, die Informationen über die Drag & Drop-Funktionalität eines Elements verfügbar machen.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Benutzeroberflächenautomatisierung,Drag & Drop-Unterstützung
- Benutzeroberflächenautomatisierung,Übersicht über das Drag-Muster
- Benutzeroberflächenautomatisierung,DropTarget-Muster – Übersicht
- Benutzeroberflächenautomatisierung,Drag & Drop–Übersicht
- Drag & Drop-Muster, Informationen
- Ziehen des Steuerelementmusters
- DropTarget-Steuerelementmuster
- Steuerelementmuster,Ziehen
- Steuerelementmuster,DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eab48f4319c51a5ccbbaadae22f1ae337740df5b6d0fdf325a01ba1323f8630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133563"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Benutzeroberflächenautomatisierung-Unterstützung für Drag & Drop

Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern. Sie implementieren das Drag-Steuerelementmuster für ein Element, das gezogen werden kann, und das DropTarget-Steuerelementmuster für ein Element, das ein gezogenes Element empfangen kann. das heißt, ein Abbruchziel. Die beiden Steuerelementmuster machen Informationen verfügbar, die eine Hilfstechnologie verwenden kann, um einem Benutzer für die Barrierefreiheit beim Abschließen eines Drag & Drop-Vorgangs zu helfen.

-   [Ziehen von Stilen](#dragging-styles)
    -   [Quell-/Zielstil](#sourcetarget-style)
    -   [Nur-Quelle-Stil](#source-only-style)
-   [Ziehen mehrerer Elemente](#dragging-multiple-items)
-   [Client Interfaces for Drag-and-Drop](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Ziehen von Stilen

Wenn Sie das *Drag-Steuerelementmuster* für ein ziehbares Element implementieren, müssen Sie entscheiden, ob der Ziehstil für *Quelle/Ziel* oder der Ziehstil nur für die Quelle implementiert werden soll. [](/windows/desktop/WinAuto/uiauto-implementingdrag)

### <a name="sourcetarget-style"></a>Quell-/Zielstil

Im Quell-/Zielstil von Drag & Drop sind das gezogene Element (die "Quelle") und das Drop-Target-Element (das "Ziel") unterschiedlich, und jedes löst einen eigenen Satz von Ereignissen aus. Hier ist der Lebenszyklus für einen Ziehvorgang, der den Quell-/Zielstil verwendet: <dl> Wenn der Benutzer einen Ziehvorgang startet:

-   Die Quelle löst das [**DragStart(UIA \_ \_ DragStartEventId)-Ereignis**](uiauto-event-ids.md)aus.
-   Die Quelle legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **TRUE fest.**
-   Ziele aktualisieren ihre [**DropTargetEffect-Eigenschaften.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)

  
Wenn der Ziehvorgang in einen Zielbereich eintritt:

-   Das Ziel löst das DragEnter-Ereignis ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)) aus.

  
Wenn der Ziehvorgang einen Zielbereich verlässt:

-   Das Ziel löst das DragLeave [**(UIA \_ DropTarget \_ DragLeaveEventId)-Ereignis**](uiauto-event-ids.md)aus.

  
Wenn der Benutzer das gezogene Element über einem Nichtziel freilässt:

-   Die Quelle löst das [**DragCancel(UIA \_ \_ DragCancelEventId)-Ereignis**](uiauto-event-ids.md)aus.
-   Die Quelle legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **FALSE fest.**

  
Wenn der Benutzer das gezogene Element über einem Ziel freilässt:

-   Die Quelle löst das DragComplete-Ereignis ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **FALSE fest.**
-   Das Ziel legt die [**IDropTargetProvider::D ropTargetEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) fest, um den aufgetretenen Effekt anzugeben.
-   Das Ziel löst das Dropped [**(UIA \_ DropTarget \_ DroppedEventId)-Ereignis**](uiauto-event-ids.md)aus.

  
</dl>

Die Ereignisse aus den Quell- und Zielobjekten sind eng miteinander verknüpft, aber eindeutig. Die Daten darüber, was gezogen wird, stammen aus der Quelle, während die Daten zu "Was könnte passieren" und "Was ist passiert" aus dem Ziel stammen.

Wenn ein Ziehvorgang durchgeführt wird, kann das gezogene Element vor Abschluss des Vorgangs so oft wie möglich in die Zielregionen und aus den Zielregionen gezogen werden.

Jedes Abbruchziel, das seine [**IDropTargetProvider::D ropTargetEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) im Fluge aktualisieren muss, sollte ein zusätzliches Eigenschaftsänderungsereignis für diese Eigenschaft erstellen.

### <a name="source-only-style"></a>Nur-Quelle-Stil

Mit dem Ziehstil "Nur Quelle" kann ein Anbieter das Implementieren von Abbruchzielen vermeiden. Das Nichtimplementierung von Abbruchzielen trägt zur Senkung der Implementierungskosten bei, bietet clientanwendungen für die Barrierefreiheit jedoch keine Informationen über das Objekt, das den Absturz empfangen hat. Im Folgenden finden Sie den Lebenszyklus für einen Ziehvorgang, bei dem nur der Quellstil verwendet wird: <dl> Wenn der Benutzer einen Ziehvorgang startet:

-   Die Quelle löst das [**DragStart(UIA \_ \_ DragStartEventId)-Ereignis**](uiauto-event-ids.md)aus.
-   Die Quelle legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **TRUE fest.**

  
Wenn der Ziehvorgang in einen Zielbereich eintritt:

-   Die Quelle legt die [**IDragProvider::D ropEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) auf den entsprechenden Wert fest.

  
Wenn der Ziehvorgang einen Zielbereich verlässt:

-   Die Quelle legt die [**IDragProvider::D ropEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) auf den entsprechenden Wert fest.

  
Wenn der Benutzer das gezogene Element über einem Nichtziel freilässt:

-   Die Quelle löst das [**DragCancel(UIA \_ \_ DragCancelEventId)-Ereignis**](uiauto-event-ids.md)aus.
-   Die Quelle legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **FALSE fest.**

  
Wenn der Benutzer das gezogene Element über einem Ziel freilässt:

-   Die Quelle löst das DragComplete-Ereignis ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**IDragProvider::D ropEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) fest, um den Effekt anzugeben, der beim Löschen des Elements stattgefunden hat.

  
</dl>

## <a name="dragging-multiple-items"></a>Ziehen mehrerer Elemente

Wenn ein Anbieter Drag & Drop-Vorgänge implementiert, bei denen der Benutzer mehrere Objekte gleichzeitig ziehen kann, verwendet der Anbieter die Im vorherigen Abschnitt beschriebenen Quell-/Ziel- oder Quellformatvorlagen, jedoch mit einem kleinen Unterschied. Wenn der Benutzer den Ziehvorgang startet, erstellt der Anbieter ein Masterquellenelement, das den vollständigen Satz von Elementen darstellt, die gezogen werden. Das Masterquellenelement löst alle Ereignisse im Namen der Gruppe gezogener Elemente aus. Die Elemente geben keine eigenen Ereignisse aus.<dl> Wenn der Benutzer einen Ziehvorgang startet:

-   Der Anbieter erstellt das Masterquellenelement.
-   Das Master-Quellelement löst das DragStart [**(UIA \_ \_ DragStartEventId)-Ereignis**](uiauto-event-ids.md)aus.
-   Das Master-Quellelement legt die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) auf **TRUE fest.**
-   Das Master-Quellelement aktualisiert die Liste der abgerufenen Elemente so, dass alle gezogenen Elemente enthalten sind, sodass die [**GetGrabbedItems-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) die Liste abrufen kann.

  
</dl>

Zu diesem Zeitpunkt übernimmt das Masterquellenelement die gleiche Rolle wie das Quellelement, wie im vorherigen Abschnitt beschrieben.

## <a name="client-interfaces-for-drag-and-drop"></a>Clientschnittstellen für Drag & Drop

UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.

 

 