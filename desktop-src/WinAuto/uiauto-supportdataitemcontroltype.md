---
title: DataItem-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den DataItem-Steuerelement Typen.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, DataItem-Steuerelement Typen
- UI-Automatisierung, Baumstruktur für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für DataItem-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für DataItem-Steuerelement Typen
- UI-Automatisierung, Ereignisse für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, große Listen und DataItem-Steuerelement Typen
- Struktur Strukturen, DataItem-Steuerelement Typen
- Eigenschaften, DataItem-Steuerelement Typen
- Steuerelement Muster, DataItem-Steuerelement Typen
- Ereignisse, DataItem-Steuerelement Typen
- große Listen
- Unterstützung für DataItem-Steuerelement Typen
- DataItem-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für DataItem-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für DataItem-Steuerelement Typen
- Steuerelement Typen, große Listen und DataItem-Steuerelement Typen
- Steuerelement Typen, Unterstützung für DataItem
- Steuerelement Typen, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036857"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="972d7-122">DataItem-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="972d7-122">DataItem Control Type</span></span>

<span data-ttu-id="972d7-123">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **DataItem** -Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="972d7-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="972d7-124">Ein Eintrag in einer Kontaktliste ist ein Beispiel für ein Datenelement-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="972d7-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="972d7-125">Ein Datenelement-Steuerelement enthält Informationen, die für einen Endbenutzer von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="972d7-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="972d7-126">Es ist komplizierter als das einfache Listenelement, da es mehr Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="972d7-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="972d7-127">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **DataItem** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="972d7-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="972d7-128">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Datenelement-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="972d7-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="972d7-129">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="972d7-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="972d7-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="972d7-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="972d7-131">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="972d7-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="972d7-132">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="972d7-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="972d7-133">Arbeiten mit dataItems in großen Listen</span><span class="sxs-lookup"><span data-stu-id="972d7-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="972d7-134">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="972d7-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="972d7-135">Beispiel für DataItem-Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="972d7-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="972d7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="972d7-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="972d7-137">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="972d7-137">Typical Tree Structure</span></span>

<span data-ttu-id="972d7-138">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Datenelement-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="972d7-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="972d7-139">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="972d7-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="972d7-140">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="972d7-140">Control View</span></span></th>
<th><span data-ttu-id="972d7-141">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="972d7-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="972d7-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="972d7-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="972d7-143">Variabel (0 oder mehr, kann hierarchisch strukturiert werden)</span><span class="sxs-lookup"><span data-stu-id="972d7-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="972d7-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="972d7-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="972d7-145">Variabel (0 oder mehr, kann hierarchisch strukturiert werden)</span><span class="sxs-lookup"><span data-stu-id="972d7-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="972d7-146">Ein DataItem-Element in einem Datenraster kann eine Vielzahl von Objekten hosten, wie etwa eine andere Ebene von Datenelementen oder bestimmte Rasterelemente, z. B. Text, Bilder oder Bearbeitungssteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="972d7-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="972d7-147">Wenn das Datenelement Element über eine bestimmte Objekt Rolle verfügt, muss das Element als bestimmter Steuer Elementtyp verfügbar gemacht werden. beispielsweise ein [ListItem](uiauto-supportlistitemcontroltype.md) -Steuer Elementtyp für ein auswählbares Datenelement im Raster.</span><span class="sxs-lookup"><span data-stu-id="972d7-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="972d7-148">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="972d7-148">Relevant Properties</span></span>

<span data-ttu-id="972d7-149">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den DataItem-Steuerelement-Typ besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="972d7-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="972d7-150">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="972d7-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="972d7-151">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="972d7-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="972d7-152">Wert</span><span class="sxs-lookup"><span data-stu-id="972d7-152">Value</span></span>        | <span data-ttu-id="972d7-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="972d7-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="972d7-154">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="972d7-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-155">See notes.</span></span>   | <span data-ttu-id="972d7-156">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="972d7-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="972d7-157">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="972d7-158">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-158">See notes.</span></span>   | <span data-ttu-id="972d7-159">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="972d7-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="972d7-160">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="972d7-161">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-161">See notes.</span></span>   | <span data-ttu-id="972d7-162">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="972d7-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="972d7-163">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="972d7-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="972d7-164">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="972d7-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="972d7-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="972d7-166">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="972d7-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="972d7-167">TRUE</span></span>         | <span data-ttu-id="972d7-168">Das Datenelement-Steuerelement muss immer ein Inhaltselement sein.</span><span class="sxs-lookup"><span data-stu-id="972d7-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="972d7-169">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="972d7-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="972d7-170">TRUE</span></span>         | <span data-ttu-id="972d7-171">Das Datenelement-Steuerelement muss immer ein Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="972d7-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="972d7-172">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="972d7-173">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-173">See notes.</span></span>   | <span data-ttu-id="972d7-174">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="972d7-175">**UIA \_ itemstatuspropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="972d7-176">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-176">See notes.</span></span>   | <span data-ttu-id="972d7-177">Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="972d7-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="972d7-178">**UIA \_ itemtypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="972d7-179">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-179">See notes.</span></span>   | <span data-ttu-id="972d7-180">Dies ist der Zeichenfolgenwert, der dem Endbenutzer das zugrunde liegende Objekt übermittelt, das vom Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="972d7-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="972d7-181">Beispiele hierfür sind "Media File" und "Contact".</span><span class="sxs-lookup"><span data-stu-id="972d7-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="972d7-182">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="972d7-183">Null</span><span class="sxs-lookup"><span data-stu-id="972d7-183">Null</span></span>         | <span data-ttu-id="972d7-184">Datenelement-Steuerelemente verfügen nicht über eine statische Textbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="972d7-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="972d7-185">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="972d7-186">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-186">See notes.</span></span>   | <span data-ttu-id="972d7-187">Lokalisierte Zeichenfolge, die dem **DataItem** -Steuerelement Typen entspricht.</span><span class="sxs-lookup"><span data-stu-id="972d7-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="972d7-188">Der Standardwert ist "Datenelement" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="972d7-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="972d7-189">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="972d7-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="972d7-190">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="972d7-190">See notes.</span></span>   | <span data-ttu-id="972d7-191">Das Datenelement-Steuerelement enthält immer ein primäres Textelement, das der Benutzer als Bezeichner für das Element erkennen würde.</span><span class="sxs-lookup"><span data-stu-id="972d7-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="972d7-192">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="972d7-192">Required Control Patterns</span></span>

<span data-ttu-id="972d7-193">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von allen Datenelement Steuerelementen unterstützt werden müssen</span><span class="sxs-lookup"><span data-stu-id="972d7-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="972d7-194">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="972d7-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="972d7-195">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="972d7-195">Control Pattern</span></span>                                                   | <span data-ttu-id="972d7-196">Support</span><span class="sxs-lookup"><span data-stu-id="972d7-196">Support</span></span> | <span data-ttu-id="972d7-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="972d7-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="972d7-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="972d7-199">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-199">Depends</span></span> | <span data-ttu-id="972d7-200">Wenn das Datenelement erweitert oder reduziert werden kann, um Informationen anzuzeigen und auszublenden, muss das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="972d7-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="972d7-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="972d7-202">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-202">Depends</span></span> | <span data-ttu-id="972d7-203">Datenelemente unterstützen das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster, wenn eine Auflistung von Datenelementen in einem Container verfügbar ist, der räumlich navigiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="972d7-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="972d7-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="972d7-205">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-205">Depends</span></span> | <span data-ttu-id="972d7-206">Alle Datenelemente unterstützen die Möglichkeit, mit dem [ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster in die Ansicht zu scrollen, wenn Ihr Datencontainer mehr Elemente enthält, als auf den Bildschirm passen.</span><span class="sxs-lookup"><span data-stu-id="972d7-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="972d7-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="972d7-208">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-208">Depends</span></span> | <span data-ttu-id="972d7-209">Die Möglichkeit, die Datenelemente auszuwählen, hängt vom Inhalt ab.</span><span class="sxs-lookup"><span data-stu-id="972d7-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="972d7-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="972d7-211">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-211">Depends</span></span> | <span data-ttu-id="972d7-212">Wenn das Datenelement in einem [DataGrid-](uiauto-supportdatagridcontroltype.md) Steuer Elementtyp enthalten ist, der über ein Header Element verfügt, sollte das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="972d7-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="972d7-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="972d7-214">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-214">Depends</span></span> | <span data-ttu-id="972d7-215">Wenn das Datenelement einen Zustand enthält, der durchlaufen werden kann, sollte es das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="972d7-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="972d7-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="972d7-217">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="972d7-217">Depends</span></span> | <span data-ttu-id="972d7-218">Wenn der primäre Text des Datenelements bearbeitbar ist, muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="972d7-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="972d7-219">Arbeiten mit dataItems in großen Listen</span><span class="sxs-lookup"><span data-stu-id="972d7-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="972d7-220">Da große Listen häufig innerhalb von Benutzeroberflächen-Frameworks virtualisiert werden, um die Leistung zu unterstützen, kann ein Benutzeroberflächenautomatisierungs-Client die Funktion "UI Automation Query" nicht verwenden, um den Inhalt der gesamten Struktur auf die gleiche Weise zu durchsuchen wie in anderen Element Containern.</span><span class="sxs-lookup"><span data-stu-id="972d7-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="972d7-221">Ein Client sollte den Bildlauf im Element anzeigen (oder das Steuerelement erweitern, um alle verfügbaren Optionen anzuzeigen), bevor er auf den vollständigen Satz von Informationen aus dem Datenelement zugreift.</span><span class="sxs-lookup"><span data-stu-id="972d7-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="972d7-222">Wenn Sie [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) für das Benutzeroberflächenautomatisierungs-Element für das Datenelement aufrufen, gibt Microsoft Windows-Explorer erfolgreich zurück und bewirkt, dass der Fokus auf das Bearbeitungs Steuerelement innerhalb der Datenelement-Teilstruktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="972d7-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="972d7-223">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="972d7-223">Required Events</span></span>

<span data-ttu-id="972d7-224">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Datenelement-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="972d7-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="972d7-225">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="972d7-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="972d7-226">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="972d7-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="972d7-227">Notizen</span><span class="sxs-lookup"><span data-stu-id="972d7-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="972d7-228">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="972d7-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="972d7-229">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="972d7-230">[**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="972d7-231">Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="972d7-232">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="972d7-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="972d7-233">Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="972d7-234">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="972d7-235">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="972d7-236">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="972d7-237">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="972d7-238">[**UIA \_ Itemstatuspropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="972d7-239">Wenn das Steuerelement die [**ItemStatus**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="972d7-240">[**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="972d7-241">**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**</span><span class="sxs-lookup"><span data-stu-id="972d7-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="972d7-242">Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="972d7-243">**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**</span><span class="sxs-lookup"><span data-stu-id="972d7-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="972d7-244">Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="972d7-245">**UIA \_ SelectionItem \_ elementselectedebug**</span><span class="sxs-lookup"><span data-stu-id="972d7-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="972d7-246">Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="972d7-247">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="972d7-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="972d7-248">[**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="972d7-249">Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="972d7-250">[**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="972d7-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="972d7-251">Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="972d7-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="972d7-252">Beispiel für DataItem-Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="972d7-252">DataItem Control Type Example</span></span>

<span data-ttu-id="972d7-253">Die folgende Abbildung veranschaulicht einen DataItem-Steuerelement Typen in einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="972d7-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![Screenshot des Listenansicht-Steuer Elements mit DataItem-Steuerelement Typen](images/dataitemxmpl.jpg)

<span data-ttu-id="972d7-255">Die Steuerelement Ansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur, die sich auf das Datenelement-Steuerelement bezieht, werden unten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="972d7-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="972d7-256">Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="972d7-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="972d7-257">Die **Gruppe** "Configuration Manager" ist auch Teil des Rasters des Datenraster-Host Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="972d7-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="972d7-258">Ein Beispiel für eine Raster Struktur höherer Ebene finden Sie unter [DataGrid-Steuerelement Typen](uiauto-supportdatagridcontroltype.md).</span><span class="sxs-lookup"><span data-stu-id="972d7-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="972d7-259">Benutzeroberflächenautomatisierungs-Struktur-Steuerelement Ansicht</span><span class="sxs-lookup"><span data-stu-id="972d7-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="972d7-260">Benutzeroberflächenautomatisierungs-Struktur-Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="972d7-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="972d7-261">Group &quot; &quot; (Tabelle, Raster)</span><span class="sxs-lookup"><span data-stu-id="972d7-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="972d7-262">DataItem- &quot; Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)</span><span class="sxs-lookup"><span data-stu-id="972d7-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="972d7-263">Receivable.docfür Image &quot; Konten &quot;</span><span class="sxs-lookup"><span data-stu-id="972d7-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="972d7-264">&quot;Name bearbeiten &quot; (TableItem, GridItem, Wert &quot; Konten Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="972d7-265">Änderungs &quot; Datum geändert &quot; (TableItem, GridItem, Wert &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="972d7-266">&quot;Größe bearbeiten &quot; (GridItem, TableItem, Wert &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="972d7-267">DataItem- &quot; Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)</span><span class="sxs-lookup"><span data-stu-id="972d7-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="972d7-268">...</span><span class="sxs-lookup"><span data-stu-id="972d7-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="972d7-269">Group &quot; &quot; (Tabelle, Raster)</span><span class="sxs-lookup"><span data-stu-id="972d7-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="972d7-270">DataItem- &quot; Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)</span><span class="sxs-lookup"><span data-stu-id="972d7-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="972d7-271">Receivable.docfür Image &quot; Konten &quot;</span><span class="sxs-lookup"><span data-stu-id="972d7-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="972d7-272">&quot;Name bearbeiten &quot; (TableItem, GridItem, Wert &quot; Konten Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="972d7-273">Änderungs &quot; Datum geändert &quot; (TableItem, GridItem, Wert &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="972d7-274">&quot;Größe bearbeiten &quot; (GridItem, TableItem, Wert &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="972d7-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="972d7-275">DataItem- &quot; Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)</span><span class="sxs-lookup"><span data-stu-id="972d7-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="972d7-276">...</span><span class="sxs-lookup"><span data-stu-id="972d7-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="972d7-277">Wenn ein Raster eine Liste auswählbarer Elemente darstellt, können die entsprechenden auswählbaren Benutzeroberflächen Elemente mit dem Steuer Elementtyp " [ListItem](uiauto-supportlistitemcontroltype.md) " statt mit dem Steuer Elementtyp "DataItem" verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="972d7-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="972d7-278">Im vorherigen Beispiel können die **DataItem** -Elemente ("Accounts Receivable.doc" und "Accounts Payable.doc") unter " **Group** (" ")" ("kontoso") verbessert werden, indem Sie als ListItem-Steuerelement Typen verfügbar gemacht werden, da dieser Typ bereits das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="972d7-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="972d7-279">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="972d7-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="972d7-280">**Licher**</span><span class="sxs-lookup"><span data-stu-id="972d7-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="972d7-281">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="972d7-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="972d7-282">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="972d7-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




