---
title: ToolBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement-Typ Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Steuerelement Typen
- UI-Automatisierung, Symbolleisten-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Struktur für Symbolleisten-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Symbolleisten-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den ToolBar-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für ToolBar-Steuerelement Typen
- Struktur Strukturen, Symbolleisten-Steuerelement Typen
- Eigenschaften, Symbolleisten-Steuerelement Typen
- Steuerelement Muster, Symbolleisten-Steuerelement Typen
- Ereignisse, Symbolleisten-Steuerelement Typen
- Unterstützung für Symbolleisten-Steuerelement
- ToolBar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Symbolleisten-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für ToolBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Symbolleiste
- Steuerelement Typen, Symbolleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388688"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="530d4-120">ToolBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="530d4-120">ToolBar Control Type</span></span>

<span data-ttu-id="530d4-121">Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="530d4-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="530d4-122">Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="530d4-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="530d4-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse **für den Steuer** Element-Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="530d4-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="530d4-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Symbolleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="530d4-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="530d4-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="530d4-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="530d4-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="530d4-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="530d4-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="530d4-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="530d4-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="530d4-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="530d4-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="530d4-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="530d4-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="530d4-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="530d4-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="530d4-131">Typical Tree Structure</span></span>

<span data-ttu-id="530d4-132">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für ToolBar-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="530d4-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="530d4-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="530d4-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="530d4-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="530d4-134">Control View</span></span></th>
<th><span data-ttu-id="530d4-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="530d4-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="530d4-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="530d4-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="530d4-137">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="530d4-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="530d4-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="530d4-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="530d4-139">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="530d4-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="530d4-140">Ein ToolBar-Steuerelement kann jede Art von Steuerelement in seiner Unterstruktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="530d4-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="530d4-141">Am häufigsten enthalten sie Schaltflächen, Kombinationsfelder und unterteilte Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="530d4-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="530d4-142">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="530d4-142">Relevant Properties</span></span>

<span data-ttu-id="530d4-143">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition **für den Steuer** Element-Steuerelement Typ besonders relevant ist</span><span class="sxs-lookup"><span data-stu-id="530d4-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="530d4-144">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="530d4-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="530d4-145">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="530d4-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="530d4-146">Wert</span><span class="sxs-lookup"><span data-stu-id="530d4-146">Value</span></span>       | <span data-ttu-id="530d4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="530d4-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="530d4-148">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="530d4-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="530d4-149">See notes.</span></span>  | <span data-ttu-id="530d4-150">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="530d4-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="530d4-151">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="530d4-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="530d4-152">See notes.</span></span>  | <span data-ttu-id="530d4-153">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="530d4-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="530d4-154">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="530d4-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="530d4-155">See notes.</span></span>  | <span data-ttu-id="530d4-156">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="530d4-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="530d4-157">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="530d4-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="530d4-158">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="530d4-159">**Suchfeld**</span><span class="sxs-lookup"><span data-stu-id="530d4-159">**ToolBar**</span></span> | <span data-ttu-id="530d4-160">Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="530d4-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="530d4-161">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="530d4-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="530d4-162">TRUE</span></span>        | <span data-ttu-id="530d4-163">Das Symbolleisten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="530d4-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="530d4-164">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="530d4-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="530d4-165">TRUE</span></span>        | <span data-ttu-id="530d4-166">Das Symbolleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="530d4-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="530d4-167">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="530d4-168">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="530d4-168">See notes.</span></span>  | <span data-ttu-id="530d4-169">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="530d4-170">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="530d4-171">NULL</span><span class="sxs-lookup"><span data-stu-id="530d4-171">NULL</span></span>        | <span data-ttu-id="530d4-172">Ein Symbolleisten-Steuerelement hat nie eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="530d4-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="530d4-173">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="530d4-174">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="530d4-174">See notes.</span></span>  | <span data-ttu-id="530d4-175">Lokalisierte Zeichenfolge für den Steuerelement-Typ der **Symbolleiste** .</span><span class="sxs-lookup"><span data-stu-id="530d4-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="530d4-176">Der Standardwert ist "Symbolleiste" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="530d4-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="530d4-177">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="530d4-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="530d4-178">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="530d4-178">Depends</span></span>     | <span data-ttu-id="530d4-179">Das Symbolleisten-Steuerelement benötigt keinen Namen, es sei denn, in einer Anwendung wird mehr als ein Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="530d4-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="530d4-180">Wenn mehr als ein Wert vorhanden ist, muss jeder über einen eindeutigen Namen verfügen (z. b. "Formatierung" oder "Gliederung").</span><span class="sxs-lookup"><span data-stu-id="530d4-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="530d4-181">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="530d4-181">Required Control Patterns</span></span>

<span data-ttu-id="530d4-182">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Toolbar-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="530d4-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="530d4-183">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="530d4-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="530d4-184">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="530d4-184">Control Pattern</span></span>                                                   | <span data-ttu-id="530d4-185">Support</span><span class="sxs-lookup"><span data-stu-id="530d4-185">Support</span></span> | <span data-ttu-id="530d4-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="530d4-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="530d4-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="530d4-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="530d4-188">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="530d4-188">Depends</span></span> | <span data-ttu-id="530d4-189">Wenn die Symbolleiste an verschiedenen Teilen des Bildschirms angedockt werden kann, muss Sie das [Dock](uiauto-implementingdock.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="530d4-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="530d4-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="530d4-191">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="530d4-191">Depends</span></span> | <span data-ttu-id="530d4-192">Wenn die Symbolleiste erweitert und reduziert werden kann, um weitere Elemente anzuzeigen, muss Sie das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="530d4-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="530d4-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="530d4-194">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="530d4-194">Depends</span></span> | <span data-ttu-id="530d4-195">Wenn die Größe der Symbolleiste geändert, gedreht oder verschoben werden kann, muss Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="530d4-196">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="530d4-196">Required Events</span></span>

<span data-ttu-id="530d4-197">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Symbolleisten-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="530d4-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="530d4-198">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="530d4-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="530d4-199">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="530d4-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="530d4-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="530d4-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="530d4-201">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="530d4-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="530d4-202">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="530d4-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="530d4-203">[**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="530d4-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="530d4-204">Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="530d4-205">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="530d4-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="530d4-206">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="530d4-207">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="530d4-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="530d4-208">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="530d4-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="530d4-209">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="530d4-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="530d4-210">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="530d4-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="530d4-211">**Licher**</span><span class="sxs-lookup"><span data-stu-id="530d4-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="530d4-212">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="530d4-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="530d4-213">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="530d4-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




