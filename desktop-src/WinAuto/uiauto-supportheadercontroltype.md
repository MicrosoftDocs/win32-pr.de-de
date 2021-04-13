---
title: Header Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Header-Steuerelement Typen.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Header-Steuerelement
- Benutzeroberflächenautomatisierungs, Header Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für den Header-Steuerelement Typen
- Benutzeroberflächen Automatisierung, Eigenschaften für den Header-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Header Steuerelement Typen
- UI-Automatisierung, Ereignisse für den Header-Steuerelement Typen
- Struktur Strukturen, Header Steuerelement-Typ
- Eigenschaften, Header-Steuerelement Typen
- Steuerelement Muster, Header Steuerelement-Typ
- Ereignisse, Header-Steuerelement Typen
- Unterstützung für den Header Steuerungstyp
- Header-Seuerelementtyp
- Steuerelement Typen, Baumstruktur für Header Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Header Steuerungstyp
- Steuerelement Typen, Unterstützung für Header
- Steuerelement Typen, Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388244"
---
# <a name="header-control-type"></a><span data-ttu-id="8969c-119">Header Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="8969c-119">Header Control Type</span></span>

<span data-ttu-id="8969c-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Header** -Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="8969c-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="8969c-121">Ein Headersteuerelement stellt einen visuellen Container für Beschriftungen von Zeilen oder Spalten bereit, die Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8969c-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="8969c-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Header** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="8969c-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="8969c-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Header Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und</span><span class="sxs-lookup"><span data-stu-id="8969c-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="8969c-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="8969c-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8969c-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="8969c-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="8969c-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8969c-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="8969c-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="8969c-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="8969c-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8969c-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="8969c-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8969c-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="8969c-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="8969c-130">Typical Tree Structure</span></span>

<span data-ttu-id="8969c-131">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Header Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8969c-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="8969c-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8969c-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8969c-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="8969c-133">Control View</span></span></th>
<th><span data-ttu-id="8969c-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="8969c-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8969c-135">Header</span><span class="sxs-lookup"><span data-stu-id="8969c-135">Header</span></span>
<ul>
<li><span data-ttu-id="8969c-136">HeaderItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="8969c-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="8969c-137">(Nicht vorhanden)</span><span class="sxs-lookup"><span data-stu-id="8969c-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8969c-138">Header Steuerelemente haben immer mindestens ein untergeordnetes Element in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8969c-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="8969c-139">Header Steuerelemente haben in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="8969c-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="8969c-140">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8969c-140">Relevant Properties</span></span>

<span data-ttu-id="8969c-141">In der folgenden Tabelle werden die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Werte oder Definitionen für Header Steuerelemente besonders relevant sind.</span><span class="sxs-lookup"><span data-stu-id="8969c-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="8969c-142">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="8969c-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="8969c-143">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8969c-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="8969c-144">Wert</span><span class="sxs-lookup"><span data-stu-id="8969c-144">Value</span></span>                                                            | <span data-ttu-id="8969c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8969c-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8969c-146">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="8969c-147">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-147">See notes.</span></span>                                                       | <span data-ttu-id="8969c-148">Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8969c-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="8969c-149">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="8969c-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-150">See notes.</span></span>                                                       | <span data-ttu-id="8969c-151">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="8969c-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="8969c-152">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="8969c-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-153">See notes.</span></span>                                                       | <span data-ttu-id="8969c-154">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="8969c-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="8969c-155">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8969c-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="8969c-156">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="8969c-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="8969c-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="8969c-158">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8969c-159">false</span><span class="sxs-lookup"><span data-stu-id="8969c-159">FALSE</span></span>                                                            | <span data-ttu-id="8969c-160">Das Header Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="8969c-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="8969c-161">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8969c-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="8969c-162">TRUE</span></span>                                                             | <span data-ttu-id="8969c-163">Das Header Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="8969c-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="8969c-164">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="8969c-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-165">See notes.</span></span>                                                       | <span data-ttu-id="8969c-166">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8969c-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="8969c-167">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="8969c-168">NULL</span><span class="sxs-lookup"><span data-stu-id="8969c-168">NULL</span></span>                                                             | <span data-ttu-id="8969c-169">Headersteuerelemente haben keine statische Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="8969c-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="8969c-170">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="8969c-171">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-171">See notes.</span></span>                                                       | <span data-ttu-id="8969c-172">Der Standardwert ist "Header" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="8969c-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="8969c-173">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="8969c-174">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8969c-174">See notes.</span></span>                                                       | <span data-ttu-id="8969c-175">Das Headersteuerelement benötigt einen Namen, wenn mehrere Zeilen- oder Spaltenüberschriften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8969c-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="8969c-176">Dadurch werden die Informationen für den Header (Überschrift) gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8969c-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="8969c-177">**UIA- \_ orientationpropertyid**</span><span class="sxs-lookup"><span data-stu-id="8969c-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="8969c-178">**OrientationType \_ Horizontal** oder **OrientationType \_ vertikal**</span><span class="sxs-lookup"><span data-stu-id="8969c-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="8969c-179">Der Wert dieser Eigenschaft macht die Position des Header Steuer Elements verfügbar – ob es sich um einen Zeilen Header (**OrientationType \_ Horizontal**) oder einen Spaltenheader (**OrientationType \_ vertikal**) handelt.</span><span class="sxs-lookup"><span data-stu-id="8969c-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="8969c-180">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="8969c-180">Required Control Patterns</span></span>

<span data-ttu-id="8969c-181">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die für Header Steuerelemente unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="8969c-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="8969c-182">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8969c-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="8969c-183">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="8969c-183">Control Pattern</span></span>                                         | <span data-ttu-id="8969c-184">Support</span><span class="sxs-lookup"><span data-stu-id="8969c-184">Support</span></span> | <span data-ttu-id="8969c-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="8969c-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8969c-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="8969c-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="8969c-187">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="8969c-187">Depends</span></span> | <span data-ttu-id="8969c-188">Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn die Größe des Header Steuer Elements geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8969c-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="8969c-189">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8969c-189">Required Events</span></span>

<span data-ttu-id="8969c-190">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Header Steuerelementen unterstützt werden müssen</span><span class="sxs-lookup"><span data-stu-id="8969c-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="8969c-191">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8969c-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="8969c-192">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="8969c-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="8969c-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="8969c-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8969c-194">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="8969c-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="8969c-195">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8969c-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="8969c-196">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8969c-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="8969c-197">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8969c-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="8969c-198">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8969c-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="8969c-199">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8969c-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="8969c-200">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="8969c-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="8969c-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8969c-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8969c-202">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8969c-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8969c-203">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="8969c-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="8969c-204">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="8969c-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




