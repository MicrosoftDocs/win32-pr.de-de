---
title: StatusBar-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den StatusBar-Steuer Elementtyp.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, StatusBar-Steuer Elementtyp
- UI-Automatisierung, Struktur für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für StatusBar-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für StatusBar-Steuer Elementtyp
- Baumstrukturen, StatusBar-Steuer Elementtyp
- Eigenschaften, StatusBar-Steuer Elementtyp
- Steuerelement Muster, StatusBar-Steuer Elementtyp
- Ereignisse, StatusBar-Steuer Elementtyp
- Unterstützung für StatusBar-Steuer Elementtyp
- StatusBar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für StatusBar-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für StatusBar-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für StatusBar
- Steuerelement Typen, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310592"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="41f7b-119">StatusBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="41f7b-119">StatusBar Control Type</span></span>

<span data-ttu-id="41f7b-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **StatusBar** -Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="41f7b-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="41f7b-121">Ein StatusBar-Steuerelement zeigt Informationen zu einem Objekt an, das in einem Fenster einer Anwendung angezeigt wird, zur Komponente des Objekts oder Kontextinformationen, die sich auf die Operation dieses Objekts in Ihrer Anwendung beziehen.</span><span class="sxs-lookup"><span data-stu-id="41f7b-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="41f7b-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuer Elementtyp " **StatusBar** " definiert.</span><span class="sxs-lookup"><span data-stu-id="41f7b-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="41f7b-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle StatusBar-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="41f7b-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="41f7b-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="41f7b-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="41f7b-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="41f7b-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="41f7b-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41f7b-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="41f7b-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="41f7b-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="41f7b-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="41f7b-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="41f7b-129">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="41f7b-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="41f7b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f7b-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="41f7b-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="41f7b-131">Typical Tree Structure</span></span>

<span data-ttu-id="41f7b-132">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Status leisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="41f7b-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="41f7b-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41f7b-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41f7b-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="41f7b-134">Control View</span></span></th>
<th><span data-ttu-id="41f7b-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="41f7b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="41f7b-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="41f7b-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="41f7b-137">Bearbeiten (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="41f7b-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="41f7b-138">ProgressBar (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="41f7b-139">Bild (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="41f7b-140">Schaltfläche (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="41f7b-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="41f7b-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="41f7b-142">Bearbeiten (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="41f7b-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="41f7b-143">ProgressBar (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="41f7b-144">Bild (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="41f7b-145">Schaltfläche (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="41f7b-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="41f7b-146">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41f7b-146">Relevant Properties</span></span>

<span data-ttu-id="41f7b-147">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Status leisten-Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="41f7b-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="41f7b-148">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="41f7b-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="41f7b-149">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41f7b-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="41f7b-150">Wert</span><span class="sxs-lookup"><span data-stu-id="41f7b-150">Value</span></span>         | <span data-ttu-id="41f7b-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f7b-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41f7b-152">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="41f7b-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41f7b-153">See notes.</span></span>    | <span data-ttu-id="41f7b-154">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="41f7b-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="41f7b-155">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="41f7b-156">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41f7b-156">See notes.</span></span>    | <span data-ttu-id="41f7b-157">Das umschließende Rechteck einer Statusleiste muss alle darin enthaltenen Steuerelemente umfassen.</span><span class="sxs-lookup"><span data-stu-id="41f7b-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="41f7b-158">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="41f7b-159">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41f7b-159">See notes.</span></span>    | <span data-ttu-id="41f7b-160">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="41f7b-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="41f7b-161">Wenn Bereiche innerhalb des umgebenden Rechtecks vorhanden sind, die nicht klickbar sind, und das-Element spezialisierte Treffer Tests durchführt, überschreiben Sie diese, und stellen Sie einen klickbaren Punkt bereit.</span><span class="sxs-lookup"><span data-stu-id="41f7b-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="41f7b-162">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="41f7b-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="41f7b-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="41f7b-164">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="41f7b-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="41f7b-165">TRUE</span></span>          | <span data-ttu-id="41f7b-166">Das StatusBar-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="41f7b-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="41f7b-167">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="41f7b-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="41f7b-168">TRUE</span></span>          | <span data-ttu-id="41f7b-169">Das StatusBar-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="41f7b-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="41f7b-170">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="41f7b-171">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41f7b-171">Depends</span></span>       | <span data-ttu-id="41f7b-172">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41f7b-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="41f7b-173">**UIA \_ isoffscreenpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="41f7b-174">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41f7b-174">Depends</span></span>       | <span data-ttu-id="41f7b-175">Wenn ein StatusBar-Steuerelement momentan nicht sichtbar ist, wird für diese Eigenschaft der Wert true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41f7b-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="41f7b-176">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="41f7b-177">NULL</span><span class="sxs-lookup"><span data-stu-id="41f7b-177">NULL</span></span>          | <span data-ttu-id="41f7b-178">Das StatusBar-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="41f7b-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="41f7b-179">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="41f7b-180">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41f7b-180">See notes.</span></span>    | <span data-ttu-id="41f7b-181">Lokalisierte Zeichenfolge für den Steuer Elementtyp " **StatusBar** ".</span><span class="sxs-lookup"><span data-stu-id="41f7b-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="41f7b-182">Der Standardwert ist "Statusleiste" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="41f7b-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="41f7b-183">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="41f7b-184">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41f7b-184">See notes.</span></span>    | <span data-ttu-id="41f7b-185">Das StatusBar-Steuerelement muss nur dann einen Namen haben, wenn in einer Anwendung mehrere Statusleisten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f7b-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="41f7b-186">Unterscheiden Sie in diesem Fall die einzelnen Balken mit Namen wie "Internet Status" oder "Anwendungs Status".</span><span class="sxs-lookup"><span data-stu-id="41f7b-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="41f7b-187">**UIA- \_ orientationpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41f7b-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="41f7b-188">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41f7b-188">Depends</span></span>       | <span data-ttu-id="41f7b-189">Ein Wert, der die Ausrichtung des Steuer Elements angibt: horizontal oder vertikal.</span><span class="sxs-lookup"><span data-stu-id="41f7b-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="41f7b-190">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="41f7b-190">Required Control Patterns</span></span>

<span data-ttu-id="41f7b-191">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die für Status leisten-Steuerelemente unterstützt</span><span class="sxs-lookup"><span data-stu-id="41f7b-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="41f7b-192">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41f7b-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="41f7b-193">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="41f7b-193">Control Pattern</span></span>                               | <span data-ttu-id="41f7b-194">Support</span><span class="sxs-lookup"><span data-stu-id="41f7b-194">Support</span></span>  | <span data-ttu-id="41f7b-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f7b-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41f7b-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="41f7b-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="41f7b-197">Optional</span><span class="sxs-lookup"><span data-stu-id="41f7b-197">Optional</span></span> | <span data-ttu-id="41f7b-198">StatusBar-Steuerelemente sollten das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster unterstützen, damit einzelne Teile überwacht und leicht referenziert werden können.</span><span class="sxs-lookup"><span data-stu-id="41f7b-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="41f7b-199">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="41f7b-199">Required Events</span></span>

<span data-ttu-id="41f7b-200">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von StatusBar-</span><span class="sxs-lookup"><span data-stu-id="41f7b-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="41f7b-201">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41f7b-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="41f7b-202">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="41f7b-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="41f7b-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f7b-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="41f7b-204">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="41f7b-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="41f7b-205">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41f7b-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="41f7b-206">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41f7b-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="41f7b-207">Wenn das Steuerelement die **isaktivierte** Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41f7b-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="41f7b-208">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41f7b-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="41f7b-209">Wenn das Steuerelement die **IsOffscreen** -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41f7b-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="41f7b-210">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="41f7b-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="41f7b-211">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41f7b-211">Remarks</span></span>

<span data-ttu-id="41f7b-212">Es wird empfohlen, Bearbeitungs Steuerelemente als untergeordnete Raster Elemente in einer Statusleiste zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="41f7b-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="41f7b-213">Die Verwendung von Bearbeitungs Steuerelementen erleichtert das Zuordnen des Zwecks des Status Felds mit dem Wert, indem der Elementname und die Value-Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f7b-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="41f7b-214">Da Text Steuerelemente das **value** -Steuerelement Muster nicht unterstützen sollten, sollten Sie nicht als untergeordnete Raster Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f7b-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41f7b-215">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f7b-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="41f7b-216">**Licher**</span><span class="sxs-lookup"><span data-stu-id="41f7b-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="41f7b-217">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="41f7b-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="41f7b-218">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="41f7b-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




