---
title: Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop
description: In diesem Thema werden die Steuerelement Muster beschrieben, die Informationen über die Drag & Drop-Funktionalität eines Elements verfügbar machen.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Benutzeroberflächenautomatisierungs-, Drag & Drop-Unterstützung
- UI-Automatisierung, Übersicht über Drag Pattern
- UI-Automatisierung, DropTarget-Muster (Übersicht)
- UI-Automatisierung, Drag & amp; Drop (Übersicht)
- Drag & Drop-Muster, Informationen zu
- Steuerelement Muster ziehen
- DropTarget-Steuerelement Muster
- Steuerelement Muster, ziehen
- Steuerelement Muster, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339894"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop

Die Microsoft-Benutzeroberflächen Automatisierung definiert zwei Steuerelement Muster für die Unterstützung von Drag & Drop-Szenarien, das [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) -Steuerelement Muster und das [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) -Steuerelement Muster. Sie implementieren das Drag-Steuerelement Muster für ein Element, das gezogen werden kann, und das DropTarget-Steuerelement Muster für ein Element, das ein gezogenes Element empfangen kann. Das heißt, ein Ablage Ziel. Die zwei-Steuerelement Muster machen Informationen verfügbar, die eine Hilfstechnologie verwenden kann, um einem Benutzer mit Eingabe Hilfen einen Drag & Drop-Vorgang abzuschließen.

-   [Ziehen von Stilen](#dragging-styles)
    -   [Quell-/Zielstil](#sourcetarget-style)
    -   [Nur-Quelle-Stil](#source-only-style)
-   [Ziehen mehrerer Elemente](#dragging-multiple-items)
-   [Client Schnittstellen für Drag & Drop](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Ziehen von Stilen

Wenn Sie das [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) -Steuerelement Muster für ein Draggable-Element implementieren, müssen Sie entscheiden, ob Sie den Zieh Stil für das Quell-oder *Ziel* Element oder das Zieh Element der reinen *Quelle* implementieren möchten.

### <a name="sourcetarget-style"></a>Quell-/Zielstil

Im Quell-/Zielstil von Drag & amp; Drop sind das gezogene Element (die "Quelle") und das Drop-Target-Element (das "Ziel") verschieden, und jede löst einen eindeutigen Satz von Ereignissen aus. Hier ist der Lebenszyklus für einen Zieh Vorgang, der den Quell-/Zielstil verwendet: <dl> Wenn der Benutzer einen Zieh Vorgang startet:

-   Die Quelle löst das Ereignis DragStart ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.
-   Ziele aktualisieren Ihre [**droptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaften.

  
Wenn der Zieh Vorgang in eine Zielregion Eintritt:

-   Das Ziel löst das DragEnter-Ereignis ([**UIA \_ DropTarget \_ dragentereventid**](uiauto-event-ids.md)) aus.

  
Wenn der Zieh Vorgang einen Zielbereich verlässt:

-   Das Ziel löst das DragLeave-Ereignis ([**UIA \_ DropTarget \_ dragleaveeventid**](uiauto-event-ids.md)) aus.

  
Wenn der Benutzer das gezogene Element über ein nicht--Ziel freigibt:

-   Die Quelle löst das Ereignis dragcancel ([**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.

  
Wenn der Benutzer das gezogene Element über einem Ziel freigibt:

-   Die Quelle löst das Ereignis dragcomplete ([**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.
-   Das Ziel legt die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft fest, um den Effekt anzugeben, der aufgetreten ist.
-   Das Ziel löst das gelöschte Ereignis ([**UIA \_ DropTarget \_ droppedeventid**](uiauto-event-ids.md)) aus.

  
</dl>

Die Ereignisse aus den Quell-und Ziel Objekten sind eng verwandt, aber unterschiedlich. Die Daten über die gezogenen Daten stammen aus der Quelle, während die Daten zu "was passieren können" und "Was ist passiert" aus dem Ziel stammen.

Wenn ein Zieh Vorgang ausgeführt wird, kann das gezogene Element beliebig oft in die Zielbereiche gezogen und aus diesen verschoben werden, bevor der Vorgang abgeschlossen ist.

Alle Ablage Ziele, die die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft im Handumdrehen aktualisieren müssen, sollten ein zusätzliches Eigenschaften Änderungs Ereignis für diese Eigenschaft aufrufen.

### <a name="source-only-style"></a>Nur-Quelle-Stil

Durch das Ziehen der reinen Quelle kann ein Anbieter das Implementieren von Drop-Zielen vermeiden. Wenn Sie Drop Targets nicht implementieren, werden die Implementierungskosten gesenkt, aber Barrierefreiheits Client Anwendungen erhalten keine Informationen über das Objekt, das den Löschvorgang erhalten hat. Hier ist der Lebenszyklus für einen Zieh Vorgang, der den reinen Quell Stil verwendet: <dl> Wenn der Benutzer einen Zieh Vorgang startet:

-   Die Quelle löst das Ereignis DragStart ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.

  
Wenn der Zieh Vorgang in eine Zielregion Eintritt:

-   Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft auf den entsprechenden Wert fest.

  
Wenn der Zieh Vorgang einen Zielbereich verlässt:

-   Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft auf den entsprechenden Wert fest.

  
Wenn der Benutzer das gezogene Element über ein nicht--Ziel freigibt:

-   Die Quelle löst das Ereignis dragcancel ([**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.

  
Wenn der Benutzer das gezogene Element über einem Ziel freigibt:

-   Die Quelle löst das Ereignis dragcomplete ([**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md)) aus.
-   Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft fest, um die Auswirkung anzugeben, die beim Löschen des Elements aufgetreten ist.

  
</dl>

## <a name="dragging-multiple-items"></a>Ziehen mehrerer Elemente

Wenn ein Anbieter Drag & amp; Drop-Vorgänge implementiert, bei denen der Benutzer mehrere Objekte gleichzeitig ziehen kann, verwendet der Anbieter den Quell-/Ziel-oder Quellen reinen Stil, wie im vorherigen Abschnitt beschrieben, aber mit einem kleinen Unterschied. Wenn der Benutzer den Zieh Vorgang startet, erstellt der Anbieter ein Master Quell Element, das den vollständigen Satz von Elementen darstellt, die gezogen werden. Das Master Quell Element löst alle Ereignisse für den Satz der gezogenen Elemente aus. die Elemente machen keine eigenen Ereignisse aus.<dl> Wenn der Benutzer einen Zieh Vorgang startet:

-   Der Anbieter erstellt das Master Quell Element.
-   Das Master Source-Element löst das DragStart-Ereignis ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.
-   Das Master Source-Element legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.
-   Das Master Quell Element aktualisiert die Liste der gepackten Elemente so, dass alle gezogenen Elemente eingeschlossen werden, sodass die [**getgrabbeditems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) -Methode die Liste abrufen kann.

  
</dl>

Zu diesem Zeitpunkt führt das Master Quell Element dieselbe Rolle wie das des Quell Elements aus, wie im vorherigen Abschnitt beschrieben.

## <a name="client-interfaces-for-drag-and-drop"></a>Client Schnittstellen für Drag & Drop

Benutzeroberflächenautomatisierungs-Client Anwendungen verwenden die [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) -Schnittstelle und die [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) -Schnittstelle für den Zugriff auf Drag & Drop-Informationen von Benutzeroberflächen Elementen.

 

 