---
title: Thumb-Steuerelement
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Steuerelement
- Benutzeroberflächenautomatisierungs-, Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Struktur für den Steuerelement-Steuerelement
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für Steuerelement-Steuerelement
- Struktur Strukturen, Typ des Thumb-Steuer Elements
- Eigenschaften, Typ des Thumb-Steuer Elements
- Steuerelement Muster, Typ des Thumb-Steuer Elements
- Ereignisse, Typ des Thumb-Steuer Elements
- Unterstützung für den Thumb-Steuerelement
- Thumb-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Thumb-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Thumb-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Thumb
- Steuerelement Typen, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388689"
---
# <a name="thumb-control-type"></a><span data-ttu-id="5e5a9-119">Thumb-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5e5a9-119">Thumb Control Type</span></span>

<span data-ttu-id="5e5a9-120">Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="5e5a9-121">Thumb-Steuerelemente bieten die Funktionen, mit denen ein Steuerelement bewegt (oder gezogen) werden kann, wie ein Schieberegler für Bildlaufleisten, oder in der Größe angepasst werden kann, wie ein Widget für die Größenanpassung von Fenstern.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="5e5a9-122">Beachten Sie, dass ein Thumb-Steuerelement keine Drag & Drop-Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="5e5a9-123">Thumb-Steuerelemente können den Maus Fokus, aber keinen Tastaturfokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="5e5a9-124">Der Entwickler von Steuerelementen muss das Steuerelement implementieren, damit es entsprechend funktioniert (d. h. es kann gezogen bzw. in der Größe angepasst werden).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="5e5a9-125">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse **für den Steuer** Element-Steuerelement Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="5e5a9-126">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Ziehpunkt-Steuerelemente, bei denen das UI-Framework/die Benutzeroberflächen Automatisierung für Steuerelement Typen und Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5e5a9-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5e5a9-127">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="5e5a9-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5e5a9-128">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="5e5a9-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5e5a9-129">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e5a9-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5e5a9-130">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="5e5a9-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5e5a9-131">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5e5a9-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5e5a9-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e5a9-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5e5a9-133">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="5e5a9-133">Typical Tree Structure</span></span>

<span data-ttu-id="5e5a9-134">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Thumb-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5e5a9-135">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e5a9-136">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="5e5a9-136">Control View</span></span></th>
<th><span data-ttu-id="5e5a9-137">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="5e5a9-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5e5a9-138">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="5e5a9-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="5e5a9-139">(Nicht vorhanden)</span><span class="sxs-lookup"><span data-stu-id="5e5a9-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5e5a9-140">Thumb-Steuerelemente werden nie in der Inhaltsansicht angezeigt, da Sie nur mit einer Maus bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="5e5a9-141">Sie werden über ein anderes Steuerelement Muster verfügbar gemacht, z. b. das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster oder das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster, das im Container des Thumb-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="5e5a9-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="5e5a9-142">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e5a9-142">Relevant Properties</span></span>

<span data-ttu-id="5e5a9-143">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Thumb-Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="5e5a9-144">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5e5a9-145">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5e5a9-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5e5a9-146">Wert</span><span class="sxs-lookup"><span data-stu-id="5e5a9-146">Value</span></span>      | <span data-ttu-id="5e5a9-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e5a9-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e5a9-148">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5e5a9-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-149">See notes.</span></span> | <span data-ttu-id="5e5a9-150">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="5e5a9-151">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5e5a9-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-152">See notes.</span></span> | <span data-ttu-id="5e5a9-153">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="5e5a9-154">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5e5a9-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-155">See notes.</span></span> | <span data-ttu-id="5e5a9-156">Ein Punkt innerhalb des sichtbaren Client Bereichs des Thumb-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="5e5a9-157">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5e5a9-158">**Thumb**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5e5a9-159">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5e5a9-160">false</span><span class="sxs-lookup"><span data-stu-id="5e5a9-160">FALSE</span></span>      | <span data-ttu-id="5e5a9-161">Das Thumb-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nie enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="5e5a9-162">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5e5a9-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="5e5a9-163">TRUE</span></span>       | <span data-ttu-id="5e5a9-164">Das Thumb-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="5e5a9-165">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5e5a9-166">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-166">See notes.</span></span> | <span data-ttu-id="5e5a9-167">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="5e5a9-168">Ein Thumb-Steuerelement kann den Fokus erhalten, wenn es als "Zieh Element"-Objekt für die Größenanpassung eines Fensters oder Bereichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="5e5a9-169">Ein Thumb-Steuerelement in einem Schieberegler oder einer Scrollleiste sollte niemals den Fokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="5e5a9-170">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5e5a9-171">NULL</span><span class="sxs-lookup"><span data-stu-id="5e5a9-171">NULL</span></span>       | <span data-ttu-id="5e5a9-172">Thumb-Steuerelemente haben niemals eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="5e5a9-173">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5e5a9-174">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-174">See notes.</span></span> | <span data-ttu-id="5e5a9-175">Lokalisierte Zeichenfolge, **die dem** Steuerelement-Steuerelement entspricht.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="5e5a9-176">Der Standardwert ist "Thumb" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="5e5a9-177">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5e5a9-178">NULL</span><span class="sxs-lookup"><span data-stu-id="5e5a9-178">NULL</span></span>       | <span data-ttu-id="5e5a9-179">Da das Thumb-Steuerelement in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht verfügbar ist, ist kein Name erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5e5a9-180">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="5e5a9-180">Required Control Patterns</span></span>

<span data-ttu-id="5e5a9-181">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Thumb-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="5e5a9-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="5e5a9-182">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="5e5a9-183">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="5e5a9-183">Control Pattern</span></span>                                         | <span data-ttu-id="5e5a9-184">Support</span><span class="sxs-lookup"><span data-stu-id="5e5a9-184">Support</span></span>  | <span data-ttu-id="5e5a9-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e5a9-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e5a9-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="5e5a9-187">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5e5a9-187">Required</span></span> | <span data-ttu-id="5e5a9-188">Ermöglicht, dass das Ziehpunkt-Steuerelement auf dem Bildschirm bewegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="5e5a9-189">Da das Thumb-Steuerelement in der Regel nicht geändert oder gedreht werden kann, unterstützt das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster hauptsächlich die [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) -Funktion</span><span class="sxs-lookup"><span data-stu-id="5e5a9-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="5e5a9-190">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5e5a9-190">Required Events</span></span>

<span data-ttu-id="5e5a9-191">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Thumb-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="5e5a9-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="5e5a9-192">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5e5a9-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5e5a9-193">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="5e5a9-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5e5a9-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e5a9-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e5a9-195">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5e5a9-196">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5e5a9-197">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5e5a9-198">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5e5a9-199">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5e5a9-200">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e5a9-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5e5a9-201">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5e5a9-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e5a9-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5e5a9-203">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5e5a9-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e5a9-204">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="5e5a9-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5e5a9-205">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="5e5a9-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




