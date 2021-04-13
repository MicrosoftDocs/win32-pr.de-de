---
title: Text Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Text Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Text Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Text Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für Text Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Text Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Text Steuerelement-Typ
- Struktur Strukturen, Text Steuerelement-Typ
- Eigenschaften, Text Steuerelement-Typ
- Steuerelement Muster, Text Steuerelement-Typ
- Ereignisse, Text Steuerelement-Typ
- Unterstützung für den Text Steuerungstyp
- Text-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Text Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Text Steuerelement Typen
- Steuerelement Typen, Unterstützung für Text
- Steuerelement Typen, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310591"
---
# <a name="text-control-type"></a><span data-ttu-id="41eca-119">Text Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="41eca-119">Text Control Type</span></span>

<span data-ttu-id="41eca-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement **Text** .</span><span class="sxs-lookup"><span data-stu-id="41eca-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="41eca-121">Ein Text Steuerelement ist ein grundlegendes Element der Benutzeroberfläche, das ein Textelement auf dem Bildschirm darstellt.</span><span class="sxs-lookup"><span data-stu-id="41eca-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="41eca-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuerelement **Text** definiert.</span><span class="sxs-lookup"><span data-stu-id="41eca-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="41eca-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Struktur Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="41eca-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="41eca-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="41eca-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="41eca-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="41eca-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="41eca-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41eca-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="41eca-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="41eca-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="41eca-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="41eca-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="41eca-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41eca-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="41eca-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="41eca-130">Typical Tree Structure</span></span>

<span data-ttu-id="41eca-131">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Text Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="41eca-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="41eca-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41eca-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41eca-133">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="41eca-133">Control View</span></span></th>
<th><span data-ttu-id="41eca-134">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="41eca-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="41eca-135">Text</span><span class="sxs-lookup"><span data-stu-id="41eca-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="41eca-136">Text (wenn Inhalt)</span><span class="sxs-lookup"><span data-stu-id="41eca-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="41eca-137">Ein Textsteuerelement kann eigenständig als Bezeichnung oder als statischer Text auf einem Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41eca-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="41eca-138">Sie kann auch in der Struktur eines der folgenden Elemente enthalten sein:</span><span class="sxs-lookup"><span data-stu-id="41eca-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="41eca-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="41eca-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="41eca-140">ListItem</span><span class="sxs-lookup"><span data-stu-id="41eca-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="41eca-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="41eca-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="41eca-142">Text Steuerelemente werden möglicherweise nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt, weil Text häufig durch die **Name** -Eigenschaft eines anderen Steuer Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="41eca-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="41eca-143">Beispielsweise wird der Text, der zum Bezeichnen eines Kombinations Feld-Steuer Elements verwendet wird, über die **Name** -Eigenschaft des Steuer Elements verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="41eca-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="41eca-144">Da sich das Kombinations Feld-Steuerelement in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur befindet, muss das Text Steuerelement nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="41eca-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="41eca-145">Text Steuerelemente können untergeordnete Elemente in der Inhaltsansicht enthalten, wenn ein eingebettetes Objekt wie ein Hyperlink vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41eca-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="41eca-146">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41eca-146">Relevant Properties</span></span>

<span data-ttu-id="41eca-147">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Text Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="41eca-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="41eca-148">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="41eca-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="41eca-149">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41eca-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="41eca-150">Wert</span><span class="sxs-lookup"><span data-stu-id="41eca-150">Value</span></span>      | <span data-ttu-id="41eca-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="41eca-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41eca-152">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="41eca-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-153">See notes.</span></span> | <span data-ttu-id="41eca-154">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="41eca-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="41eca-155">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="41eca-156">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-156">See notes.</span></span> | <span data-ttu-id="41eca-157">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="41eca-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="41eca-158">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="41eca-159">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-159">See notes.</span></span> | <span data-ttu-id="41eca-160">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="41eca-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="41eca-161">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="41eca-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="41eca-162">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="41eca-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="41eca-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="41eca-164">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="41eca-165">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41eca-165">Depends</span></span>    | <span data-ttu-id="41eca-166">Das Text Steuerelement ist Inhalt, wenn es Informationen enthält, die nicht in der Namenseigenschaft eines anderen Steuer Elements verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="41eca-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="41eca-167">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="41eca-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="41eca-168">TRUE</span></span>       | <span data-ttu-id="41eca-169">Das Textsteuerelement muss stets ein Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="41eca-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="41eca-170">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="41eca-171">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-171">See notes.</span></span> | <span data-ttu-id="41eca-172">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41eca-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="41eca-173">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="41eca-174">NULL</span><span class="sxs-lookup"><span data-stu-id="41eca-174">NULL</span></span>       | <span data-ttu-id="41eca-175">Textsteuerelemente haben keine statische Textbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="41eca-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="41eca-176">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="41eca-177">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-177">See notes.</span></span> | <span data-ttu-id="41eca-178">Lokalisierte Zeichenfolge, die dem **Text** Steuerelement-Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="41eca-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="41eca-179">Der Standardwert ist "Text" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="41eca-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="41eca-180">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="41eca-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="41eca-181">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="41eca-181">See notes.</span></span> | <span data-ttu-id="41eca-182">Der Name eines Text Steuer Elements kann der Text sein, der angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="41eca-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="41eca-183">Wenn das Steuerelement jedoch auch das [Text](uiauto-implementingtextandtextrange.md) Muster unterstützt, und der Text sehr umfangreich ist, verwenden Sie nicht den voll Text Inhalt als **Name** -Wert.</span><span class="sxs-lookup"><span data-stu-id="41eca-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="41eca-184">Geben Sie **stattdessen einen** kürzerer Wert an, der von anderen Eigenschaften Ihres Steuer Elements abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="41eca-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="41eca-185">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="41eca-185">Required Control Patterns</span></span>

<span data-ttu-id="41eca-186">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Text Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="41eca-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="41eca-187">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41eca-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="41eca-188">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="41eca-188">Control Pattern</span></span>                                         | <span data-ttu-id="41eca-189">Support</span><span class="sxs-lookup"><span data-stu-id="41eca-189">Support</span></span> | <span data-ttu-id="41eca-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="41eca-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41eca-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="41eca-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="41eca-192">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41eca-192">Depends</span></span> | <span data-ttu-id="41eca-193">Wenn das Text Steuerelement in einem Tabellen Steuerelement enthalten ist, muss das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="41eca-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="41eca-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="41eca-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="41eca-195">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41eca-195">Depends</span></span> | <span data-ttu-id="41eca-196">Wenn das Text Steuerelement in einem Tabellen Steuerelement enthalten ist, muss das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="41eca-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="41eca-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="41eca-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="41eca-198">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="41eca-198">Depends</span></span> | <span data-ttu-id="41eca-199">Text sollte das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster für eine bessere Barrierefreiheit unterstützen. Es ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41eca-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="41eca-200">Das Text-Steuerelementmuster ist nützlich, wenn der Text viele Formate und Attribute hat (z. B., Farbe, Fettdruck und Kursivdruck).</span><span class="sxs-lookup"><span data-stu-id="41eca-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="41eca-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="41eca-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="41eca-202">Nie</span><span class="sxs-lookup"><span data-stu-id="41eca-202">Never</span></span>   | <span data-ttu-id="41eca-203">Ein Text Steuerelement unterstützt niemals das [value](uiauto-implementingvalue.md) -Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="41eca-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="41eca-204">Wenn der Text bearbeitet werden kann, handelt es sich um den [Bearbeitungs](uiauto-supporteditcontroltype.md) Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="41eca-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="41eca-205">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="41eca-205">Required Events</span></span>

<span data-ttu-id="41eca-206">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Text Steuerelemente zur Unterstützung von benötigen</span><span class="sxs-lookup"><span data-stu-id="41eca-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="41eca-207">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="41eca-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="41eca-208">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="41eca-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="41eca-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="41eca-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41eca-210">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="41eca-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="41eca-211">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41eca-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="41eca-212">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41eca-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="41eca-213">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41eca-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="41eca-214">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41eca-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="41eca-215">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41eca-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="41eca-216">[**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41eca-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="41eca-217">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="41eca-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="41eca-218">**UIA \_ \_ -Text textchangedebug**</span><span class="sxs-lookup"><span data-stu-id="41eca-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="41eca-219">Wenn das Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="41eca-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="41eca-220">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41eca-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="41eca-221">**Licher**</span><span class="sxs-lookup"><span data-stu-id="41eca-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="41eca-222">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="41eca-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="41eca-223">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="41eca-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




