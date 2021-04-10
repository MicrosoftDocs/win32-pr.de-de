---
title: TitleBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den TitleBar-Steuerelement-Typ. Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungs Leiste in einem Fenster dar.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement (Titlebar)
- UI-Automatisierung, Struktur für TitleBar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement Muster für TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für TitleBar-Steuerelement Typen
- Baumstrukturen, TitleBar-Steuerelement Typen
- Eigenschaften, TitleBar-Steuerelement Typen
- Steuerelement Muster, TitleBar-Steuerelement Typen
- Ereignisse, TitleBar-Steuerelement Typen
- Unterstützung für TitleBar-Steuerelement Typen
- TitleBar-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für TitleBar-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für TitleBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Titlebar
- Steuerelement Typen, Titlebar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948044"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="57739-120">TitleBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="57739-120">TitleBar Control Type</span></span>

<span data-ttu-id="57739-121">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **TitleBar** -Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="57739-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="57739-122">Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungs Leiste in einem Fenster dar.</span><span class="sxs-lookup"><span data-stu-id="57739-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="57739-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **TitleBar** -Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="57739-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="57739-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Titelleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="57739-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="57739-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="57739-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="57739-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="57739-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="57739-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57739-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="57739-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="57739-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="57739-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="57739-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="57739-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57739-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="57739-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="57739-131">Typical Tree Structure</span></span>

<span data-ttu-id="57739-132">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Titelleisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57739-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="57739-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="57739-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57739-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="57739-134">Control View</span></span></th>
<th><span data-ttu-id="57739-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="57739-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="57739-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="57739-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="57739-137">Menü (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="57739-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="57739-138">Schaltfläche (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="57739-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="57739-139">(Nicht zutreffend; das Titelleisten-Steuerelement hat keinen Inhalt)</span><span class="sxs-lookup"><span data-stu-id="57739-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="57739-140">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57739-140">Relevant Properties</span></span>

<span data-ttu-id="57739-141">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **TitleBar** -Steuerelement Typ besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="57739-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="57739-142">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="57739-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="57739-143">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57739-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="57739-144">Wert</span><span class="sxs-lookup"><span data-stu-id="57739-144">Value</span></span>        | <span data-ttu-id="57739-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="57739-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57739-146">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="57739-147">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="57739-147">See notes.</span></span>   | <span data-ttu-id="57739-148">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="57739-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="57739-149">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="57739-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="57739-150">See notes.</span></span>   | <span data-ttu-id="57739-151">Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.</span><span class="sxs-lookup"><span data-stu-id="57739-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="57739-152">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="57739-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="57739-153">See notes.</span></span>   | <span data-ttu-id="57739-154">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="57739-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="57739-155">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="57739-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="57739-156">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="57739-157">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="57739-157">**TitleBar**</span></span> | <span data-ttu-id="57739-158">Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="57739-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="57739-159">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="57739-160">false</span><span class="sxs-lookup"><span data-stu-id="57739-160">FALSE</span></span>        | <span data-ttu-id="57739-161">Das Titelleisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nie enthalten.</span><span class="sxs-lookup"><span data-stu-id="57739-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="57739-162">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="57739-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="57739-163">TRUE</span></span>         | <span data-ttu-id="57739-164">Das Titelleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="57739-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="57739-165">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="57739-166">false</span><span class="sxs-lookup"><span data-stu-id="57739-166">FALSE</span></span>        | <span data-ttu-id="57739-167">Ein Titelleisten-Steuerelement hat nie den Tastaturfokus.</span><span class="sxs-lookup"><span data-stu-id="57739-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="57739-168">**UIA \_ isoffscreenpropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="57739-169">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="57739-169">Depends</span></span>      | <span data-ttu-id="57739-170">Ein Titelleisten-Steuerelement gibt einen Wert zurück, abhängig davon, ob es auf dem Bildschirm sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="57739-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="57739-171">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="57739-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="57739-172">See notes.</span></span>   | <span data-ttu-id="57739-173">Ein Titelleisten-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="57739-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="57739-174">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="57739-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="57739-175">See notes.</span></span>   | <span data-ttu-id="57739-176">Lokalisierte Zeichenfolge für den Steuerelementtyp „TitleBar“.</span><span class="sxs-lookup"><span data-stu-id="57739-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="57739-177">Der Standardwert ist "Titelleiste" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="57739-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="57739-178">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="57739-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="57739-179">""</span><span class="sxs-lookup"><span data-stu-id="57739-179">""</span></span>           | <span data-ttu-id="57739-180">Eine Titelleiste ist kein Inhalt. die Textinformationen werden durch den Namen des übergeordneten Fensters verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="57739-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="57739-181">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="57739-181">Required Control Patterns</span></span>

<span data-ttu-id="57739-182">Der **TitleBar** -Steuerelement-Typ ist nicht erforderlich, um Steuerelement Muster zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57739-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="57739-183">Seine Funktionalität wird über das [Window](uiauto-implementingwindow.md) -Steuerelement Muster des [Window](uiauto-supportwindowcontroltype.md) -Steuerelement Typs verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="57739-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="57739-184">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="57739-184">Required Events</span></span>

<span data-ttu-id="57739-185">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Steuerelementen für die</span><span class="sxs-lookup"><span data-stu-id="57739-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="57739-186">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="57739-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="57739-187">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="57739-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="57739-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="57739-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57739-189">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="57739-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="57739-190">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="57739-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="57739-191">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="57739-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="57739-192">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57739-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="57739-193">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="57739-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="57739-194">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57739-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="57739-195">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="57739-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="57739-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57739-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57739-197">**Licher**</span><span class="sxs-lookup"><span data-stu-id="57739-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57739-198">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="57739-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="57739-199">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="57739-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




