---
title: Slider-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Schieberegler-Steuerelement Typen.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Schieberegler
- Benutzeroberflächenautomatisierungs-, Slider-Steuerelement
- Benutzeroberflächenautomatisierungs-Struktur für Schieberegler-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Slider-Steuerelement
- UI-Automatisierung, Steuerelement Muster für den Schieberegler-Steuerelement
- UI-Automatisierung, Ereignisse für den Schieberegler-Steuerelement
- Baumstrukturen, Schieberegler-Steuerelement Typen
- Eigenschaften, Schieberegler-Steuerelement Typen
- Steuerelement Muster, Schieberegler-Steuerelement Typen
- Ereignisse, Schieberegler-Steuerelement Typen
- Unterstützung für den Slider-Steuerelement
- Schiebereglersteuerungstyp
- Steuerelement Typen, Baumstruktur für den Schieberegler-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Schieberegler-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Schieberegler
- Steuerelement Typen, Schieberegler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947845"
---
# <a name="slider-control-type"></a><span data-ttu-id="51210-119">Slider-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="51210-119">Slider Control Type</span></span>

<span data-ttu-id="51210-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Schieberegler** -Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="51210-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="51210-121">Ein Schieberegler-Steuerelement ist ein zusammengesetztes Steuerelement mit Schaltflächen, mit denen ein Benutzer einen numerischen Bereich festlegen oder einen Satz von Elementen auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="51210-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="51210-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Schieberegler** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="51210-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="51210-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schieberegler-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="51210-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="51210-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="51210-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="51210-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="51210-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="51210-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51210-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="51210-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="51210-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="51210-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="51210-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="51210-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51210-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="51210-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="51210-130">Typical Tree Structure</span></span>

<span data-ttu-id="51210-131">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Schieberegler-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51210-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="51210-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51210-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51210-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="51210-133">Control View</span></span></th>
<th><span data-ttu-id="51210-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="51210-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="51210-135">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="51210-135">Slider</span></span>
<ul>
<li><span data-ttu-id="51210-136">Schaltfläche (2 oder 4)</span><span class="sxs-lookup"><span data-stu-id="51210-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="51210-137">Thumb (1)</span><span class="sxs-lookup"><span data-stu-id="51210-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="51210-138">Listenelement (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="51210-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="51210-139">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="51210-139">Slider</span></span>
<ul>
<li><span data-ttu-id="51210-140">Listenelement (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="51210-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="51210-141">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51210-141">Relevant Properties</span></span>

<span data-ttu-id="51210-142">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Schieberegler-Steuerelemente besonders relevant ist</span><span class="sxs-lookup"><span data-stu-id="51210-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="51210-143">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="51210-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="51210-144">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51210-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="51210-145">Wert</span><span class="sxs-lookup"><span data-stu-id="51210-145">Value</span></span>      | <span data-ttu-id="51210-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="51210-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51210-147">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="51210-148">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-148">See notes.</span></span> | <span data-ttu-id="51210-149">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="51210-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="51210-150">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="51210-151">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-151">See notes.</span></span> | <span data-ttu-id="51210-152">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="51210-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="51210-153">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="51210-154">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-154">See notes.</span></span> | <span data-ttu-id="51210-155">Die Mehrzahl der Schieberegler-Steuerelemente müssen den [**UIA \_ E \_ noclickablepoint**](uiauto-error-codes.md) -Fehler zurückgeben, da das gesamte umgebende Rechteck des Schieberegler-Steuer Elements durch untergeordnete Steuerelemente belegt wird.</span><span class="sxs-lookup"><span data-stu-id="51210-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="51210-156">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="51210-157">**Schieberegler**</span><span class="sxs-lookup"><span data-stu-id="51210-157">**Slider**</span></span> | <span data-ttu-id="51210-158">Dieser Wert ist für alle Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="51210-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="51210-159">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="51210-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="51210-160">TRUE</span></span>       | <span data-ttu-id="51210-161">Das Schieberegler-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="51210-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="51210-162">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="51210-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="51210-163">TRUE</span></span>       | <span data-ttu-id="51210-164">Das Schieberegler-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="51210-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="51210-165">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="51210-166">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-166">See notes.</span></span> | <span data-ttu-id="51210-167">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="51210-168">Die untergeordneten Elemente (Schaltflächen und Thumb) eines Schieberegler-Steuer Elements sollten niemals den Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="51210-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="51210-169">Der Fokus sollte immer auf dem Schieberegler-Steuerelement selbst bleiben.</span><span class="sxs-lookup"><span data-stu-id="51210-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="51210-170">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="51210-171">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-171">See notes.</span></span> | <span data-ttu-id="51210-172">Wenn dem Steuerelement eine statische Text Bezeichnung zugeordnet ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="51210-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="51210-173">Wenn das Text Steuerelement eine Unterkomponente eines anderen Steuer Elements ist, wird keine **LabeledBy** -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51210-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="51210-174">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="51210-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-175">See notes.</span></span> | <span data-ttu-id="51210-176">Lokalisierte Zeichenfolge für den Steuerungstyp des **Schiebereglers** .</span><span class="sxs-lookup"><span data-stu-id="51210-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="51210-177">Der Standardwert ist "Slider" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="51210-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="51210-178">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="51210-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="51210-179">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="51210-179">See notes.</span></span> | <span data-ttu-id="51210-180">Der Name des Schieberegler-Steuer Elements wird in der Regel aus einer statischen Text Bezeichnung generiert.</span><span class="sxs-lookup"><span data-stu-id="51210-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="51210-181">Wenn keine statische Text Bezeichnung vorhanden ist, muss der Anwendungsentwickler einen Eigenschafts Wert für den **Namen** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="51210-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="51210-182">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="51210-182">Required Control Patterns</span></span>

<span data-ttu-id="51210-183">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von allen Slider-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="51210-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="51210-184">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51210-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="51210-185">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="51210-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="51210-186">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="51210-186">Support/Value</span></span> | <span data-ttu-id="51210-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="51210-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51210-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="51210-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="51210-189">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="51210-189">Depends</span></span>       | <span data-ttu-id="51210-190">Ein Schieberegler muss das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützen, wenn der Inhalt auf einen Wert in einem numerischen Bereich festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="51210-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="51210-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="51210-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="51210-192">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="51210-192">Depends</span></span>       | <span data-ttu-id="51210-193">Ein Schieberegler sollte das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen, wenn der Inhalt einen Wert unter einem diskreten Satz von Optionen darstellt.</span><span class="sxs-lookup"><span data-stu-id="51210-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="51210-194">Wenn das Selection-Steuerelementmuster unterstützt wird, muss die entsprechende Auswahl als ein oder mehrere untergeordnete Listenelemente des Schiebereglers verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="51210-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="51210-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="51210-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="51210-196">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="51210-196">Depends</span></span>       | <span data-ttu-id="51210-197">Ein Schieberegler muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen, wenn der Inhalt einen Wert unter einem diskreten Satz von Optionen darstellt.</span><span class="sxs-lookup"><span data-stu-id="51210-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="51210-198">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="51210-198">Required Events</span></span>

<span data-ttu-id="51210-199">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Schieberegler-Steuerelemente zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="51210-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="51210-200">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51210-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="51210-201">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="51210-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="51210-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="51210-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51210-203">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="51210-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="51210-204">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51210-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="51210-205">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51210-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="51210-206">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="51210-207">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51210-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="51210-208">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="51210-209">[**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51210-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="51210-210">Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="51210-211">**UIA- \_ Auswahl \_ invalidatedeventid**</span><span class="sxs-lookup"><span data-stu-id="51210-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="51210-212">Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="51210-213">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="51210-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="51210-214">[**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51210-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="51210-215">Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51210-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="51210-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51210-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51210-217">**Licher**</span><span class="sxs-lookup"><span data-stu-id="51210-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51210-218">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="51210-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="51210-219">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="51210-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




