---
title: Hyperlink-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Link Steuerelement-Typ.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Hyperlink-Steuerelement Typen
- UI-Automatisierung, Struktur für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Hyperlink-Steuerelement Typen
- Struktur Strukturen, Hyperlink-Steuerelement Typen
- Eigenschaften, Hyperlink-Steuerelement Typen
- Steuerelement Muster, Hyperlink-Steuerelement Typen
- Ereignisse, Hyperlink-Steuerelement Typen
- Unterstützung für Hyperlink-Steuerelement Typen
- HyperLink-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Hyperlink-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Hyperlink-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Hyperlink
- Steuerelement Typen, Hyperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710313"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="22a0b-119">Hyperlink-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="22a0b-119">Hyperlink Control Type</span></span>

<span data-ttu-id="22a0b-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Link** Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="22a0b-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="22a0b-121">Hyperlink-Steuerelemente erstellen Links, die es Benutzern ermöglichen, innerhalb derselben Seite oder von einer Seite zu einer anderen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="22a0b-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="22a0b-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Link** Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="22a0b-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="22a0b-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Link Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="22a0b-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="22a0b-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="22a0b-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="22a0b-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="22a0b-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="22a0b-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a0b-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="22a0b-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22a0b-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="22a0b-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="22a0b-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="22a0b-129">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="22a0b-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="22a0b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22a0b-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="22a0b-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="22a0b-131">Typical Tree Structure</span></span>

<span data-ttu-id="22a0b-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Link Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a0b-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="22a0b-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="22a0b-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22a0b-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="22a0b-134">Control View</span></span></th>
<th><span data-ttu-id="22a0b-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="22a0b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="22a0b-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="22a0b-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="22a0b-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="22a0b-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="22a0b-138">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a0b-138">Relevant Properties</span></span>

<span data-ttu-id="22a0b-139">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Link Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="22a0b-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="22a0b-140">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="22a0b-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="22a0b-141">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22a0b-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="22a0b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="22a0b-142">Value</span></span>         | <span data-ttu-id="22a0b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="22a0b-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a0b-144">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="22a0b-145">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-145">See notes.</span></span>    | <span data-ttu-id="22a0b-146">Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="22a0b-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="22a0b-147">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="22a0b-148">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-148">See notes.</span></span>    | <span data-ttu-id="22a0b-149">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="22a0b-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="22a0b-150">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="22a0b-151">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-151">See notes.</span></span>    | <span data-ttu-id="22a0b-152">Der durch Klicken aktivierbare Punkt des Link Steuer Elements muss ein Punkt sein, der den Hyperlink öffnet, wenn mit einem Mauszeiger darauf geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="22a0b-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="22a0b-153">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="22a0b-154">**Link**</span><span class="sxs-lookup"><span data-stu-id="22a0b-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="22a0b-155">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="22a0b-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="22a0b-156">TRUE</span></span>          | <span data-ttu-id="22a0b-157">Das Link Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="22a0b-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="22a0b-158">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="22a0b-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="22a0b-159">TRUE</span></span>          | <span data-ttu-id="22a0b-160">Das Link Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="22a0b-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="22a0b-161">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="22a0b-162">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-162">See notes.</span></span>    | <span data-ttu-id="22a0b-163">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="22a0b-164">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="22a0b-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-165">See notes.</span></span>    | <span data-ttu-id="22a0b-166">Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="22a0b-167">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="22a0b-168">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-168">See notes.</span></span>    | <span data-ttu-id="22a0b-169">Lokalisierte Zeichenfolge für den Steuerelement Typ " **Hyperlink** ".</span><span class="sxs-lookup"><span data-stu-id="22a0b-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="22a0b-170">Der Standardwert ist "Hyperlink" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="22a0b-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="22a0b-171">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="22a0b-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="22a0b-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22a0b-172">See notes.</span></span>    | <span data-ttu-id="22a0b-173">Der Name des Link Steuer Elements ist der Text, der auf dem Bildschirm unterstrichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="22a0b-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="22a0b-174">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22a0b-174">Required Control Patterns</span></span>

<span data-ttu-id="22a0b-175">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die für die Unterstützung von Link-</span><span class="sxs-lookup"><span data-stu-id="22a0b-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="22a0b-176">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="22a0b-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="22a0b-177">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="22a0b-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="22a0b-178">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="22a0b-178">Support/Value</span></span>                | <span data-ttu-id="22a0b-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="22a0b-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a0b-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="22a0b-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="22a0b-181">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="22a0b-181">Required</span></span>                     | <span data-ttu-id="22a0b-182">Alle Link Steuerelemente müssen das Steuerelement Muster " [aufrufen](uiauto-implementinginvoke.md) " unterstützen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="22a0b-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="22a0b-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="22a0b-184">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="22a0b-184">Depends</span></span>                      | <span data-ttu-id="22a0b-185">Link Steuerelemente sollten das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen, wenn der Link Informationen enthält, die für den Benutzer verwendbar und aussagekräftig sind.</span><span class="sxs-lookup"><span data-stu-id="22a0b-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="22a0b-186">**Wert**</span><span class="sxs-lookup"><span data-stu-id="22a0b-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="22a0b-187">Beispiel: „https://www..“.</span><span class="sxs-lookup"><span data-stu-id="22a0b-187">For example, "https://www..."</span></span> | <span data-ttu-id="22a0b-188">Eine URL für eine Internet-oder Intranetadresse ist ein Beispiel für einen Hyperlink, der Informationen enthält, die für den Benutzer von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="22a0b-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="22a0b-189">Ein Programm gesteuerter Link ist jedoch nur für eine Anwendung sinnvoll und wird für die **value** -Eigenschaft nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="22a0b-190">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="22a0b-190">Required Events</span></span>

<span data-ttu-id="22a0b-191">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Link Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="22a0b-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="22a0b-192">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="22a0b-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="22a0b-193">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="22a0b-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="22a0b-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="22a0b-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a0b-195">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="22a0b-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="22a0b-196">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22a0b-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="22a0b-197">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="22a0b-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="22a0b-198">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22a0b-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="22a0b-199">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="22a0b-200">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22a0b-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="22a0b-201">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="22a0b-202">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="22a0b-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="22a0b-203">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22a0b-203">Remarks</span></span>

<span data-ttu-id="22a0b-204">Der Typ des Hyperlink-Steuer Elements sollte nur auf ein Objekt angewendet werden, das beim Klicken auf die Navigation bewirkt. Er sollte nicht auf den Container des Links angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a0b-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="22a0b-205">Beispielsweise sollten nur die durch Klicken aktivierbaren "Hotspots" innerhalb einer ImageMap den **Hyperlink** -Steuer Elementtyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="22a0b-206">Das gleiche gilt für Hyperlinks in einem Textfeld oder Dokument Container.</span><span class="sxs-lookup"><span data-stu-id="22a0b-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="22a0b-207">In diesem Fall sollte nur der Hyperlink-Text oder das Bild den **Hyperlink** -Steuer ungstyp haben, nicht den Container.</span><span class="sxs-lookup"><span data-stu-id="22a0b-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="22a0b-208">Das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster ist ideal für die Unterstützung eingebetteter Hyperlinks in Text-oder Dokument Elementen.</span><span class="sxs-lookup"><span data-stu-id="22a0b-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22a0b-209">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22a0b-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22a0b-210">**Licher**</span><span class="sxs-lookup"><span data-stu-id="22a0b-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22a0b-211">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="22a0b-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="22a0b-212">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="22a0b-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




