---
title: Separator-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuer Zeichentyp.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für Trenn Zeichentyp
- Benutzeroberflächenautomatisierungs-Steuerelement Typen
- UI-Automatisierung, Struktur für Trenn Zeichentyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für Steuerelement-Trennzeichen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Steuerelement-Trennzeichen
- Benutzeroberflächenautomatisierungs, Ereignisse für Trenn Zeichentyp
- Struktur Strukturen, Trenn Steuerelement-Typ
- Eigenschaften, Separator-Steuerelement Typen
- Steuerelement Muster, Trenn Zeichentyp
- Ereignisse, Separator-Steuerelement Typen
- Unterstützung für Trenn Zeichentyp
- Trennzeichensteuerelementtyp
- Steuerelement Typen, Struktur für Trenn Zeichentyp
- Steuerelement Typen, Steuerelement Muster für Trennzeichen-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Trennzeichen
- Steuerelement Typen, Trennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515932"
---
# <a name="separator-control-type"></a><span data-ttu-id="5f29f-119">Separator-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="5f29f-119">Separator Control Type</span></span>

<span data-ttu-id="5f29f-120">Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuer Zeichentyp.</span><span class="sxs-lookup"><span data-stu-id="5f29f-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="5f29f-121">Mithilfe von Separator-Steuerelementen wird ein Bereich visuell in zwei Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="5f29f-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="5f29f-122">Ein Separator-Steuerelement kann z. B. eine Leiste sein, die zwei Bereiche in einem Fenster definiert.</span><span class="sxs-lookup"><span data-stu-id="5f29f-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="5f29f-123">Wenn die Trennlinie verschoben werden kann, sollte das Steuerelement als Steuerelementtyp „Thumb“ verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="5f29f-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="5f29f-124">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuerelement- **Trenn** Zeichentyp definiert.</span><span class="sxs-lookup"><span data-stu-id="5f29f-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="5f29f-125">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Trenn Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und</span><span class="sxs-lookup"><span data-stu-id="5f29f-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5f29f-126">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="5f29f-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5f29f-127">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="5f29f-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5f29f-128">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f29f-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5f29f-129">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="5f29f-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5f29f-130">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5f29f-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5f29f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f29f-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5f29f-132">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="5f29f-132">Typical Tree Structure</span></span>

<span data-ttu-id="5f29f-133">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Separator-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f29f-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5f29f-134">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5f29f-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f29f-135">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="5f29f-135">Control View</span></span></th>
<th><span data-ttu-id="5f29f-136">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="5f29f-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5f29f-137">Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="5f29f-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5f29f-138">Der Steuer Zeichentyp des <strong>Trenn</strong> Zeichens hat nie Inhalt.</span><span class="sxs-lookup"><span data-stu-id="5f29f-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="5f29f-139">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f29f-139">Relevant Properties</span></span>

<span data-ttu-id="5f29f-140">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Trennzeichen Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="5f29f-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="5f29f-141">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="5f29f-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5f29f-142">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f29f-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5f29f-143">Wert</span><span class="sxs-lookup"><span data-stu-id="5f29f-143">Value</span></span>         | <span data-ttu-id="5f29f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f29f-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f29f-145">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5f29f-146">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5f29f-146">See notes.</span></span>    | <span data-ttu-id="5f29f-147">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5f29f-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="5f29f-148">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5f29f-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5f29f-149">See notes.</span></span>    | <span data-ttu-id="5f29f-150">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="5f29f-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="5f29f-151">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5f29f-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5f29f-152">See notes.</span></span>    | <span data-ttu-id="5f29f-153">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="5f29f-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5f29f-154">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5f29f-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="5f29f-155">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5f29f-156">**Trennzeichen**</span><span class="sxs-lookup"><span data-stu-id="5f29f-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="5f29f-157">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5f29f-158">false</span><span class="sxs-lookup"><span data-stu-id="5f29f-158">FALSE</span></span>         | <span data-ttu-id="5f29f-159">Das Separator-Steuerelement ist nie ein Inhaltselement.</span><span class="sxs-lookup"><span data-stu-id="5f29f-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="5f29f-160">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5f29f-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="5f29f-161">TRUE</span></span>          | <span data-ttu-id="5f29f-162">Das Separator-Steuerelement muss immer ein Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="5f29f-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="5f29f-163">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5f29f-164">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5f29f-164">See notes.</span></span>    | <span data-ttu-id="5f29f-165">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5f29f-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="5f29f-166">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5f29f-167">NULL</span><span class="sxs-lookup"><span data-stu-id="5f29f-167">NULL</span></span>          | <span data-ttu-id="5f29f-168">Das Separator-Steuerelement hat keine statische Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="5f29f-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="5f29f-169">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5f29f-170">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5f29f-170">See notes.</span></span>    | <span data-ttu-id="5f29f-171">Lokalisierte Zeichenfolge für den Steuer Zeichentyp des **Trenn** Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5f29f-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="5f29f-172">Der Standardwert ist "Separator" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="5f29f-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="5f29f-173">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5f29f-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5f29f-174">""</span><span class="sxs-lookup"><span data-stu-id="5f29f-174">""</span></span>            | <span data-ttu-id="5f29f-175">Das Trennzeichen Steuerelement erfordert keine **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5f29f-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5f29f-176">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="5f29f-176">Required Control Patterns</span></span>

<span data-ttu-id="5f29f-177">Das Separator-Steuerelement ist nicht erforderlich, um Steuerelementmuster zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5f29f-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="5f29f-178">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5f29f-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="5f29f-179">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5f29f-179">Required Events</span></span>

<span data-ttu-id="5f29f-180">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Trenn Steuerelementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5f29f-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="5f29f-181">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5f29f-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5f29f-182">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f29f-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5f29f-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f29f-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f29f-184">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="5f29f-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5f29f-185">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5f29f-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5f29f-186">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5f29f-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5f29f-187">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5f29f-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5f29f-188">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5f29f-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5f29f-189">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5f29f-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5f29f-190">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="5f29f-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5f29f-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f29f-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5f29f-192">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5f29f-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f29f-193">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="5f29f-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5f29f-194">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="5f29f-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




