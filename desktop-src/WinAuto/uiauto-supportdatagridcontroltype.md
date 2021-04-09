---
title: DataGrid-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den DataGrid-Steuerelement Typen.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung des DataGrid-Steuerelement Typs
- UI-Automatisierung, DataGrid-Steuerelement Typen
- UI-Automatisierung, Baumstruktur für DataGrid-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den DataGrid-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für DataGrid-Steuerelement Typen
- UI-Automatisierung, Ereignisse für den DataGrid-Steuerelement Typen
- Struktur Strukturen, DataGrid-Steuerelement Typen
- Eigenschaften, DataGrid-Steuerelement Typen
- Steuerelement Muster, DataGrid-Steuerelement Typen
- Ereignisse, DataGrid-Steuerelement Typen
- Unterstützung des DataGrid-Steuerelement Typs
- DataGrid-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für DataGrid-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den DataGrid-Steuerelement Typen
- Steuerelement Typen, Unterstützung für DataGrid
- Steuerelement Typen, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947651"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="55ef2-119">DataGrid-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="55ef2-119">DataGrid Control Type</span></span>

<span data-ttu-id="55ef2-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **DataGrid-** Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="55ef2-121">Mit dem **DataGrid-** Steuer Elementtyp kann ein Benutzer problemlos mit Elementen arbeiten, die in Spalten oder Zeilen dargestellten Daten-oder Automatisierungselemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="55ef2-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="55ef2-122">Datenraster-Steuerelemente enthalten Zeilen mit Elementen und Spalten mit Informationen über diese Elemente.</span><span class="sxs-lookup"><span data-stu-id="55ef2-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="55ef2-123">Ein Listenansicht-Steuerelement in Windows Vista Explorer ist ein Beispiel, das den **DataGrid-** Steuerelement Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55ef2-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="55ef2-124">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **DataGrid-** Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="55ef2-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="55ef2-125">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Datenraster-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="55ef2-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="55ef2-126">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="55ef2-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="55ef2-127">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="55ef2-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="55ef2-128">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55ef2-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="55ef2-129">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="55ef2-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="55ef2-130">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="55ef2-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="55ef2-131">Beispiel für den DataGrid-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="55ef2-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="55ef2-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55ef2-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="55ef2-133">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="55ef2-133">Typical Tree Structure</span></span>

<span data-ttu-id="55ef2-134">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Datenraster-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="55ef2-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="55ef2-135">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55ef2-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55ef2-136">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="55ef2-136">Control View</span></span></th>
<th><span data-ttu-id="55ef2-137">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="55ef2-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="55ef2-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="55ef2-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="55ef2-139">Header (0, 1 oder 2)</span><span class="sxs-lookup"><span data-stu-id="55ef2-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="55ef2-140">HeaderItem (Anzahl von Spalten oder Zeilen)</span><span class="sxs-lookup"><span data-stu-id="55ef2-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="55ef2-141">DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</span><span class="sxs-lookup"><span data-stu-id="55ef2-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55ef2-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="55ef2-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="55ef2-143">DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</span><span class="sxs-lookup"><span data-stu-id="55ef2-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="55ef2-144">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55ef2-144">Relevant Properties</span></span>

<span data-ttu-id="55ef2-145">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **DataGrid-** Steuerelement-Typ besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="55ef2-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="55ef2-146">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="55ef2-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="55ef2-147">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ef2-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="55ef2-148">Wert</span><span class="sxs-lookup"><span data-stu-id="55ef2-148">Value</span></span>        | <span data-ttu-id="55ef2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="55ef2-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55ef2-150">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="55ef2-151">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-151">See notes.</span></span>   | <span data-ttu-id="55ef2-152">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="55ef2-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="55ef2-153">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="55ef2-154">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-154">See notes.</span></span>   | <span data-ttu-id="55ef2-155">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="55ef2-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="55ef2-156">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="55ef2-157">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-157">See notes.</span></span>   | <span data-ttu-id="55ef2-158">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="55ef2-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="55ef2-159">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="55ef2-160">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="55ef2-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="55ef2-162">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55ef2-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="55ef2-163">TRUE</span></span>         | <span data-ttu-id="55ef2-164">Der Wert dieser Eigenschaft muss immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="55ef2-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="55ef2-165">Dies bedeutet, dass das Datenraster-Steuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur vorliegen muss.</span><span class="sxs-lookup"><span data-stu-id="55ef2-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="55ef2-166">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55ef2-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="55ef2-167">TRUE</span></span>         | <span data-ttu-id="55ef2-168">Der Wert dieser Eigenschaft muss immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="55ef2-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="55ef2-169">Dies bedeutet, dass das Datenraster-Steuerelement immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="55ef2-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="55ef2-170">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="55ef2-171">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-171">See notes.</span></span>   | <span data-ttu-id="55ef2-172">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="55ef2-173">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="55ef2-174">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-174">See notes.</span></span>   | <span data-ttu-id="55ef2-175">Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="55ef2-176">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="55ef2-177">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-177">See notes.</span></span>   | <span data-ttu-id="55ef2-178">Lokalisierte Zeichenfolge, die dem **DataGrid-** Steuerelement Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="55ef2-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="55ef2-179">Der Standardwert ist "Data Grid" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="55ef2-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="55ef2-180">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="55ef2-181">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55ef2-181">See notes.</span></span>   | <span data-ttu-id="55ef2-182">Das Datenraster-Steuerelement ruft in der Regel den Wert für seine **Name** -Eigenschaft aus einer statischen Text Bezeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="55ef2-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="55ef2-183">Wenn keine statische Text Bezeichnung vorhanden ist, muss ein Anwendungsentwickler einen Wert für die **Name** -Eigenschaft zuweisen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="55ef2-184">Der Wert der **Name** -Eigenschaft darf nie der Text Inhalt des Bearbeitungs Steuer Elements sein.</span><span class="sxs-lookup"><span data-stu-id="55ef2-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="55ef2-185">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="55ef2-185">Required Control Patterns</span></span>

<span data-ttu-id="55ef2-186">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Datenraster Steuerelementen unterstützt werden müssen</span><span class="sxs-lookup"><span data-stu-id="55ef2-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="55ef2-187">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55ef2-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="55ef2-188">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="55ef2-188">Control Pattern</span></span>                                         | <span data-ttu-id="55ef2-189">Support</span><span class="sxs-lookup"><span data-stu-id="55ef2-189">Support</span></span>  | <span data-ttu-id="55ef2-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="55ef2-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55ef2-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="55ef2-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="55ef2-192">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="55ef2-192">Required</span></span> | <span data-ttu-id="55ef2-193">Das Datenraster-Steuerelement selbst unterstützt immer das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster, da die darin enthaltenen Elemente über Metadaten verfügen, die in einem Raster angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55ef2-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="55ef2-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="55ef2-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="55ef2-195">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="55ef2-195">Depends</span></span>  | <span data-ttu-id="55ef2-196">Die Möglichkeit, im Datenraster zu scrollen, hängt vom Inhalt und davon ab, ob Scrollleisten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="55ef2-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="55ef2-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="55ef2-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="55ef2-198">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="55ef2-198">Depends</span></span>  | <span data-ttu-id="55ef2-199">Die Möglichkeit, das Datenraster auszuwählen, hängt vom Inhalt ab.</span><span class="sxs-lookup"><span data-stu-id="55ef2-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="55ef2-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="55ef2-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="55ef2-201">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="55ef2-201">Depends</span></span>  | <span data-ttu-id="55ef2-202">Ein Datenraster-Steuerelement mit einem-Header sollte das [Table](uiauto-implementingtable.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="55ef2-203">Datenelemente im Datenrastercontainer unterstützen mindestens Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55ef2-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="55ef2-204">[SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster (wenn das Datenraster ausgewählt werden kann)</span><span class="sxs-lookup"><span data-stu-id="55ef2-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="55ef2-205">[ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster (wenn das Datenraster scrollfähig ist)</span><span class="sxs-lookup"><span data-stu-id="55ef2-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="55ef2-206">[GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="55ef2-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="55ef2-207">[TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster (wenn das Datenraster über einen Header verfügt)</span><span class="sxs-lookup"><span data-stu-id="55ef2-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="55ef2-208">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="55ef2-208">Required Events</span></span>

<span data-ttu-id="55ef2-209">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Datenraster-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="55ef2-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="55ef2-210">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55ef2-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="55ef2-211">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="55ef2-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="55ef2-212">Notizen</span><span class="sxs-lookup"><span data-stu-id="55ef2-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55ef2-213">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="55ef2-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="55ef2-214">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="55ef2-215">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="55ef2-216">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="55ef2-217">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="55ef2-218">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="55ef2-219">**UIA \_ layoutinvalidatedeventid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="55ef2-220">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="55ef2-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="55ef2-221">[**UIA \_ Multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="55ef2-222">Wenn das Steuerelement die CurrentView-Eigenschaft des [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Musters unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="55ef2-223">[**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="55ef2-224">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="55ef2-225">[**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="55ef2-226">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="55ef2-227">[**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="55ef2-228">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="55ef2-229">[**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="55ef2-230">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="55ef2-231">[**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="55ef2-232">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="55ef2-233">[**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55ef2-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="55ef2-234">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="55ef2-235">**UIA- \_ Auswahl \_ invalidatedeventid**</span><span class="sxs-lookup"><span data-stu-id="55ef2-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="55ef2-236">Beispiel für den DataGrid-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="55ef2-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="55ef2-237">Die folgende Abbildung veranschaulicht ein Listenansicht-Steuerelement, das den **DataGrid-** Steuerelement Typ implementiert.</span><span class="sxs-lookup"><span data-stu-id="55ef2-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![Screenshot des Listenansicht-Steuer Elements mit DataGrid-Steuerelement Typen](images/datagridxmpl.jpg)

<span data-ttu-id="55ef2-239">Die Steuerelement Ansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur, die sich auf das Listenansicht-Steuerelement bezieht, werden unten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ef2-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="55ef2-240">Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="55ef2-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55ef2-241">Benutzeroberflächenautomatisierungs-Struktur-Steuerelement Ansicht</span><span class="sxs-lookup"><span data-stu-id="55ef2-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="55ef2-242">Benutzeroberflächenautomatisierungs-Struktur-Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="55ef2-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55ef2-243">DataGrid (Sortieren, Tabelle, Auswahl, Raster)</span><span class="sxs-lookup"><span data-stu-id="55ef2-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="55ef2-244">Header</span><span class="sxs-lookup"><span data-stu-id="55ef2-244">Header</span></span>
<ul>
<li><span data-ttu-id="55ef2-245">Header Item &quot; Name &quot; (aufrufen)</span><span class="sxs-lookup"><span data-stu-id="55ef2-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="55ef2-246">Datum des headertem- &quot; Datums &quot; (aufrufen)</span><span class="sxs-lookup"><span data-stu-id="55ef2-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="55ef2-247">Header Item &quot; size &quot; (aufrufen)</span><span class="sxs-lookup"><span data-stu-id="55ef2-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="55ef2-248">Group &quot; &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="55ef2-249">DataItem- &quot; Konten Receivable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="55ef2-250">DataItem- &quot; Konten Payable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="55ef2-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="55ef2-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="55ef2-252">Group &quot; &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="55ef2-253">DataItem- &quot; Konten Receivable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="55ef2-254">DataItem- &quot; Konten Payable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="55ef2-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55ef2-255">\*Das vorangehende Beispiel zeigt ein Datenraster, das mehrere Ebenen von Steuerelementen enthält.</span><span class="sxs-lookup"><span data-stu-id="55ef2-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="55ef2-256">Das **Gruppen** Steuerelement ("kontoso") enthält zwei **DataItem** -Steuerelemente ("Accounts Receivable.doc" und "Accounts Payable.doc").</span><span class="sxs-lookup"><span data-stu-id="55ef2-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="55ef2-257">Ein **DataGrid-** / **GridItem** -Paar ist unabhängig von einem Paar auf einer anderen Ebene.</span><span class="sxs-lookup"><span data-stu-id="55ef2-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="55ef2-258">Die **DataItem** -Steuerelemente unter einer **Gruppe** können auch als [ListItem](uiauto-supportlistitemcontroltype.md) -Steuer Elementtyp verfügbar gemacht werden, sodass Sie deutlicher als auswählbare Objekte und nicht als einfache Datenelemente dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="55ef2-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="55ef2-259">Dieses Beispiel enthält nicht die Unterelemente der gruppierten Datenelemente.</span><span class="sxs-lookup"><span data-stu-id="55ef2-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="55ef2-260">Ein weiteres Beispiel für mehrere Ebenen von Steuerelementen finden Sie unter [DataItem](uiauto-supportdataitemcontroltype.md) -Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="55ef2-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55ef2-261">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55ef2-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="55ef2-262">**Licher**</span><span class="sxs-lookup"><span data-stu-id="55ef2-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55ef2-263">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="55ef2-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="55ef2-264">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="55ef2-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




