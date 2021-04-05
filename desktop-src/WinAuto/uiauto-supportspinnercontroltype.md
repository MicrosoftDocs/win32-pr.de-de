---
title: Spinner-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Spinner-Steuerelement.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für Spinner-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement Typen
- Benutzeroberflächenautomatisierungs-Struktur für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Spinner-Steuerelement Typen
- Baumstrukturen, Spinner-Steuerelement Typen
- Eigenschaften, Typ des Spinner-Steuer Elements
- Steuerelement Muster, Spinner-Steuerelement Typen
- Ereignisse, Spinner-Steuerelement Typen
- Unterstützung für Spinner-Steuerelement Typen
- Spinner-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Spinner-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Spinner-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Spinner
- Steuerelement Typen, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712701"
---
# <a name="spinner-control-type"></a><span data-ttu-id="ff7b9-119">Spinner-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-119">Spinner Control Type</span></span>

<span data-ttu-id="ff7b9-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Spinner** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="ff7b9-121">Spinner-Steuerelemente werden dazu verwendet, um aus einem Bereich von Elementen oder Zahlen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="ff7b9-122">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Spinner** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="ff7b9-123">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Spinner-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ff7b9-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ff7b9-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ff7b9-125">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ff7b9-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ff7b9-126">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff7b9-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ff7b9-127">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ff7b9-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ff7b9-128">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ff7b9-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ff7b9-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ff7b9-130">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ff7b9-130">Typical Tree Structure</span></span>

<span data-ttu-id="ff7b9-131">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur dargestellt, die sich auf Spinner-Steuerelemente bezieht, wenn Sie das **RangeValue** -Steuerelement und das **Selection** -Steuerelement Muster unterstützen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="ff7b9-132">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff7b9-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="ff7b9-133">**RangeValue-Steuerelement Muster**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff7b9-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ff7b9-134">Control View</span></span></th>
<th><span data-ttu-id="ff7b9-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ff7b9-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff7b9-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff7b9-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff7b9-137">Bearbeitung (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="ff7b9-138">Schaltfläche (2)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ff7b9-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff7b9-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff7b9-140">**Selection-Steuerelementmuster**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff7b9-141">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ff7b9-141">Control View</span></span></th>
<th><span data-ttu-id="ff7b9-142">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ff7b9-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff7b9-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff7b9-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff7b9-144">Bearbeitung (0 oder 1)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="ff7b9-145">Schaltfläche (2)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-145">Button (2)</span></span></li>
<li><span data-ttu-id="ff7b9-146">Listenelement (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ff7b9-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff7b9-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff7b9-148">ListItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff7b9-149">Um sicherzustellen, dass die beiden Schaltflächen in der Teilstruktur der Steuerelement Ansicht von automatisierten Testtools unterschieden werden können, weisen Sie der **AutomationId** -Eigenschaft nach Bedarf den Wert **ScrollAmount \_ SmallIncrement** oder [**ScrollAmount \_ smalldekrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) zu.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="ff7b9-150">Bei einigen Implementierungen ist das zugeordnete Bearbeitungs Steuerelement möglicherweise ein Peer des Spinner-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ff7b9-151">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff7b9-151">Relevant Properties</span></span>

<span data-ttu-id="ff7b9-152">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Spinner-Steuerelemente besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="ff7b9-153">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ff7b9-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ff7b9-154">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff7b9-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ff7b9-155">Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b9-155">Value</span></span>       | <span data-ttu-id="ff7b9-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7b9-157">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ff7b9-158">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-158">See notes.</span></span>  | <span data-ttu-id="ff7b9-159">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="ff7b9-160">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ff7b9-161">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-161">See notes.</span></span>  | <span data-ttu-id="ff7b9-162">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ff7b9-163">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ff7b9-164">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-164">See notes.</span></span>  | <span data-ttu-id="ff7b9-165">Der durch Klicken aktivierbare Punkt des Spinner-Steuerelements übergibt den Fokus an den Bearbeitungsbereich des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ff7b9-166">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ff7b9-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-167">**Spinner**</span></span> | <span data-ttu-id="ff7b9-168">Dieser Wert ist für alle Frameworks gleich.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="ff7b9-169">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ff7b9-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff7b9-170">TRUE</span></span>        | <span data-ttu-id="ff7b9-171">Das Spinner-Steuerelement muss immer ein Inhaltselement sein.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="ff7b9-172">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ff7b9-173">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff7b9-173">TRUE</span></span>        | <span data-ttu-id="ff7b9-174">Das Spinner-Steuerelement muss immer ein Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ff7b9-175">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ff7b9-176">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-176">See notes.</span></span>  | <span data-ttu-id="ff7b9-177">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="ff7b9-178">Ein Spinner-Steuerelement nimmt nur selten den Fokus, aber wenn dies der Fall ist, sollte der Fokus auf dem Spinner-Steuerelement selbst bleiben, nicht auf den untergeordneten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="ff7b9-179">Der Benutzer sollte in der Lage sein, alle scrollaktionen mithilfe der nach-oben-und nach-unten-Taste auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="ff7b9-180">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ff7b9-181">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-181">See notes.</span></span>  | <span data-ttu-id="ff7b9-182">Spinner-Steuerelemente verfügen über eine statische Textbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="ff7b9-183">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ff7b9-184">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-184">See notes.</span></span>  | <span data-ttu-id="ff7b9-185">Lokalisierte Zeichenfolge, die dem **Spinner** -Steuerelement Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="ff7b9-186">Der Standardwert ist "Spinner" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="ff7b9-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="ff7b9-187">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ff7b9-188">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-188">See notes.</span></span>  | <span data-ttu-id="ff7b9-189">Das Spinner-Steuerelement ruft seinen Namen in der Regel aus einer statischen Textbezeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ff7b9-190">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ff7b9-190">Required Control Patterns</span></span>

<span data-ttu-id="ff7b9-191">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Spinner-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff7b9-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="ff7b9-192">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff7b9-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ff7b9-193">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff7b9-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="ff7b9-194">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b9-194">Support/Value</span></span> | <span data-ttu-id="ff7b9-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7b9-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="ff7b9-197">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-197">Depends</span></span>       | <span data-ttu-id="ff7b9-198">Spinner-Steuerelemente, die einen numerischen Bereich umfassen, können das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="ff7b9-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="ff7b9-200">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-200">Depends</span></span>       | <span data-ttu-id="ff7b9-201">Spinner-Steuerelemente, die eine Liste der auszuwählenden Elemente aufweisen, müssen das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="ff7b9-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="ff7b9-203">false</span><span class="sxs-lookup"><span data-stu-id="ff7b9-203">FALSE</span></span>         | <span data-ttu-id="ff7b9-204">Spinner-Steuerelemente sind immer Einfachauswahlcontainer.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="ff7b9-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="ff7b9-206">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="ff7b9-206">Depends</span></span>       | <span data-ttu-id="ff7b9-207">Spinner-Steuerelemente, die einen Satz von Optionen oder Zahlen umfassen, können das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="ff7b9-208">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ff7b9-208">Required Events</span></span>

<span data-ttu-id="ff7b9-209">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Spinner-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="ff7b9-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="ff7b9-210">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff7b9-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ff7b9-211">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="ff7b9-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ff7b9-212">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7b9-213">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ff7b9-214">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ff7b9-215">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ff7b9-216">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ff7b9-217">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ff7b9-218">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="ff7b9-219">[**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="ff7b9-220">Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="ff7b9-221">[**UIA \_ Auswahl für die Eigenschaft " \_ invalidatedeventid**](uiauto-event-ids.md) " für "Changed".</span><span class="sxs-lookup"><span data-stu-id="ff7b9-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="ff7b9-222">Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="ff7b9-223">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="ff7b9-224">[**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="ff7b9-225">Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff7b9-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="ff7b9-226">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff7b9-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff7b9-227">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ff7b9-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff7b9-228">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ff7b9-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ff7b9-229">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ff7b9-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




