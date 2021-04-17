---
title: Pane-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Pane-Steuerelement Typen.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Pane-Steuerelement
- Benutzeroberflächenautomatisierungs, Bereich-Steuerelement Typen
- UI-Automatisierung, Struktur für Pane-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für den Pane-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Pane-Steuerelement Typen
- UI-Automatisierung, Ereignisse für den Pane-Steuerelement Typen
- Struktur Strukturen, Pane-Steuerelement Typen
- Eigenschaften, Fenster Steuerelement-Typ
- Steuerelement Muster, Fenster Steuerelement-Typ
- Ereignisse, Pane-Steuerelement Typen
- Unterstützung für Pane-Steuerelement Typen
- Pane-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für den Pane-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Pane-Steuer ungstyp
- Steuerelement Typen, Unterstützung für Bereich
- Steuerelement Typen, Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566785"
---
# <a name="pane-control-type"></a><span data-ttu-id="98e6e-119">Pane-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="98e6e-119">Pane Control Type</span></span>

<span data-ttu-id="98e6e-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Pane** -Steuerelement Typen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="98e6e-121">Der **Pane** -Steuer ungstyp ist für potenziell Bild lauffähigen Bereiche mit unterschiedlichen Inhalten.</span><span class="sxs-lookup"><span data-stu-id="98e6e-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="98e6e-122">Sie wird verwendet, um ein Objekt innerhalb eines Frame-oder Dokument Fensters darzustellen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="98e6e-123">Benutzer können zwischen Pane-Steuerelementen und innerhalb des Inhalts des aktuellen Bereichs navigieren.</span><span class="sxs-lookup"><span data-stu-id="98e6e-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="98e6e-124">Bereichs Steuerelemente stellen eine Gruppierungs Ebene unterhalb von Fenstern oder Dokumenten dar, jedoch oberhalb einzelner Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="98e6e-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="98e6e-125">Der Benutzer kann je nach Kontext durch Drücken von TAB, F6 oder STRG+TAB zwischen den Bereichen navigieren.</span><span class="sxs-lookup"><span data-stu-id="98e6e-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="98e6e-126">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Pane** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="98e6e-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="98e6e-127">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Bereichs Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und</span><span class="sxs-lookup"><span data-stu-id="98e6e-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="98e6e-128">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="98e6e-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="98e6e-129">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="98e6e-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="98e6e-130">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98e6e-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="98e6e-131">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="98e6e-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="98e6e-132">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="98e6e-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="98e6e-133">Beispiel für Pane-Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="98e6e-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="98e6e-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98e6e-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="98e6e-135">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="98e6e-135">Typical Tree Structure</span></span>

<span data-ttu-id="98e6e-136">In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Bereichs Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="98e6e-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="98e6e-137">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="98e6e-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98e6e-138">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="98e6e-138">Control View</span></span></th>
<th><span data-ttu-id="98e6e-139">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="98e6e-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="98e6e-140">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98e6e-141">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="98e6e-142">Ein Pane-Steuerelement wird immer in der Steuerelement-und der Inhaltsansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98e6e-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="98e6e-143">Machen Sie ein Layoutobjekt nicht als Bereich in der Steuerelement-oder der Inhaltsansicht verfügbar, wenn das Objekt nur für die visuelle Darstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98e6e-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="98e6e-144">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98e6e-144">Relevant Properties</span></span>

<span data-ttu-id="98e6e-145">In der folgenden Tabelle werden die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Werte oder Definitionen für Bereichs Steuerelemente besonders relevant sind.</span><span class="sxs-lookup"><span data-stu-id="98e6e-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="98e6e-146">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="98e6e-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="98e6e-147">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98e6e-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="98e6e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="98e6e-148">Value</span></span>      | <span data-ttu-id="98e6e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="98e6e-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98e6e-150">**UIA \_ accesskeypropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="98e6e-151">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-151">See notes.</span></span> | <span data-ttu-id="98e6e-152">Wenn eine bestimmte Tastenkombination den Fokus auf den Bereich legt, müssen diese Informationen über diese Eigenschaft verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="98e6e-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="98e6e-153">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="98e6e-154">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-154">See notes.</span></span> | <span data-ttu-id="98e6e-155">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="98e6e-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="98e6e-156">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="98e6e-157">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-157">See notes.</span></span> | <span data-ttu-id="98e6e-158">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="98e6e-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="98e6e-159">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="98e6e-160">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-160">See notes.</span></span> | <span data-ttu-id="98e6e-161">Diese Eigenschaft macht einen durch Klicken aktivierbaren Punkt des Bereichssteuerelements verfügbar, durch den der Bereich den Fokus erhält, wenn auf den Punkt geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="98e6e-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="98e6e-162">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="98e6e-163">**Bereich**</span><span class="sxs-lookup"><span data-stu-id="98e6e-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="98e6e-164">**UIA \_ helptextpropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="98e6e-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-165">See notes.</span></span> | <span data-ttu-id="98e6e-166">Der Hilfetext für Bereichs Steuerelemente sollte den Zweck des Frames und seine Beziehung zu anderen Frames erläutern.</span><span class="sxs-lookup"><span data-stu-id="98e6e-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="98e6e-167">Eine Beschreibung ist erforderlich, wenn der Zweck und die Beziehung der Frames nicht aus dem Wert der Eigenschaft [**UIA \_ namepropertyid**](uiauto-automation-element-propids.md) gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="98e6e-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="98e6e-168">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="98e6e-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="98e6e-169">TRUE</span></span>       | <span data-ttu-id="98e6e-170">Das Bereichs Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="98e6e-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="98e6e-171">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="98e6e-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="98e6e-172">TRUE</span></span>       | <span data-ttu-id="98e6e-173">Das Pane-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="98e6e-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="98e6e-174">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="98e6e-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-175">See notes.</span></span> | <span data-ttu-id="98e6e-176">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="98e6e-177">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="98e6e-178">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-178">See notes.</span></span> | <span data-ttu-id="98e6e-179">Bereichssteuerelemente haben in der Regel keine statische Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="98e6e-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="98e6e-180">Ist eine statische Beschriftung vorhanden, muss sie über diese Eigenschaft verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="98e6e-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="98e6e-181">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="98e6e-182">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-182">See notes.</span></span> | <span data-ttu-id="98e6e-183">Lokalisierte Zeichenfolge für den Steuerelement-Typ " **Pane** ".</span><span class="sxs-lookup"><span data-stu-id="98e6e-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="98e6e-184">Der Standardwert ist "Pane" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="98e6e-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="98e6e-185">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="98e6e-186">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="98e6e-186">See notes.</span></span> | <span data-ttu-id="98e6e-187">Der Wert für diese Eigenschaft muss immer ein eindeutiger, präziser und aussagekräftiger Titel sein.</span><span class="sxs-lookup"><span data-stu-id="98e6e-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="98e6e-188">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="98e6e-188">Required Control Patterns</span></span>

<span data-ttu-id="98e6e-189">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Bereichs Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="98e6e-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="98e6e-190">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="98e6e-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="98e6e-191">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="98e6e-191">Control Pattern</span></span>                                         | <span data-ttu-id="98e6e-192">Support</span><span class="sxs-lookup"><span data-stu-id="98e6e-192">Support</span></span> | <span data-ttu-id="98e6e-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="98e6e-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98e6e-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="98e6e-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="98e6e-195">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="98e6e-195">Depends</span></span> | <span data-ttu-id="98e6e-196">Implementieren Sie das [Dock](uiauto-implementingdock.md) -Steuerelement Muster, wenn das Bereichs Steuerelement angedockt werden kann.</span><span class="sxs-lookup"><span data-stu-id="98e6e-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="98e6e-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="98e6e-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="98e6e-198">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="98e6e-198">Depends</span></span> | <span data-ttu-id="98e6e-199">Implementieren Sie das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, wenn das Bereichs Steuerelement gescrollt werden kann.</span><span class="sxs-lookup"><span data-stu-id="98e6e-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="98e6e-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="98e6e-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="98e6e-201">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="98e6e-201">Depends</span></span> | <span data-ttu-id="98e6e-202">Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn das Pane-Steuerelement auf dem Bildschirm verschoben, verkleinert oder gedreht werden kann.</span><span class="sxs-lookup"><span data-stu-id="98e6e-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="98e6e-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="98e6e-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="98e6e-204">Nie</span><span class="sxs-lookup"><span data-stu-id="98e6e-204">Never</span></span>   | <span data-ttu-id="98e6e-205">Wenn das Element das [Window](uiauto-implementingwindow.md) -Steuerelement Muster implementieren muss, sollte das Steuerelement auf dem Steuer Elementtyp " [Window](uiauto-supportwindowcontroltype.md) " basieren.</span><span class="sxs-lookup"><span data-stu-id="98e6e-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="98e6e-206">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="98e6e-206">Required Events</span></span>

<span data-ttu-id="98e6e-207">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Bereichs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="98e6e-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="98e6e-208">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="98e6e-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="98e6e-209">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="98e6e-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="98e6e-210">Notizen</span><span class="sxs-lookup"><span data-stu-id="98e6e-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98e6e-211">**UIA \_ asynccontentloadedeventid**</span><span class="sxs-lookup"><span data-stu-id="98e6e-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="98e6e-212">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="98e6e-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="98e6e-213">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="98e6e-214">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="98e6e-215">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="98e6e-216">[**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="98e6e-217">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="98e6e-218">[**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="98e6e-219">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="98e6e-220">[**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="98e6e-221">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="98e6e-222">[**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="98e6e-223">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="98e6e-224">[**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="98e6e-225">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="98e6e-226">[**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98e6e-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="98e6e-227">Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="98e6e-228">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="98e6e-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="98e6e-229">Beispiel für Pane-Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="98e6e-229">Pane Control Type Example</span></span>

<span data-ttu-id="98e6e-230">Die folgende Abbildung veranschaulicht **ein Steuerelement, das den Steuer** Element-Steuerelement Typ implementiert.</span><span class="sxs-lookup"><span data-stu-id="98e6e-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![Screenshot mit einem Beispiel für ein Pane-Steuerelement](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98e6e-232">Benutzeroberflächenautomatisierungs-Struktur – Steuerelement Ansicht</span><span class="sxs-lookup"><span data-stu-id="98e6e-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="98e6e-233">Benutzeroberflächenautomatisierungs-Struktur – Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="98e6e-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="98e6e-234">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-234">Pane</span></span>
<ul>
<li><span data-ttu-id="98e6e-235">Struktur (Scroll-Muster)</span><span class="sxs-lookup"><span data-stu-id="98e6e-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="98e6e-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="98e6e-236">TreeItem</span></span></li>
<li><span data-ttu-id="98e6e-237">...</span><span class="sxs-lookup"><span data-stu-id="98e6e-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="98e6e-238">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-238">Pane</span></span>
<ul>
<li><span data-ttu-id="98e6e-239">Bearbeiten (Scroll-Muster)</span><span class="sxs-lookup"><span data-stu-id="98e6e-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98e6e-240">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-240">Pane</span></span>
<ul>
<li><span data-ttu-id="98e6e-241">Struktur (Scroll-Muster)</span><span class="sxs-lookup"><span data-stu-id="98e6e-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="98e6e-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="98e6e-242">TreeItem</span></span></li>
<li><span data-ttu-id="98e6e-243">...</span><span class="sxs-lookup"><span data-stu-id="98e6e-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="98e6e-244">Bereich</span><span class="sxs-lookup"><span data-stu-id="98e6e-244">Pane</span></span>
<ul>
<li><span data-ttu-id="98e6e-245">Bearbeiten (Scroll-Muster)</span><span class="sxs-lookup"><span data-stu-id="98e6e-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="98e6e-246">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98e6e-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="98e6e-247">**Licher**</span><span class="sxs-lookup"><span data-stu-id="98e6e-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98e6e-248">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="98e6e-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="98e6e-249">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="98e6e-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




