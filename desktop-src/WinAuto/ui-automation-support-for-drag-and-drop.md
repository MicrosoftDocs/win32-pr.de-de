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
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="e831c-112">Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="e831c-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="e831c-113">Die Microsoft-Benutzeroberflächen Automatisierung definiert zwei Steuerelement Muster für die Unterstützung von Drag & Drop-Szenarien, das [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) -Steuerelement Muster und das [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) -Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="e831c-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="e831c-114">Sie implementieren das Drag-Steuerelement Muster für ein Element, das gezogen werden kann, und das DropTarget-Steuerelement Muster für ein Element, das ein gezogenes Element empfangen kann. Das heißt, ein Ablage Ziel.</span><span class="sxs-lookup"><span data-stu-id="e831c-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="e831c-115">Die zwei-Steuerelement Muster machen Informationen verfügbar, die eine Hilfstechnologie verwenden kann, um einem Benutzer mit Eingabe Hilfen einen Drag & Drop-Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e831c-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="e831c-116">Ziehen von Stilen</span><span class="sxs-lookup"><span data-stu-id="e831c-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="e831c-117">Quell-/Zielstil</span><span class="sxs-lookup"><span data-stu-id="e831c-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="e831c-118">Nur-Quelle-Stil</span><span class="sxs-lookup"><span data-stu-id="e831c-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="e831c-119">Ziehen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="e831c-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="e831c-120">Client Schnittstellen für Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="e831c-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="e831c-121">Ziehen von Stilen</span><span class="sxs-lookup"><span data-stu-id="e831c-121">Dragging Styles</span></span>

<span data-ttu-id="e831c-122">Wenn Sie das [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) -Steuerelement Muster für ein Draggable-Element implementieren, müssen Sie entscheiden, ob Sie den Zieh Stil für das Quell-oder *Ziel* Element oder das Zieh Element der reinen *Quelle* implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e831c-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="e831c-123">Quell-/Zielstil</span><span class="sxs-lookup"><span data-stu-id="e831c-123">Source/target Style</span></span>

<span data-ttu-id="e831c-124">Im Quell-/Zielstil von Drag & amp; Drop sind das gezogene Element (die "Quelle") und das Drop-Target-Element (das "Ziel") verschieden, und jede löst einen eindeutigen Satz von Ereignissen aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="e831c-125">Hier ist der Lebenszyklus für einen Zieh Vorgang, der den Quell-/Zielstil verwendet:</span><span class="sxs-lookup"><span data-stu-id="e831c-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="e831c-126">Wenn der Benutzer einen Zieh Vorgang startet:</span><span class="sxs-lookup"><span data-stu-id="e831c-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="e831c-127">Die Quelle löst das Ereignis DragStart ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-128">Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="e831c-129">Ziele aktualisieren Ihre [**droptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e831c-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="e831c-130">Wenn der Zieh Vorgang in eine Zielregion Eintritt:</span><span class="sxs-lookup"><span data-stu-id="e831c-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="e831c-131">Das Ziel löst das DragEnter-Ereignis ([**UIA \_ DropTarget \_ dragentereventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="e831c-132">Wenn der Zieh Vorgang einen Zielbereich verlässt:</span><span class="sxs-lookup"><span data-stu-id="e831c-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="e831c-133">Das Ziel löst das DragLeave-Ereignis ([**UIA \_ DropTarget \_ dragleaveeventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="e831c-134">Wenn der Benutzer das gezogene Element über ein nicht--Ziel freigibt:</span><span class="sxs-lookup"><span data-stu-id="e831c-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="e831c-135">Die Quelle löst das Ereignis dragcancel ([**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-136">Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="e831c-137">Wenn der Benutzer das gezogene Element über einem Ziel freigibt:</span><span class="sxs-lookup"><span data-stu-id="e831c-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="e831c-138">Die Quelle löst das Ereignis dragcomplete ([**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-139">Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="e831c-140">Das Ziel legt die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft fest, um den Effekt anzugeben, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e831c-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="e831c-141">Das Ziel löst das gelöschte Ereignis ([**UIA \_ DropTarget \_ droppedeventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="e831c-142">Die Ereignisse aus den Quell-und Ziel Objekten sind eng verwandt, aber unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="e831c-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="e831c-143">Die Daten über die gezogenen Daten stammen aus der Quelle, während die Daten zu "was passieren können" und "Was ist passiert" aus dem Ziel stammen.</span><span class="sxs-lookup"><span data-stu-id="e831c-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="e831c-144">Wenn ein Zieh Vorgang ausgeführt wird, kann das gezogene Element beliebig oft in die Zielbereiche gezogen und aus diesen verschoben werden, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e831c-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="e831c-145">Alle Ablage Ziele, die die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft im Handumdrehen aktualisieren müssen, sollten ein zusätzliches Eigenschaften Änderungs Ereignis für diese Eigenschaft aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e831c-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="e831c-146">Nur-Quelle-Stil</span><span class="sxs-lookup"><span data-stu-id="e831c-146">Source-only Style</span></span>

<span data-ttu-id="e831c-147">Durch das Ziehen der reinen Quelle kann ein Anbieter das Implementieren von Drop-Zielen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e831c-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="e831c-148">Wenn Sie Drop Targets nicht implementieren, werden die Implementierungskosten gesenkt, aber Barrierefreiheits Client Anwendungen erhalten keine Informationen über das Objekt, das den Löschvorgang erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="e831c-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="e831c-149">Hier ist der Lebenszyklus für einen Zieh Vorgang, der den reinen Quell Stil verwendet:</span><span class="sxs-lookup"><span data-stu-id="e831c-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="e831c-150">Wenn der Benutzer einen Zieh Vorgang startet:</span><span class="sxs-lookup"><span data-stu-id="e831c-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="e831c-151">Die Quelle löst das Ereignis DragStart ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-152">Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="e831c-153">Wenn der Zieh Vorgang in eine Zielregion Eintritt:</span><span class="sxs-lookup"><span data-stu-id="e831c-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="e831c-154">Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft auf den entsprechenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="e831c-155">Wenn der Zieh Vorgang einen Zielbereich verlässt:</span><span class="sxs-lookup"><span data-stu-id="e831c-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="e831c-156">Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft auf den entsprechenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="e831c-157">Wenn der Benutzer das gezogene Element über ein nicht--Ziel freigibt:</span><span class="sxs-lookup"><span data-stu-id="e831c-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="e831c-158">Die Quelle löst das Ereignis dragcancel ([**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-159">Die Quelle legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="e831c-160">Wenn der Benutzer das gezogene Element über einem Ziel freigibt:</span><span class="sxs-lookup"><span data-stu-id="e831c-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="e831c-161">Die Quelle löst das Ereignis dragcomplete ([**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-162">Die Quelle legt die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft fest, um die Auswirkung anzugeben, die beim Löschen des Elements aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e831c-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="e831c-163">Ziehen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="e831c-163">Dragging Multiple Items</span></span>

<span data-ttu-id="e831c-164">Wenn ein Anbieter Drag & amp; Drop-Vorgänge implementiert, bei denen der Benutzer mehrere Objekte gleichzeitig ziehen kann, verwendet der Anbieter den Quell-/Ziel-oder Quellen reinen Stil, wie im vorherigen Abschnitt beschrieben, aber mit einem kleinen Unterschied.</span><span class="sxs-lookup"><span data-stu-id="e831c-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="e831c-165">Wenn der Benutzer den Zieh Vorgang startet, erstellt der Anbieter ein Master Quell Element, das den vollständigen Satz von Elementen darstellt, die gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e831c-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="e831c-166">Das Master Quell Element löst alle Ereignisse für den Satz der gezogenen Elemente aus. die Elemente machen keine eigenen Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="e831c-167">Wenn der Benutzer einen Zieh Vorgang startet:</span><span class="sxs-lookup"><span data-stu-id="e831c-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="e831c-168">Der Anbieter erstellt das Master Quell Element.</span><span class="sxs-lookup"><span data-stu-id="e831c-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="e831c-169">Das Master Source-Element löst das DragStart-Ereignis ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)) aus.</span><span class="sxs-lookup"><span data-stu-id="e831c-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="e831c-170">Das Master Source-Element legt die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="e831c-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="e831c-171">Das Master Quell Element aktualisiert die Liste der gepackten Elemente so, dass alle gezogenen Elemente eingeschlossen werden, sodass die [**getgrabbeditems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) -Methode die Liste abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e831c-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="e831c-172">Zu diesem Zeitpunkt führt das Master Quell Element dieselbe Rolle wie das des Quell Elements aus, wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e831c-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="e831c-173">Client Schnittstellen für Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="e831c-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="e831c-174">Benutzeroberflächenautomatisierungs-Client Anwendungen verwenden die [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) -Schnittstelle und die [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) -Schnittstelle für den Zugriff auf Drag & Drop-Informationen von Benutzeroberflächen Elementen.</span><span class="sxs-lookup"><span data-stu-id="e831c-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 