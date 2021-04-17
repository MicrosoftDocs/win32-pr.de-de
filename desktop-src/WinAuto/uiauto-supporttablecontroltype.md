---
title: Table-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Tabellen Steuerungstyp.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Tabellen Steuerelement
- Benutzeroberflächenautomatisierungs, Tabellen Steuerungstyp
- UI-Automatisierung, Baumstruktur für den Tabellen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Tabellen Steuerungstyp
- UI-Automatisierung, Steuerelement Muster für den Tabellen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für den Tabellen Steuerungstyp
- Baumstrukturen, Tabellen Steuerelement-Typ
- Eigenschaften, Tabellen Steuerelement-Typ
- Steuerelement Muster, Tabellen Steuerelement-Typ
- Ereignisse, Tabellen Steuerelement-Typ
- Unterstützung für den Tabellen Steuerungstyp
- Table-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für den Tabellen Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den Tabellen Steuerelement-Typ
- Steuerelement Typen, Unterstützung für Tabelle
- Steuerelement Typen, Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515926"
---
# <a name="table-control-type"></a><span data-ttu-id="ce2d2-119">Table-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-119">Table Control Type</span></span>

<span data-ttu-id="ce2d2-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Tabellen** Steuerungstyp.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="ce2d2-121">Tabellen Steuerelemente enthalten Zeilen und Spalten mit Text und, optional, Zeilen-und Spaltenüberschriften.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="ce2d2-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Tabellen** Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="ce2d2-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Table-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ce2d2-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ce2d2-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ce2d2-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ce2d2-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ce2d2-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce2d2-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ce2d2-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ce2d2-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ce2d2-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ce2d2-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ce2d2-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ce2d2-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ce2d2-130">Typical Tree Structure</span></span>

<span data-ttu-id="ce2d2-131">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Table-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ce2d2-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d2-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce2d2-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ce2d2-133">Control View</span></span></th>
<th><span data-ttu-id="ce2d2-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ce2d2-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ce2d2-135">Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce2d2-135">Table</span></span>
<ul>
<li><span data-ttu-id="ce2d2-136">Text (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="ce2d2-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="ce2d2-137">Header (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce2d2-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="ce2d2-138">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce2d2-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce2d2-139">Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce2d2-139">Table</span></span>
<ul>
<li><span data-ttu-id="ce2d2-140">Text (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce2d2-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="ce2d2-141">Verschiedene Steuerelemente (0 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="ce2d2-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce2d2-142">Wenn ein Tabellen Steuerelement über Zeilen-oder Spaltenheader verfügt, müssen diese in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="ce2d2-143">Die Inhaltsansicht muss diese Informationen nicht verfügbar machen, da Sie mithilfe von [**iuiautomationtablepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ce2d2-144">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce2d2-144">Relevant Properties</span></span>

<span data-ttu-id="ce2d2-145">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Table-Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="ce2d2-146">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d2-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ce2d2-147">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce2d2-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ce2d2-148">Wert</span><span class="sxs-lookup"><span data-stu-id="ce2d2-148">Value</span></span>      | <span data-ttu-id="ce2d2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce2d2-150">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ce2d2-151">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-151">See notes.</span></span> | <span data-ttu-id="ce2d2-152">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="ce2d2-153">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ce2d2-154">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-154">See notes.</span></span> | <span data-ttu-id="ce2d2-155">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="ce2d2-156">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ce2d2-157">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-157">See notes.</span></span> | <span data-ttu-id="ce2d2-158">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="ce2d2-159">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="ce2d2-160">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ce2d2-161">**Table**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ce2d2-162">**UIA \_ describedbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ce2d2-163">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-163">See notes.</span></span> | <span data-ttu-id="ce2d2-164">Wenn die Tabelle von anderen Benutzeroberflächenelementen (z. B. von einem Textelement, das die Beschreibung für die Tabelle enthält) mit Anmerkungen versehen ist, sollte die „DescribedBy“-Eigenschaft einen Verweis auf das Automatisierungselement des Textsteuerelements verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="ce2d2-165">**UIA \_ helptextpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="ce2d2-166">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-166">See notes.</span></span> | <span data-ttu-id="ce2d2-167">Weitere Details zum Zweck der Tabelle sollten über diese Eigenschaft verfügbar gemacht werden, wenn Sie von der Eigenschaft [**UIA \_ namepropertyid**](uiauto-automation-element-propids.md) nicht ausreichend erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="ce2d2-168">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ce2d2-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce2d2-169">TRUE</span></span>       | <span data-ttu-id="ce2d2-170">Das Table-Steuerelement muss immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="ce2d2-171">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ce2d2-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce2d2-172">TRUE</span></span>       | <span data-ttu-id="ce2d2-173">Das Table-Steuerelement muss immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="ce2d2-174">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ce2d2-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-175">See notes.</span></span> | <span data-ttu-id="ce2d2-176">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="ce2d2-177">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ce2d2-178">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-178">See notes.</span></span> | <span data-ttu-id="ce2d2-179">Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das Automatisierungselement des Steuerelements verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="ce2d2-180">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ce2d2-181">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-181">See notes.</span></span> | <span data-ttu-id="ce2d2-182">Lokalisierte Zeichenfolge, die dem **Tabellen** Steuerelement-Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="ce2d2-183">Der Standardwert ist "Table" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="ce2d2-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="ce2d2-184">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ce2d2-185">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-185">See notes.</span></span> | <span data-ttu-id="ce2d2-186">Das Table-Steuerelement ruft in der Regel den Wert für seinen Namen aus einer statischen Text Bezeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="ce2d2-187">Wenn keine statische Text Bezeichnung vorhanden ist, muss das Element eine Name-Eigenschaft zuweisen, die immer verfügbar sein muss, um den Zweck der Tabelle zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ce2d2-188">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ce2d2-188">Required Control Patterns</span></span>

<span data-ttu-id="ce2d2-189">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Tabellen Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="ce2d2-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="ce2d2-190">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d2-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ce2d2-191">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="ce2d2-191">Control Pattern</span></span>                                         | <span data-ttu-id="ce2d2-192">Support</span><span class="sxs-lookup"><span data-stu-id="ce2d2-192">Support</span></span>                     | <span data-ttu-id="ce2d2-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce2d2-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="ce2d2-195">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ce2d2-195">Required</span></span>                    | <span data-ttu-id="ce2d2-196">Da das Table-Steuerelement Elemente enthält, die in einem Raster dargestellt sind, unterstützt es immer das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="ce2d2-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="ce2d2-198">Erforderlich für untergeordnete Objekte</span><span class="sxs-lookup"><span data-stu-id="ce2d2-198">Required with child objects</span></span> | <span data-ttu-id="ce2d2-199">Die inneren Objekte einer Tabelle sollten sowohl das [GridItem](uiauto-implementinggriditem.md) -Steuerelement als auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="ce2d2-200">Die Tabelle selbst muss das GridItem-oder TableItem-Steuerelement Muster nicht unterstützen, es sei denn, die Tabelle ist Teil einer anderen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="ce2d2-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="ce2d2-202">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ce2d2-202">Required</span></span>                    | <span data-ttu-id="ce2d2-203">Das Table-Steuerelement kann immer über Header verfügen, die dem Inhalt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="ce2d2-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="ce2d2-205">Erforderlich für untergeordnete Objekte</span><span class="sxs-lookup"><span data-stu-id="ce2d2-205">Required with child objects</span></span> | <span data-ttu-id="ce2d2-206">Die inneren Objekte einer Tabelle sollten sowohl das [GridItem](uiauto-implementinggriditem.md) -Steuerelement als auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="ce2d2-207">Die Tabelle selbst muss das GridItem- oder TableItem-Steuerelementmuster nicht unterstützen, es sei denn, die Tabelle ist Teil einer anderen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ce2d2-208">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ce2d2-208">Required Events</span></span>

<span data-ttu-id="ce2d2-209">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Tabellen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="ce2d2-210">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d2-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ce2d2-211">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="ce2d2-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ce2d2-212">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce2d2-213">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ce2d2-214">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ce2d2-215">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ce2d2-216">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ce2d2-217">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ce2d2-218">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ce2d2-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="ce2d2-219">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ce2d2-220">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce2d2-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ce2d2-221">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ce2d2-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce2d2-222">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ce2d2-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ce2d2-223">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ce2d2-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




