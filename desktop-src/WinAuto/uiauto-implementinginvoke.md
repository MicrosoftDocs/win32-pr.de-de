---
title: Steuerelement Muster aufrufen
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IInvokeProvider, einschließlich Informationen zu-Methoden.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Aufruf Steuerungs Musters
- UI-Automatisierung, Steuerelement Muster aufrufen
- UI-Automatisierung, IInvokeProvider
- IInvokeProvider
- Implementieren von Steuerelement Mustern für die Benutzeroberflächen Automatisierung
- Aufrufen von Steuerelement Mustern
- Steuerelement Muster, IInvokeProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächenautomatisierungs-aufrufen
- Steuerelement Muster, aufrufen
- Schnittstellen, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855923"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="9d23a-113">Steuerelement Muster aufrufen</span><span class="sxs-lookup"><span data-stu-id="9d23a-113">Invoke Control Pattern</span></span>

<span data-ttu-id="9d23a-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), einschließlich Informationen zu-Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d23a-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="9d23a-115">Das **Aufruf** Steuerelement-Muster wird zur Unterstützung von Steuerelementen verwendet, die den Zustand nicht beibehalten, wenn Sie aktiviert werden, sondern eine einzelne, eindeutige Aktion initiieren oder ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d23a-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="9d23a-116">Steuerelemente, die den Zustand beibehalten (z. b. Kontrollkästchen und Options Felder), müssen stattdessen [**itggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) bzw. [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren.</span><span class="sxs-lookup"><span data-stu-id="9d23a-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="9d23a-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9d23a-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9d23a-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9d23a-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9d23a-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="9d23a-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9d23a-120">Erforderliche Member für **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="9d23a-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="9d23a-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d23a-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9d23a-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="9d23a-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9d23a-123">Beachten Sie beim Implementieren des **Aufruf** Steuerungs Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="9d23a-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9d23a-124">Steuerelemente implementieren [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) , wenn das gleiche Verhalten nicht durch einen anderen Steuerelement Muster-Anbieter verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="9d23a-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="9d23a-125">Wenn z. b. die [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) -Methode in einem-Steuerelement dieselbe Aktion wie die [**iuiautomationexpandredusepattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) -oder [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) -Methode ausführt, sollte das Steuerelement **IInvokeProvider** nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="9d23a-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="9d23a-126">Ein Steuerelement wird normalerweise durch Klicken, Doppelklicken, Drücken der EINGABETASTE oder durch eine vordefinierte oder alternative Tastenkombination aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d23a-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="9d23a-127">Das Ereignis **Aufruf** Ereignis ([**UIA \_ aufrufen \_ invokedeventid**](uiauto-event-ids.md)) wird für ein Steuerelement ausgelöst, das aktiviert wurde (als Antwort auf ein Steuerelement, das die zugehörige Aktion ausführt).</span><span class="sxs-lookup"><span data-stu-id="9d23a-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="9d23a-128">Sofern möglich, sollte das Ereignis ausgelöst werden, nachdem das Steuerelement die Aktion abgeschlossen hat und ohne Blockierung zurückgekehrt ist.</span><span class="sxs-lookup"><span data-stu-id="9d23a-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="9d23a-129">Das **aufgerufene** Ereignis (**UIA \_ -Aufruf \_ invoketoventid**) sollte vor der Wartung der **Aufruf** Anforderung in den folgenden Szenarien ausgelöst werden:</span><span class="sxs-lookup"><span data-stu-id="9d23a-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="9d23a-130">Es ist nicht möglich oder zweckmäßig, bis zum Abschluss der Aktion zu warten.</span><span class="sxs-lookup"><span data-stu-id="9d23a-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="9d23a-131">Die Aktion erfordert eine Benutzeraktion.</span><span class="sxs-lookup"><span data-stu-id="9d23a-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="9d23a-132">Die Aktion ist zeitaufwändig und führt dazu, dass der aufrufende Client für einen längeren Zeitraum blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d23a-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="9d23a-133">Wenn das Aufrufen des Steuer Elements bedeutende Nebeneffekte hat, sollten diese Nebeneffekte über die **HelpText** -Eigenschaft verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="9d23a-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="9d23a-134">Wenn z. b. [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) nicht mit der Auswahl verknüpft ist, kann der **Aufruf** bewirken, dass ein anderes Steuerelement ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9d23a-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="9d23a-135">Hover-(oder Mouseover) Effekte stellen im Allgemeinen kein **aufgerufenes** Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="9d23a-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="9d23a-136">Allerdings sollten Steuerelemente, die eine Aktion ausführen (im Gegensatz zur Ursache eines visuellen Effekts), das Steuerelement Muster **aufrufen** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9d23a-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="9d23a-137">Diese Implementierung wird als Problem für Barrierefreiheit betrachtet, wenn das Steuerelement nur als Ergebnis eines mausbezogenen Nebeneffekts aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d23a-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="9d23a-138">Das Aufrufen eines Steuerelements unterscheidet sich vom Auswählen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="9d23a-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="9d23a-139">Abhängig vom Steuerelement kann das Aufrufen jedoch möglicherweise den Nebeneffekt haben, dass das Element ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9d23a-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="9d23a-140">Wenn Sie z. b. ein Microsoft Word-Dokument Listenelement im Ordner "eigene Dokumente" aufrufen, wird das Element ausgewählt und das Dokument geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9d23a-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="9d23a-141">Ein Element kann beim Aufrufen nicht sofort aus der Microsoft UI Automation-Struktur verschwinden.</span><span class="sxs-lookup"><span data-stu-id="9d23a-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="9d23a-142">Dies kann zur Folge haben, dass das Anfordern von Informationen von dem Element, die durch den Ereignisrückruf bereitgestellt werden, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9d23a-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="9d23a-143">Als Problemlösung wird empfohlen, zwischengespeicherte Informationen vorab abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9d23a-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="9d23a-144">Steuerelemente können mehrere Steuerelementmuster implementieren.</span><span class="sxs-lookup"><span data-stu-id="9d23a-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="9d23a-145">Beispielsweise implementiert das **Füllfarbe** -Steuerelement auf der Microsoft Excel-Symbolleiste sowohl das Aufruf-als auch das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="9d23a-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="9d23a-146">Das ExpandCollapse-Steuerelement Muster macht das Menü verfügbar, und das Muster zum **aufrufen** des Steuer Elements füllt die aktive Auswahl mit der ausgewählten Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="9d23a-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="9d23a-147">Erforderliche Member für **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="9d23a-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="9d23a-148">Die folgende Methode ist für die Implementierung der [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d23a-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="9d23a-149">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="9d23a-149">Required members</span></span>                                | <span data-ttu-id="9d23a-150">Memberart</span><span class="sxs-lookup"><span data-stu-id="9d23a-150">Member type</span></span> | <span data-ttu-id="9d23a-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d23a-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d23a-152">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="9d23a-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="9d23a-153">Methode</span><span class="sxs-lookup"><span data-stu-id="9d23a-153">Method</span></span>      | <span data-ttu-id="9d23a-154">" **Aufrufen** " ist ein asynchroner Aufruf und muss sofort ohne Blockierung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d23a-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="9d23a-155">Dieses Verhalten ist insbesondere für Steuerelemente wichtig, die direkt oder indirekt ein modales Dialogfeld starten, wenn sie aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9d23a-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="9d23a-156">Jeder Benutzeroberflächenautomatisierungs-Client, der das Ereignis ausgelöst hat, bleibt blockiert, bis das modale Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9d23a-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="9d23a-157">Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9d23a-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d23a-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d23a-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d23a-159">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9d23a-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9d23a-160">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9d23a-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9d23a-161">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="9d23a-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="9d23a-162">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="9d23a-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





