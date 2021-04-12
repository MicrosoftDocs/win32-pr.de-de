---
title: TabItem-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den TabItem-Steuer Elementtyp.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, TabItem-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für TabItem-Steuer Elementtyp
- Baumstrukturen, TabItem-Steuer Elementtyp
- Eigenschaften, TabItem-Steuer Elementtyp
- Steuerelement Muster, TabItem-Steuer Elementtyp
- Ereignisse, TabItem-Steuer Elementtyp
- Unterstützung für den TabItem-Steuer Elementtyp
- TabItem-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für TabItem-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den TabItem-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für TabItem
- Steuerelement Typen, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207192"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="6b8f3-119">TabItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6b8f3-119">TabItem Control Type</span></span>

<span data-ttu-id="6b8f3-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **TabItem** -Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="6b8f3-121">Ein Registerkartenelement-Steuerelement (TabItem) wird in einem Registerkarten-Steuerelement (Tab) als das Steuerelement verwendet, über das eine bestimmte Seite ausgewählt wird, die in einem Fenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="6b8f3-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **TabItem** -Steuer Elementtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="6b8f3-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Registerkarten Element-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6b8f3-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6b8f3-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6b8f3-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="6b8f3-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6b8f3-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b8f3-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6b8f3-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6b8f3-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6b8f3-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6b8f3-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6b8f3-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6b8f3-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="6b8f3-130">Typical Tree Structure</span></span>

<span data-ttu-id="6b8f3-131">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Registerkarten Element-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6b8f3-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b8f3-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="6b8f3-133">Control View</span></span></th>
<th><span data-ttu-id="6b8f3-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="6b8f3-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6b8f3-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="6b8f3-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="6b8f3-136">Bild (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="6b8f3-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="6b8f3-137">Text</span><span class="sxs-lookup"><span data-stu-id="6b8f3-137">Text</span></span></li>
<li><span data-ttu-id="6b8f3-138">Bereich</span><span class="sxs-lookup"><span data-stu-id="6b8f3-138">Pane</span></span>
<ul>
<li><span data-ttu-id="6b8f3-139">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="6b8f3-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b8f3-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="6b8f3-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="6b8f3-141">Bereich</span><span class="sxs-lookup"><span data-stu-id="6b8f3-141">Pane</span></span>
<ul>
<li><span data-ttu-id="6b8f3-142">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="6b8f3-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="6b8f3-143">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b8f3-143">Relevant Properties</span></span>

<span data-ttu-id="6b8f3-144">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **TabItem** -Steuer Elementtyp besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="6b8f3-145">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6b8f3-146">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6b8f3-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6b8f3-147">Wert</span><span class="sxs-lookup"><span data-stu-id="6b8f3-147">Value</span></span>       | <span data-ttu-id="6b8f3-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b8f3-149">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6b8f3-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-150">See notes.</span></span>  | <span data-ttu-id="6b8f3-151">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="6b8f3-152">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6b8f3-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-153">See notes.</span></span>  | <span data-ttu-id="6b8f3-154">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="6b8f3-155">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6b8f3-156">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-156">See notes.</span></span>  | <span data-ttu-id="6b8f3-157">Das Registerkartenelement-Steuerelement muss einen klickbaren Punkt haben, über den veranlasst wird, dass das Element ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="6b8f3-158">**UIA \_ controllerforpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="6b8f3-159">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-159">See notes.</span></span>  | <span data-ttu-id="6b8f3-160">Diese Eigenschaft kann als Zeiger auf den zugeordneten Registerkartenbereich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="6b8f3-161">Dies ist nützlich, wenn der Bereich keinen Bereich als untergeordnetes Element des Registerkartenelement-Objekts hosten kann.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="6b8f3-162">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6b8f3-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-163">**TabItem**</span></span> | <span data-ttu-id="6b8f3-164">Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="6b8f3-165">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6b8f3-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b8f3-166">TRUE</span></span>        | <span data-ttu-id="6b8f3-167">Das Registerkarten Element-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="6b8f3-168">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6b8f3-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b8f3-169">TRUE</span></span>        | <span data-ttu-id="6b8f3-170">Das Registerkarten Element-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="6b8f3-171">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6b8f3-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-172">See notes.</span></span>  | <span data-ttu-id="6b8f3-173">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="6b8f3-174">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6b8f3-175">Null</span><span class="sxs-lookup"><span data-stu-id="6b8f3-175">Null</span></span>        | <span data-ttu-id="6b8f3-176">Das Registerkartenelement-Steuerelement hat keine statische Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="6b8f3-177">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6b8f3-178">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-178">See notes.</span></span>  | <span data-ttu-id="6b8f3-179">Lokalisierte Zeichenfolge für den Steuer Elementtyp " **TabItem** ".</span><span class="sxs-lookup"><span data-stu-id="6b8f3-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="6b8f3-180">Der Standardwert ist "Registerkarten Element" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="6b8f3-181">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6b8f3-182">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-182">See notes.</span></span>  | <span data-ttu-id="6b8f3-183">Das Registerkarten Element-Steuerelement ist selbst beschriftet.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6b8f3-184">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6b8f3-184">Required Control Patterns</span></span>

<span data-ttu-id="6b8f3-185">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Registerkarten-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="6b8f3-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="6b8f3-186">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6b8f3-187">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="6b8f3-187">Control Pattern</span></span>                                                 | <span data-ttu-id="6b8f3-188">Support</span><span class="sxs-lookup"><span data-stu-id="6b8f3-188">Support</span></span>  | <span data-ttu-id="6b8f3-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b8f3-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="6b8f3-191">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6b8f3-191">Required</span></span> | <span data-ttu-id="6b8f3-192">Das Registerkarten Element-Steuerelement muss [**iuiautomationselectionitempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern)unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="6b8f3-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="6b8f3-194">Nie</span><span class="sxs-lookup"><span data-stu-id="6b8f3-194">Never</span></span>    | <span data-ttu-id="6b8f3-195">Das Registerkarten Element-Steuerelement unterstützt niemals [**iuiautomationinvokepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="6b8f3-196">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6b8f3-196">Required Events</span></span>

<span data-ttu-id="6b8f3-197">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Registerkarten Element-Steuerelemente zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="6b8f3-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="6b8f3-198">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6b8f3-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6b8f3-199">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="6b8f3-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="6b8f3-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b8f3-201">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="6b8f3-202">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="6b8f3-203">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="6b8f3-204">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="6b8f3-205">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="6b8f3-206">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b8f3-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="6b8f3-207">**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="6b8f3-208">**UIA \_ SelectionItem \_ elementselectedebug**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="6b8f3-209">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="6b8f3-210">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b8f3-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6b8f3-211">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6b8f3-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b8f3-212">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6b8f3-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6b8f3-213">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6b8f3-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




