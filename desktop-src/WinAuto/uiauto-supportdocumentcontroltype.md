---
title: Dokument Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp "Dokument".
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Dokument Steuerelement Typen
- UI-Automatisierung, Dokument Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Dokument Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für Dokument Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Dokument Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Dokument Steuerelement Typen
- Struktur Strukturen, Dokument Steuerelement-Typ
- Eigenschaften, Dokument Steuerelement-Typ
- Steuerelement Muster, Dokument Steuerelement-Typ
- Ereignisse, Dokument Steuerelement-Typ
- Unterstützung für Dokument Steuerelement Typen
- Document-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Dokument Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Dokument Steuerelement Typen
- Steuerelement Typen, Unterstützung für Dokumente
- Steuerelement Typen, Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036856"
---
# <a name="document-control-type"></a><span data-ttu-id="dea25-119">Dokument Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="dea25-119">Document Control Type</span></span>

<span data-ttu-id="dea25-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp " **Dokument** ".</span><span class="sxs-lookup"><span data-stu-id="dea25-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="dea25-121">Mithilfe von Dokumentsteuerelementen kann ein Benutzer mehrere Seiten Text anzeigen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="dea25-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="dea25-122">Im Gegensatz zu Bearbeitungs Steuerelementen, die nur eine einfache Zeile unformatierten Texts unterstützen, können Dokument Steuerelemente den umfangreichen und formatierten Text hosten.</span><span class="sxs-lookup"><span data-stu-id="dea25-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="dea25-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Dokument** Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="dea25-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="dea25-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Dokument Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="dea25-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="dea25-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dea25-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dea25-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="dea25-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="dea25-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dea25-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="dea25-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="dea25-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="dea25-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dea25-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="dea25-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dea25-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="dea25-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="dea25-131">Typical Tree Structure</span></span>

<span data-ttu-id="dea25-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Dokument Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dea25-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="dea25-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dea25-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dea25-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="dea25-134">Control View</span></span></th>
<th><span data-ttu-id="dea25-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="dea25-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="dea25-136">Dokument</span><span class="sxs-lookup"><span data-stu-id="dea25-136">Document</span></span>
<ul>
<li><span data-ttu-id="dea25-137">Varies</span><span class="sxs-lookup"><span data-stu-id="dea25-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="dea25-138">Dokument</span><span class="sxs-lookup"><span data-stu-id="dea25-138">Document</span></span>
<ul>
<li><span data-ttu-id="dea25-139">Varies</span><span class="sxs-lookup"><span data-stu-id="dea25-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="dea25-140">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dea25-140">Relevant Properties</span></span>

<span data-ttu-id="dea25-141">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Dokument Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="dea25-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="dea25-142">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="dea25-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="dea25-143">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dea25-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="dea25-144">Wert</span><span class="sxs-lookup"><span data-stu-id="dea25-144">Value</span></span>        | <span data-ttu-id="dea25-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="dea25-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea25-146">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="dea25-147">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-147">See notes.</span></span>   | <span data-ttu-id="dea25-148">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="dea25-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="dea25-149">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="dea25-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-150">See notes.</span></span>   | <span data-ttu-id="dea25-151">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="dea25-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="dea25-152">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="dea25-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-153">See notes.</span></span>   | <span data-ttu-id="dea25-154">Das Dokument hat einen klickbaren Punkt, über den veranlasst werden kann, dass das Dokument oder eines seiner Elemente im Dokumentcontainer den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="dea25-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="dea25-155">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="dea25-156">**Dokument**</span><span class="sxs-lookup"><span data-stu-id="dea25-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="dea25-157">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="dea25-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="dea25-158">TRUE</span></span>         | <span data-ttu-id="dea25-159">Das Dokument Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="dea25-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="dea25-160">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="dea25-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="dea25-161">TRUE</span></span>         | <span data-ttu-id="dea25-162">Das Dokument Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="dea25-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="dea25-163">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="dea25-164">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-164">See notes.</span></span>   | <span data-ttu-id="dea25-165">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="dea25-166">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="dea25-167">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-167">See notes.</span></span>   | <span data-ttu-id="dea25-168">Der Wert dieser Eigenschaft muss die Bezeichnung des Dokumentsteuerelements sein.</span><span class="sxs-lookup"><span data-stu-id="dea25-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="dea25-169">In der Regel wird der Titel des Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="dea25-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="dea25-170">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="dea25-171">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-171">See notes.</span></span>   | <span data-ttu-id="dea25-172">Lokalisierte Zeichenfolge, die dem **Dokument** Steuerelement-Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="dea25-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="dea25-173">Der Standardwert ist "Document" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="dea25-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="dea25-174">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="dea25-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="dea25-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dea25-175">See notes.</span></span>   | <span data-ttu-id="dea25-176">Das Dokument Steuerelement erhält seinen Namen in der Regel aus dem Dateinamen, aus dem er geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="dea25-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="dea25-177">Dieser wird häufig im Titel eines umgebenden Fensters oder Rahmens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dea25-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="dea25-178">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="dea25-178">Required Control Patterns</span></span>

<span data-ttu-id="dea25-179">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Dokument Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="dea25-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="dea25-180">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dea25-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="dea25-181">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="dea25-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="dea25-182">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="dea25-182">Support/Value</span></span> | <span data-ttu-id="dea25-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="dea25-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea25-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="dea25-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="dea25-185">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="dea25-185">Depends</span></span>       | <span data-ttu-id="dea25-186">Das Dokumentsteuerelement kann einen Bereich umfassen, der größer ist als der Bereich des Viewports.</span><span class="sxs-lookup"><span data-stu-id="dea25-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="dea25-187">Das-Steuerelement muss das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützen, wenn der Inhalt ScrollBar ist.</span><span class="sxs-lookup"><span data-stu-id="dea25-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="dea25-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="dea25-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="dea25-189">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dea25-189">Required</span></span>      | <span data-ttu-id="dea25-190">Alle Dokument Steuerelemente müssen das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="dea25-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="dea25-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="dea25-192">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="dea25-192">Depends</span></span>       | <span data-ttu-id="dea25-193">Während Benutzeroberflächenautomatisierungs-Clients mit [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) Textinformationen zu einem Dokument abrufen können, benötigen Sie das [value](uiauto-implementingvalue.md) -Steuerelement Muster, um den inneren Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dea25-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="dea25-194">Ein einfacher Text Eintrag ist nur über das Value-Steuerelement Muster möglich.</span><span class="sxs-lookup"><span data-stu-id="dea25-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="dea25-195">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dea25-195">Required Events</span></span>

<span data-ttu-id="dea25-196">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Dokument Steuerelementen unterstützt werden müssen</span><span class="sxs-lookup"><span data-stu-id="dea25-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="dea25-197">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dea25-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="dea25-198">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="dea25-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="dea25-199">Notizen</span><span class="sxs-lookup"><span data-stu-id="dea25-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea25-200">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="dea25-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="dea25-201">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="dea25-202">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="dea25-203">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="dea25-204">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="dea25-205">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="dea25-206">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="dea25-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="dea25-207">[**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="dea25-208">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="dea25-209">[**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="dea25-210">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="dea25-211">[**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="dea25-212">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="dea25-213">[**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="dea25-214">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="dea25-215">[**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="dea25-216">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="dea25-217">[**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="dea25-218">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="dea25-219">**UIA- \_ Auswahl \_ invalidatedeventid**</span><span class="sxs-lookup"><span data-stu-id="dea25-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="dea25-220">Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="dea25-221">**UIA \_ \_ -Text textselectionchangedebug**</span><span class="sxs-lookup"><span data-stu-id="dea25-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="dea25-222">**UIA \_ \_ -Text textchangedebug**</span><span class="sxs-lookup"><span data-stu-id="dea25-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="dea25-223">[**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dea25-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="dea25-224">Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dea25-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="dea25-225">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dea25-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dea25-226">**Licher**</span><span class="sxs-lookup"><span data-stu-id="dea25-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dea25-227">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="dea25-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="dea25-228">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="dea25-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




