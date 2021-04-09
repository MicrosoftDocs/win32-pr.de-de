---
title: CheckBox-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den CheckBox-Steuerelement-Typ.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für CheckBox-Steuerelement Typen
- UI-Automatisierung, CheckBox-Steuerelement Typen
- UI-Automatisierung, Struktur für CheckBox-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für CheckBox-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für CheckBox-Steuerelement Typen
- UI-Automatisierung, Ereignisse für CheckBox-Steuerelement Typen
- Baumstrukturen, CheckBox-Steuerelement Typen
- Eigenschaften, CheckBox-Steuerelement Typen
- Steuerelement Muster, CheckBox-Steuerelement Typen
- Ereignisse, CheckBox-Steuerelement Typen
- Unterstützung für CheckBox-Steuerelement Typen
- CheckBox-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für CheckBox-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für CheckBox-Steuerelement Typen
- Steuerelement Typen, Unterstützung für CheckBox
- Steuerelement Typen, Kontrollkästchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856084"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="aaa22-119">CheckBox-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="aaa22-119">CheckBox Control Type</span></span>

<span data-ttu-id="aaa22-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **CheckBox** -Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="aaa22-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="aaa22-121">Ein Kontrollkästchen ist ein Objekt, mit dem ein Zustand gekennzeichnet wird und das Benutzer dazu verwenden können, diesen Zustand zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="aaa22-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="aaa22-122">Kontrollkästchen bieten dem Benutzer eine binäre Option [(Ja/Nein) oder (Ein/Aus)] oder eine tertiäre Option (Ein, Aus, Unbestimmt).</span><span class="sxs-lookup"><span data-stu-id="aaa22-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="aaa22-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **CheckBox** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="aaa22-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="aaa22-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Kontrollkästchen-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="aaa22-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="aaa22-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="aaa22-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aaa22-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="aaa22-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="aaa22-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aaa22-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="aaa22-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="aaa22-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="aaa22-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="aaa22-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="aaa22-130">DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="aaa22-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="aaa22-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aaa22-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="aaa22-132">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="aaa22-132">Typical Tree Structure</span></span>

<span data-ttu-id="aaa22-133">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Kontrollkästchen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aaa22-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="aaa22-134">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="aaa22-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aaa22-135">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="aaa22-135">Control View</span></span></th>
<th><span data-ttu-id="aaa22-136">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="aaa22-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="aaa22-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="aaa22-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="aaa22-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="aaa22-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="aaa22-139">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aaa22-139">Relevant Properties</span></span>

<span data-ttu-id="aaa22-140">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **CheckBox** -Steuerelement-Typ besonders relevant ist</span><span class="sxs-lookup"><span data-stu-id="aaa22-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="aaa22-141">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="aaa22-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="aaa22-142">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aaa22-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="aaa22-143">Wert</span><span class="sxs-lookup"><span data-stu-id="aaa22-143">Value</span></span>        | <span data-ttu-id="aaa22-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa22-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaa22-145">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="aaa22-146">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-146">See notes.</span></span>   | <span data-ttu-id="aaa22-147">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="aaa22-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="aaa22-148">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="aaa22-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-149">See notes.</span></span>   | <span data-ttu-id="aaa22-150">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa22-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="aaa22-151">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="aaa22-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-152">See notes.</span></span>   | <span data-ttu-id="aaa22-153">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="aaa22-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="aaa22-154">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aaa22-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="aaa22-155">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="aaa22-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="aaa22-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="aaa22-157">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aaa22-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="aaa22-158">TRUE</span></span>         | <span data-ttu-id="aaa22-159">Der Wert dieser Eigenschaft muss immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="aaa22-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="aaa22-160">Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="aaa22-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="aaa22-161">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aaa22-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="aaa22-162">TRUE</span></span>         | <span data-ttu-id="aaa22-163">Der Wert dieser Eigenschaft muss immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="aaa22-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="aaa22-164">Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="aaa22-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="aaa22-165">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="aaa22-166">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-166">See notes.</span></span>   | <span data-ttu-id="aaa22-167">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aaa22-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="aaa22-168">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="aaa22-169">Null</span><span class="sxs-lookup"><span data-stu-id="aaa22-169">Null</span></span>         | <span data-ttu-id="aaa22-170">Kontrollkästchen-Steuerelemente sind selbst beschriftet.</span><span class="sxs-lookup"><span data-stu-id="aaa22-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="aaa22-171">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="aaa22-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-172">See notes.</span></span>   | <span data-ttu-id="aaa22-173">Lokalisierte Zeichenfolge für den Steuerelement-Typ " **CheckBox** ".</span><span class="sxs-lookup"><span data-stu-id="aaa22-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="aaa22-174">Der Standardwert ist "Kontrollkästchen" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="aaa22-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="aaa22-175">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="aaa22-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="aaa22-176">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aaa22-176">See notes.</span></span>   | <span data-ttu-id="aaa22-177">Der Wert der [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (oder [**cachedname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname))-Eigenschaft des Kontrollkästchen-Steuer Elements ist der Text, der neben dem Feld angezeigt wird, das den UMSCHALT Zustand beibehält.</span><span class="sxs-lookup"><span data-stu-id="aaa22-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="aaa22-178">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="aaa22-178">Required Control Patterns</span></span>

<span data-ttu-id="aaa22-179">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Kontrollkästchen-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="aaa22-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="aaa22-180">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="aaa22-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="aaa22-181">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="aaa22-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="aaa22-182">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="aaa22-182">Support/Value</span></span> | <span data-ttu-id="aaa22-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa22-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaa22-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="aaa22-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="aaa22-185">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aaa22-185">Required</span></span>      | <span data-ttu-id="aaa22-186">Kontrollkästchen unterstützen das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster, damit das Kontrollkästchen Programm gesteuert durch den internen Zustand des Kontrollkästchens durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="aaa22-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="aaa22-187">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="aaa22-187">Required Events</span></span>

<span data-ttu-id="aaa22-188">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Kontrollkästchen-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="aaa22-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="aaa22-189">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="aaa22-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="aaa22-190">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="aaa22-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="aaa22-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa22-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaa22-192">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="aaa22-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="aaa22-193">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aaa22-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="aaa22-194">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aaa22-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="aaa22-195">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aaa22-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="aaa22-196">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aaa22-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="aaa22-197">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aaa22-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="aaa22-198">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="aaa22-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="aaa22-199">[**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aaa22-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="aaa22-200">DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="aaa22-200">DefaultAction</span></span>

<span data-ttu-id="aaa22-201">Die Standardaktion für ein Kontrollkästchen besteht darin, einem Optionsfeld den Fokus zu geben und dessen aktuellen Status umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="aaa22-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="aaa22-202">Wie bereits erwähnt, bieten Kontrollkästchen dem Benutzer eine binäre (Yes/No-oder on/off)-Entscheidung, oder eine tertiäre (ein-, ausschalten, unbestimmt).</span><span class="sxs-lookup"><span data-stu-id="aaa22-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="aaa22-203">Ist das Kontrollkästchen binär, bewirkt die Standardaktion, dass aus dem Zustand „Ein“ in den Zustand „Aus“ oder aus dem Zustand „Aus“ in den Zustand „Ein“ geschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="aaa22-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="aaa22-204">In einem tertiären Kontrollkästchen durchläuft die Standardaktion die Status des Kontrollkästchens in derselben Reihenfolge, in der der Benutzer aufeinander folgende Mausklicks an das Steuerelement gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="aaa22-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaa22-205">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aaa22-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aaa22-206">**Licher**</span><span class="sxs-lookup"><span data-stu-id="aaa22-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aaa22-207">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="aaa22-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="aaa22-208">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="aaa22-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




