---
title: Register Steuerungstyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Tab-Steuerelement-Typ.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Tab-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Struktur für Register Steuerungstyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für Register Steuerelement-Typ
- Struktur Strukturen, Registerkarten-Steuerelement Typen
- Eigenschaften, Register Steuerelement-Typ
- Steuerelement Muster, Register Steuerelement-Typ
- Ereignisse, Registerkarten-Steuerelement Typen
- Unterstützung für Tab-Steuerelement Typen
- Tabulator-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Register Steuerungstyp
- Steuerelement Typen, Steuerelement Muster für Registerkarten-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Registerkarte
- Steuerelement Typen, Registerkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947844"
---
# <a name="tab-control-type"></a><span data-ttu-id="ce9b5-119">Register Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="ce9b5-119">Tab Control Type</span></span>

<span data-ttu-id="ce9b5-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Tab** -Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="ce9b5-121">Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="ce9b5-122">Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="ce9b5-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Tab** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="ce9b5-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Registerkarten-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ce9b5-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ce9b5-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ce9b5-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ce9b5-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ce9b5-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce9b5-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ce9b5-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ce9b5-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ce9b5-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ce9b5-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ce9b5-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ce9b5-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ce9b5-131">Typical Tree Structure</span></span>

<span data-ttu-id="ce9b5-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Registerkarten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ce9b5-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b5-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce9b5-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ce9b5-134">Control View</span></span></th>
<th><span data-ttu-id="ce9b5-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ce9b5-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ce9b5-136">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ce9b5-136">Tab</span></span>
<ul>
<li><span data-ttu-id="ce9b5-137">TabItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="ce9b5-138">ScrollBar (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="ce9b5-139">Button (0 oder 2)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce9b5-140">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ce9b5-140">Tab</span></span>
<ul>
<li><span data-ttu-id="ce9b5-141">TabItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce9b5-142">Registerkarten-Steuerelemente verfügen über untergeordnete Benutzeroberflächenautomatisierungs-Elemente, die auf dem [TabItem](uiauto-supporttabitemcontroltype.md) -</span><span class="sxs-lookup"><span data-stu-id="ce9b5-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="ce9b5-143">Wenn Registerkarten Elemente gruppiert sind (z. b. wie in Microsoft Office Anwendungen), kann der **Register** Steuerelementtyp auch **Gruppen** Steuerelement Typen für die gruppierten Registerkarten Elemente hosten, wie in der folgenden Baumstruktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce9b5-144">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ce9b5-144">Control View</span></span></th>
<th><span data-ttu-id="ce9b5-145">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ce9b5-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ce9b5-146">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ce9b5-146">Tab</span></span>
<ul>
<li><span data-ttu-id="ce9b5-147">TabItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="ce9b5-148">Group (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="ce9b5-149">TabItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="ce9b5-150">ScrollBar (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="ce9b5-151">Button (0 oder 2)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce9b5-152">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ce9b5-152">Tab</span></span>
<ul>
<li><span data-ttu-id="ce9b5-153">TabItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="ce9b5-154">Group (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="ce9b5-155">TabItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="ce9b5-156">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce9b5-156">Relevant Properties</span></span>

<span data-ttu-id="ce9b5-157">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Register Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="ce9b5-158">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b5-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ce9b5-159">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce9b5-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ce9b5-160">Wert</span><span class="sxs-lookup"><span data-stu-id="ce9b5-160">Value</span></span>      | <span data-ttu-id="ce9b5-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce9b5-162">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ce9b5-163">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-163">See notes.</span></span> | <span data-ttu-id="ce9b5-164">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ce9b5-165">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ce9b5-166">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-166">See notes.</span></span> | <span data-ttu-id="ce9b5-167">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ce9b5-168">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ce9b5-169">Nein</span><span class="sxs-lookup"><span data-stu-id="ce9b5-169">No</span></span>         | <span data-ttu-id="ce9b5-170">Das Registerkarten-Steuerelement enthält keine durch Klicken aktivierbaren Punkte.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="ce9b5-171">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ce9b5-172">**TAB**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="ce9b5-173">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ce9b5-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce9b5-174">TRUE</span></span>       | <span data-ttu-id="ce9b5-175">Das Registerkarten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="ce9b5-176">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ce9b5-177">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce9b5-177">TRUE</span></span>       | <span data-ttu-id="ce9b5-178">Das Registerkarten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="ce9b5-179">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ce9b5-180">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce9b5-180">TRUE</span></span>       | <span data-ttu-id="ce9b5-181">Der Tab-Steuerelementtyp muss den Tastaturfokus empfangen können.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="ce9b5-182">In der Regel Ruft ein Benutzeroberflächenautomatisierungs-Client [**iuiautomationelement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) auf einem Registerkarten-Steuerelement auf, und eines seiner Elemente führt den Tastaturfokus an das Registerkarten-Steuerelement weiter.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="ce9b5-183">Bei einigen Registerkartencontainern ist es möglich, dass sie den Fokus annehmen, ohne dass der Fokus für eines ihrer Elemente festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="ce9b5-184">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ce9b5-185">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-185">See notes.</span></span> | <span data-ttu-id="ce9b5-186">Registerkarten-Steuerelemente haben üblicherweise eine statische Beschriftung, die durch diese Eigenschaft verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="ce9b5-187">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ce9b5-188">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-188">See notes.</span></span> | <span data-ttu-id="ce9b5-189">Lokalisierte Zeichenfolge, die dem **Register** Steuerungstyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="ce9b5-190">Der Standardwert ist "Tab" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="ce9b5-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ce9b5-191">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ce9b5-192">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-192">See notes.</span></span> | <span data-ttu-id="ce9b5-193">Das Registerkarten-Steuerelement erfordert selten eine **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="ce9b5-194">**UIA- \_ orientationpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ce9b5-195">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-195">See notes.</span></span> | <span data-ttu-id="ce9b5-196">Durch das Registerkarten-Steuerelement muss immer angeben werden, ob es horizontal oder vertikal positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ce9b5-197">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ce9b5-197">Required Control Patterns</span></span>

<span data-ttu-id="ce9b5-198">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Register Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="ce9b5-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="ce9b5-199">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b5-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ce9b5-200">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce9b5-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="ce9b5-201">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="ce9b5-201">Support/Value</span></span> | <span data-ttu-id="ce9b5-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce9b5-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="ce9b5-204">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ce9b5-204">Required</span></span>      | <span data-ttu-id="ce9b5-205">Alle Registerkarten-Steuerelemente müssen das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="ce9b5-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="ce9b5-207">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce9b5-207">TRUE</span></span>          | <span data-ttu-id="ce9b5-208">Ein Registerkarten-Steuerelement erfordert immer, dass eine Auswahl getroffen wird.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="ce9b5-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="ce9b5-210">false</span><span class="sxs-lookup"><span data-stu-id="ce9b5-210">FALSE</span></span>         | <span data-ttu-id="ce9b5-211">Registerkarten-Steuerelemente sind immer Einzelauswahlcontainer.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="ce9b5-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="ce9b5-213">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="ce9b5-213">Depends</span></span>       | <span data-ttu-id="ce9b5-214">Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster muss unterstützt werden, wenn das Registerkarten-Steuerelement Widgets enthält, mit denen ein Satz von Registerkarten Elementen durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ce9b5-215">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ce9b5-215">Required Events</span></span>

<span data-ttu-id="ce9b5-216">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Registerkarten-Steuerelemente zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ce9b5-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="ce9b5-217">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b5-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ce9b5-218">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="ce9b5-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="ce9b5-219">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce9b5-220">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="ce9b5-221">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="ce9b5-222">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="ce9b5-223">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ce9b5-224">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="ce9b5-225">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="ce9b5-226">[**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="ce9b5-227">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="ce9b5-228">[**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="ce9b5-229">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="ce9b5-230">[**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="ce9b5-231">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="ce9b5-232">[**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="ce9b5-233">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="ce9b5-234">[**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="ce9b5-235">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="ce9b5-236">[**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="ce9b5-237">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce9b5-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="ce9b5-238">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ce9b5-239">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce9b5-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ce9b5-240">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ce9b5-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce9b5-241">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ce9b5-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ce9b5-242">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ce9b5-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




