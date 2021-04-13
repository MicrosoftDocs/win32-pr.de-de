---
title: Gruppen Steuerungstyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Gruppen Steuerelement-Typ.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Steuerelement
- Benutzeroberflächenautomatisierungs, Gruppen Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Struktur für Gruppen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Gruppen Steuerungstyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Gruppen Steuerungstyp
- Benutzeroberflächenautomatisierungs, Ereignisse für den Gruppen Steuerungstyp
- Struktur Strukturen, Gruppen Steuerelement Typen
- Eigenschaften, Gruppen Steuerelement-Typ
- Steuerelement Muster, Gruppen Steuerelement-Typ
- Ereignisse, Gruppen Steuerelement Typen
- Unterstützung für den Gruppen Steuerungstyp
- Gruppe-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Gruppen Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den Gruppen Steuerungstyp
- Steuerelement Typen, Unterstützung für Gruppe
- Steuerelement Typen, Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388246"
---
# <a name="group-control-type"></a><span data-ttu-id="9763f-119">Gruppen Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="9763f-119">Group Control Type</span></span>

<span data-ttu-id="9763f-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Gruppen** Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="9763f-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="9763f-121">Ein Gruppen Steuerelement stellt einen Knoten innerhalb einer Hierarchie dar.</span><span class="sxs-lookup"><span data-stu-id="9763f-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="9763f-122">Der Steuer Elementtyp " **Group** " erstellt eine Trennung in der Benutzeroberflächenautomatisierungs-Struktur, sodass Elemente, die gruppiert werden, eine logische Division innerhalb der Benutzeroberflächenautomatisierungs-Struktur aufweisen</span><span class="sxs-lookup"><span data-stu-id="9763f-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="9763f-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Gruppen** Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="9763f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="9763f-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Gruppen Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und</span><span class="sxs-lookup"><span data-stu-id="9763f-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9763f-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9763f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9763f-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9763f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9763f-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9763f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9763f-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9763f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9763f-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9763f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9763f-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9763f-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9763f-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9763f-131">Typical Tree Structure</span></span>

<span data-ttu-id="9763f-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Gruppen Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9763f-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9763f-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9763f-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9763f-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="9763f-134">Control View</span></span></th>
<th><span data-ttu-id="9763f-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="9763f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9763f-136">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="9763f-136">Group</span></span>
<ul>
<li><span data-ttu-id="9763f-137">Beliebig viele Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9763f-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9763f-138">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="9763f-138">Group</span></span>
<ul>
<li><span data-ttu-id="9763f-139">Beliebig viele Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9763f-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9763f-140">Gruppen Steuerelemente enthalten in der Regel Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen, die sich in der Teilstruktur darunter befinden, einschließlich der Steuerelement Typen [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)und [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="9763f-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="9763f-141">Da es sich bei einem Gruppen Steuerelement um einen generischen Container handelt, ist es möglich, dass jeder Typ von Steuerelement unter dem Gruppen Steuerelement in der Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="9763f-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9763f-142">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9763f-142">Relevant Properties</span></span>

<span data-ttu-id="9763f-143">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Gruppen Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="9763f-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="9763f-144">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9763f-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9763f-145">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9763f-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9763f-146">Wert</span><span class="sxs-lookup"><span data-stu-id="9763f-146">Value</span></span>      | <span data-ttu-id="9763f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="9763f-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9763f-148">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9763f-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-149">See notes.</span></span> | <span data-ttu-id="9763f-150">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9763f-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="9763f-151">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9763f-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-152">See notes.</span></span> | <span data-ttu-id="9763f-153">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="9763f-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="9763f-154">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9763f-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-155">See notes.</span></span> | <span data-ttu-id="9763f-156">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="9763f-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9763f-157">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9763f-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="9763f-158">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9763f-159">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="9763f-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="9763f-160">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9763f-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9763f-161">**TRUE**</span></span>   | <span data-ttu-id="9763f-162">Das Gruppen Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="9763f-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="9763f-163">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9763f-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9763f-164">**TRUE**</span></span>   | <span data-ttu-id="9763f-165">Das Gruppen Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="9763f-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="9763f-166">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9763f-167">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-167">See notes.</span></span> | <span data-ttu-id="9763f-168">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="9763f-169">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9763f-170">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-170">See notes.</span></span> | <span data-ttu-id="9763f-171">Gruppensteuerelemente sind in der Regel selbstbezeichnend.</span><span class="sxs-lookup"><span data-stu-id="9763f-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="9763f-172">In diesen Fällen wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9763f-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="9763f-173">Wenn die Gruppe über eine statische Text Bezeichnung verfügt, geben Sie die Bezeichnung als Wert der Eigenschaft " **LabeledBy** " zurück.</span><span class="sxs-lookup"><span data-stu-id="9763f-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="9763f-174">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9763f-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-175">See notes.</span></span> | <span data-ttu-id="9763f-176">Lokalisierte Zeichenfolge, die **dem Steuerelement** des Steuer Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="9763f-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="9763f-177">Der Standardwert ist "Group" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="9763f-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="9763f-178">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9763f-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9763f-179">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9763f-179">See notes.</span></span> | <span data-ttu-id="9763f-180">Das Gruppensteuerelement ruft seinen Namen in der Regel aus dem Text ab, mit dem das Steuerelement beschriftet ist.</span><span class="sxs-lookup"><span data-stu-id="9763f-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9763f-181">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9763f-181">Required Control Patterns</span></span>

<span data-ttu-id="9763f-182">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die für den **Gruppen** Steuerelement-Typ unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="9763f-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="9763f-183">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9763f-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9763f-184">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="9763f-184">Control Pattern</span></span>                                                   | <span data-ttu-id="9763f-185">Support</span><span class="sxs-lookup"><span data-stu-id="9763f-185">Support</span></span> | <span data-ttu-id="9763f-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="9763f-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9763f-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9763f-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9763f-188">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="9763f-188">Depends</span></span> | <span data-ttu-id="9763f-189">Gruppen Steuerelemente, die zum Anzeigen oder Ausblenden von Informationen verwendet werden können, müssen das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="9763f-190">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9763f-190">Required Events</span></span>

<span data-ttu-id="9763f-191">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Gruppen Steuerelementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9763f-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="9763f-192">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9763f-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9763f-193">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="9763f-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="9763f-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="9763f-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9763f-195">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="9763f-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="9763f-196">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9763f-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="9763f-197">[**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9763f-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="9763f-198">Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster-Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="9763f-199">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9763f-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="9763f-200">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="9763f-201">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9763f-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="9763f-202">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="9763f-203">[**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9763f-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="9763f-204">Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9763f-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="9763f-205">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="9763f-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9763f-206">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9763f-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9763f-207">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9763f-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9763f-208">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9763f-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9763f-209">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9763f-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




