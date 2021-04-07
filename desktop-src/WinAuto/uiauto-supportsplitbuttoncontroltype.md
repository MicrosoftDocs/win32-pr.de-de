---
title: SplitButton-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den SplitButton-Steuer Elementtyp.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Steuer Elementtyp "SplitButton
- Benutzeroberflächenautomatisierungs, SplitButton-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Eigenschaften für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für den SplitButton-Steuer Elementtyp
- Struktur Strukturen, SplitButton-Steuer Elementtyp
- Eigenschaften, SplitButton-Steuer Elementtyp
- Steuerelement Muster, SplitButton-Steuer Elementtyp
- Ereignisse, SplitButton-Steuer Elementtyp
- Unterstützung für den SplitButton-Steuer Elementtyp
- SplitButton-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für den SplitButton-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den SplitButton-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für SplitButton
- Steuerelement Typen, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712696"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="67802-119">SplitButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="67802-119">SplitButton Control Type</span></span>

<span data-ttu-id="67802-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **SplitButton** -Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="67802-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="67802-121">Das Steuerelement unterteilte Schaltflächen ermöglicht das Ausführen einer Aktion für ein Steuerelement und das Erweitern des Steuer Elements, um eine Liste mit anderen möglichen Aktionen anzuzeigen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="67802-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="67802-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **SplitButton** -Steuer Elementtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="67802-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="67802-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Steuerelemente für unterteilte Schaltflächen, in denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement</span><span class="sxs-lookup"><span data-stu-id="67802-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="67802-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="67802-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="67802-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="67802-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="67802-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67802-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="67802-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="67802-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="67802-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="67802-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="67802-129">Beispiel für den SplitButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="67802-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="67802-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67802-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="67802-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="67802-131">Typical Tree Structure</span></span>

<span data-ttu-id="67802-132">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für unterteilte Schaltflächen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="67802-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="67802-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="67802-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67802-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="67802-134">Control View</span></span></th>
<th><span data-ttu-id="67802-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="67802-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="67802-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="67802-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="67802-137">Bild (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="67802-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="67802-138">Text (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="67802-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="67802-139">Button (1 oder 2)</span><span class="sxs-lookup"><span data-stu-id="67802-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="67802-140">Menu (0 oder 1; wird als untergeordnetes Element einer untergeordneten Schaltfläche angezeigt, die das ExpandCollapse-Muster unterstützt)</span><span class="sxs-lookup"><span data-stu-id="67802-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="67802-141">MenuItem (1:n)</span><span class="sxs-lookup"><span data-stu-id="67802-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="67802-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="67802-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="67802-143">Button (1 oder 2)</span><span class="sxs-lookup"><span data-stu-id="67802-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="67802-144">MenuItem (1:n)</span><span class="sxs-lookup"><span data-stu-id="67802-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="67802-145">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67802-145">Relevant Properties</span></span>

<span data-ttu-id="67802-146">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **SplitButton** -Steuer Elementtyp besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="67802-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="67802-147">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="67802-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="67802-148">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67802-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="67802-149">Wert</span><span class="sxs-lookup"><span data-stu-id="67802-149">Value</span></span>           | <span data-ttu-id="67802-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="67802-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67802-151">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="67802-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-152">See notes.</span></span>      | <span data-ttu-id="67802-153">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="67802-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="67802-154">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="67802-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-155">See notes.</span></span>      | <span data-ttu-id="67802-156">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="67802-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="67802-157">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="67802-158">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-158">See notes.</span></span>      | <span data-ttu-id="67802-159">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="67802-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="67802-160">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="67802-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="67802-161">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="67802-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="67802-162">**SplitButton**</span></span> | <span data-ttu-id="67802-163">Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="67802-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="67802-164">**UIA \_ helptextpropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="67802-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-165">See notes.</span></span>      | <span data-ttu-id="67802-166">Der Hilfetext kann das Ergebnis der Aktivierung der unterteilten Schaltfläche angeben. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="67802-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="67802-167">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="67802-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="67802-168">TRUE</span></span>            | <span data-ttu-id="67802-169">Das Steuerelement für eine unterteilte Schaltfläche enthält Informationen für den Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="67802-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="67802-170">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="67802-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="67802-171">TRUE</span></span>            | <span data-ttu-id="67802-172">Das Steuerelement für eine unterteilte Schaltfläche ist für den Endbenutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="67802-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="67802-173">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="67802-174">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-174">See notes.</span></span>      | <span data-ttu-id="67802-175">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67802-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="67802-176">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="67802-177">NULL</span><span class="sxs-lookup"><span data-stu-id="67802-177">NULL</span></span>            | <span data-ttu-id="67802-178">Steuerelemente für unterteilte Schaltflächen verfügen nicht über eine statische Textbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="67802-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="67802-179">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="67802-180">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-180">See notes.</span></span>      | <span data-ttu-id="67802-181">Lokalisierte Zeichenfolge, die dem **SplitButton** -Steuer Elementtyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="67802-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="67802-182">Der Standardwert ist "unterteilte Schaltfläche" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="67802-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="67802-183">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="67802-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="67802-184">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67802-184">See notes.</span></span>      | <span data-ttu-id="67802-185">Der Text, der zum bezeichnen der Trenn Schaltfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67802-185">The text that is used to label the split button.</span></span> <span data-ttu-id="67802-186">Wenn ein Bild zum Bezeichnen einer unterteilten Schaltfläche verwendet wird, muss für die Eigenschaft Name der unterteilten Schaltfläche alternativer Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="67802-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="67802-187">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="67802-187">Required Control Patterns</span></span>

<span data-ttu-id="67802-188">In der folgenden Tabelle sind die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgeführt</span><span class="sxs-lookup"><span data-stu-id="67802-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="67802-189">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="67802-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="67802-190">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="67802-190">Control Pattern</span></span>                                                   | <span data-ttu-id="67802-191">Support</span><span class="sxs-lookup"><span data-stu-id="67802-191">Support</span></span>  | <span data-ttu-id="67802-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="67802-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67802-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="67802-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="67802-194">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="67802-194">Required</span></span> | <span data-ttu-id="67802-195">Da unterteilte Schaltflächen immer in der Lage sind, eine Liste von Optionen zu erweitern, müssen Sie das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67802-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="67802-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="67802-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="67802-197">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="67802-197">Required</span></span> | <span data-ttu-id="67802-198">Da Trenn Schaltflächen immer über eine Standardaktion verfügen, die der [**IInvokeProvider:: Aufrufen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) -Methode zugeordnet ist, müssen Sie [das Steuerelement](uiauto-implementinginvoke.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67802-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="67802-199">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="67802-199">Required Events</span></span>

<span data-ttu-id="67802-200">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die unterteilte Schaltflächen-Steuerelemente für die</span><span class="sxs-lookup"><span data-stu-id="67802-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="67802-201">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="67802-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="67802-202">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="67802-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="67802-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="67802-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67802-204">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="67802-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="67802-205">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67802-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="67802-206">[**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67802-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="67802-207">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="67802-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="67802-208">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67802-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="67802-209">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67802-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="67802-210">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67802-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="67802-211">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67802-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="67802-212">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="67802-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="67802-213">Beispiel für den SplitButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="67802-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="67802-214">Die folgende Abbildung veranschaulicht ein Steuerelement, das den **SplitButton** -Steuer Elementtyp implementiert.</span><span class="sxs-lookup"><span data-stu-id="67802-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![Screenshot mit einem Beispiel für ein SplitButton-Steuerelement](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67802-216">Benutzeroberflächenautomatisierungs-Struktur – Steuerelement Ansicht</span><span class="sxs-lookup"><span data-stu-id="67802-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="67802-217">Benutzeroberflächenautomatisierungs-Struktur – Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="67802-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="67802-218">SplitButton- &quot; Name &quot; (aufrufen, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="67802-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="67802-219">Schaltfläche " &quot; Weitere Optionen" &quot; (aufrufen)</span><span class="sxs-lookup"><span data-stu-id="67802-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="67802-220">Menü</span><span class="sxs-lookup"><span data-stu-id="67802-220">Menu</span></span>
<ul>
<li><span data-ttu-id="67802-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="67802-221">MenuItem</span></span></li>
<li><span data-ttu-id="67802-222">...</span><span class="sxs-lookup"><span data-stu-id="67802-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="67802-223">SplitButton- &quot; Name &quot; (aufrufen, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="67802-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="67802-224">Schaltfläche " &quot; Weitere Optionen" &quot; (aufrufen)</span><span class="sxs-lookup"><span data-stu-id="67802-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="67802-225">Menü</span><span class="sxs-lookup"><span data-stu-id="67802-225">Menu</span></span>
<ul>
<li><span data-ttu-id="67802-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="67802-226">MenuItem</span></span></li>
<li><span data-ttu-id="67802-227">...</span><span class="sxs-lookup"><span data-stu-id="67802-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="67802-228">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67802-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67802-229">**Licher**</span><span class="sxs-lookup"><span data-stu-id="67802-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67802-230">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="67802-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="67802-231">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="67802-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




