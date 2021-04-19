---
title: Header Item-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Header Item-Steuer Elementtyp.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs-, Baumstruktur für Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für Header Item-Steuer Elementtyp
- Struktur Strukturen, Header Item-Steuer Elementtyp
- Eigenschaften, Header Item-Steuer Elementtyp
- Steuerelement Muster, Header Item-Steuer Elementtyp
- Ereignisse, Header Item-Steuer Elementtyp
- Unterstützung für den Header Item-Steuer Elementtyp
- Header Item-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für Header Item-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den Header Item-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für Header Item
- Steuerelement Typen, Header Item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342263"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="e4093-119">Header Item-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e4093-119">HeaderItem Control Type</span></span>

<span data-ttu-id="e4093-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Header** Item-Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="e4093-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="e4093-121">Der **Header** Item-Steuer Elementtyp stellt eine visuelle Bezeichnung für eine Zeile oder Spalte mit Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e4093-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="e4093-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Header** Item-Steuer Elementtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="e4093-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="e4093-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Header Element-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="e4093-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e4093-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e4093-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e4093-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="e4093-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e4093-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4093-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e4093-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="e4093-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e4093-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e4093-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e4093-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4093-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e4093-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="e4093-130">Typical Tree Structure</span></span>

<span data-ttu-id="e4093-131">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Header Element-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4093-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e4093-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e4093-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4093-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="e4093-133">Control View</span></span></th>
<th><span data-ttu-id="e4093-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="e4093-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e4093-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="e4093-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="e4093-136">(Nicht vorhanden)</span><span class="sxs-lookup"><span data-stu-id="e4093-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e4093-137">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4093-137">Relevant Properties</span></span>

<span data-ttu-id="e4093-138">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **Header** Item-Steuer Elementtyp besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="e4093-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="e4093-139">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e4093-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e4093-140">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4093-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e4093-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e4093-141">Value</span></span>          | <span data-ttu-id="e4093-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4093-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4093-143">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e4093-144">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-144">See notes.</span></span>     | <span data-ttu-id="e4093-145">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="e4093-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="e4093-146">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e4093-147">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-147">See notes.</span></span>     | <span data-ttu-id="e4093-148">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="e4093-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="e4093-149">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e4093-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-150">See notes.</span></span>     | <span data-ttu-id="e4093-151">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="e4093-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="e4093-152">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e4093-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="e4093-153">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e4093-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="e4093-154">**HeaderItem**</span></span> | <span data-ttu-id="e4093-155">Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="e4093-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e4093-156">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e4093-157">false</span><span class="sxs-lookup"><span data-stu-id="e4093-157">FALSE</span></span>          | <span data-ttu-id="e4093-158">Das Header Element-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4093-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="e4093-159">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e4093-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="e4093-160">TRUE</span></span>           | <span data-ttu-id="e4093-161">Das Header Element-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4093-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="e4093-162">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e4093-163">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-163">See notes.</span></span>     | <span data-ttu-id="e4093-164">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4093-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="e4093-165">**UIA \_ itemstatuspropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="e4093-166">Siehe Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4093-166">See notes</span></span>      | <span data-ttu-id="e4093-167">Diese Eigenschaft stellt Informationen für Sortierreihenfolgen nach Headerelement bereit.</span><span class="sxs-lookup"><span data-stu-id="e4093-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="e4093-168">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e4093-169">NULL</span><span class="sxs-lookup"><span data-stu-id="e4093-169">NULL</span></span>           | <span data-ttu-id="e4093-170">Header Element-Steuerelemente verfügen nicht über eine statische Text Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="e4093-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="e4093-171">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e4093-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-172">See notes.</span></span>     | <span data-ttu-id="e4093-173">Lokalisierte Zeichenfolge für den Steuer Elementtyp " **Header** Item".</span><span class="sxs-lookup"><span data-stu-id="e4093-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="e4093-174">Der Standardwert ist "Header Element" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="e4093-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="e4093-175">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="e4093-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e4093-176">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4093-176">See notes.</span></span>     | <span data-ttu-id="e4093-177">Das Headerelement-Steuerelement ist immer selbstbezeichnend.</span><span class="sxs-lookup"><span data-stu-id="e4093-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e4093-178">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="e4093-178">Required Control Patterns</span></span>

<span data-ttu-id="e4093-179">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Header Element-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="e4093-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="e4093-180">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e4093-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="e4093-181">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="e4093-181">Control Pattern</span></span>                                         | <span data-ttu-id="e4093-182">Support</span><span class="sxs-lookup"><span data-stu-id="e4093-182">Support</span></span> | <span data-ttu-id="e4093-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4093-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4093-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="e4093-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="e4093-185">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="e4093-185">Depends</span></span> | <span data-ttu-id="e4093-186">Implementieren Sie das [Aufruf](uiauto-implementinginvoke.md) Steuerelement Muster, wenn zum Sortieren der Daten auf das Header Element-Steuerelement geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4093-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="e4093-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="e4093-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="e4093-188">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="e4093-188">Depends</span></span> | <span data-ttu-id="e4093-189">Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn die Größe des Header Element-Steuer Elements geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4093-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="e4093-190">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e4093-190">Required Events</span></span>

<span data-ttu-id="e4093-191">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Header Element-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="e4093-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="e4093-192">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e4093-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e4093-193">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="e4093-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e4093-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4093-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4093-195">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="e4093-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="e4093-196">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e4093-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="e4093-197">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="e4093-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="e4093-198">Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4093-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="e4093-199">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e4093-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e4093-200">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4093-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="e4093-201">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e4093-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e4093-202">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4093-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="e4093-203">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="e4093-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e4093-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4093-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e4093-205">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e4093-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e4093-206">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="e4093-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e4093-207">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="e4093-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




