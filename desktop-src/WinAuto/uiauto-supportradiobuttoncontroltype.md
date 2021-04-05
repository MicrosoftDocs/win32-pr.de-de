---
title: RadioButton-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den RadioButton-Steuer Elementtyp.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für RadioButton-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, RadioButton-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Eigenschaften für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für RadioButton-Steuer Elementtyp
- Struktur Strukturen, RadioButton-Steuer Elementtyp
- Eigenschaften, RadioButton-Steuer Elementtyp
- Steuerelement Muster, RadioButton-Steuer Elementtyp
- Ereignisse, RadioButton-Steuer Elementtyp
- Unterstützung für RadioButton-Steuer Elementtyp
- RadioButton-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für RadioButton-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den RadioButton-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für RadioButton
- Steuerelement Typen, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712702"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="6da54-119">RadioButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6da54-119">RadioButton Control Type</span></span>

<span data-ttu-id="6da54-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **RadioButton** -Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="6da54-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="6da54-121">Ein Optionsfeld besteht aus einer runden Schaltfläche und anwendungsdefiniertem Text (eine Bezeichnung), einem Symbol oder eine Bitmap, die eine Option anzeigt, die der Benutzer durch Aktivieren der Schaltfläche auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="6da54-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="6da54-122">Eine Anwendung verwendet in der Regel Optionsfelder in einem Gruppenfeld, um es dem Benutzer zu gestatten, aus einer Gruppe von verwandten, aber sich gegenseitig ausschließenden Optionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6da54-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="6da54-123">Die Anwendung kann z. B. eine Gruppe von Optionsfeldern darstellen, unter denen der Benutzer eine Formateinstellung für Text auswählen kann, der im Clientbereich markiert ist.</span><span class="sxs-lookup"><span data-stu-id="6da54-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="6da54-124">Der Benutzer kann ein linksbündiges, rechtsbündiges oder zentriertes Format auswählen, indem er das entsprechende Optionsfeld aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6da54-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="6da54-125">In der Regel kann der Benutzer jeweils nur eine Option zur Zeit aus einer Gruppe von Optionsfeldern auswählen.</span><span class="sxs-lookup"><span data-stu-id="6da54-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="6da54-126">Eine weitere Steuerelement Verallgemeinerung für Schaltflächen, bei denen nur eine in einer Gruppe ausgewählt werden kann, ist der Inhalt einer UMSCHALT Fläche.</span><span class="sxs-lookup"><span data-stu-id="6da54-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="6da54-127">Einige Benutzeroberflächen-Frameworks stellen ein Optionsfeld dar, das eine spezielle UMSCHALT Fläche ist.</span><span class="sxs-lookup"><span data-stu-id="6da54-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="6da54-128">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **RadioButton** -Steuer Elementtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="6da54-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="6da54-129">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schaltflächen-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="6da54-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6da54-130">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6da54-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6da54-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="6da54-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6da54-132">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6da54-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6da54-133">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6da54-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6da54-134">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6da54-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6da54-135">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="6da54-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="6da54-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6da54-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6da54-137">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="6da54-137">Typical Tree Structure</span></span>

<span data-ttu-id="6da54-138">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Optionsfeld-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6da54-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6da54-139">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6da54-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6da54-140">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="6da54-140">Control View</span></span></th>
<th><span data-ttu-id="6da54-141">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="6da54-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6da54-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="6da54-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6da54-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="6da54-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6da54-144">Es sind keine untergeordneten Elemente in der Steuerelementansicht oder der Inhaltsansicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="6da54-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="6da54-145">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6da54-145">Relevant Properties</span></span>

<span data-ttu-id="6da54-146">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente besonders relevant ist, die den Steuer Elementtyp " **RadioButton** " implementieren (z. b. Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="6da54-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="6da54-147">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6da54-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6da54-148">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6da54-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6da54-149">Wert</span><span class="sxs-lookup"><span data-stu-id="6da54-149">Value</span></span>           | <span data-ttu-id="6da54-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="6da54-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6da54-151">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6da54-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-152">See notes.</span></span>      | <span data-ttu-id="6da54-153">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="6da54-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="6da54-154">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6da54-155">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-155">See notes.</span></span>      | <span data-ttu-id="6da54-156">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="6da54-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="6da54-157">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6da54-158">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-158">See notes.</span></span>      | <span data-ttu-id="6da54-159">Der durch Klicken aktivierbare Punkt muss ein Punkt sein, der beim Klicken auf das Optionsfeld klickt.</span><span class="sxs-lookup"><span data-stu-id="6da54-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="6da54-160">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6da54-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="6da54-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="6da54-162">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6da54-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="6da54-163">TRUE</span></span>            | <span data-ttu-id="6da54-164">Das Optionsfeld-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="6da54-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="6da54-165">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6da54-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="6da54-166">TRUE</span></span>            | <span data-ttu-id="6da54-167">Das Optionsfeld-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="6da54-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="6da54-168">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6da54-169">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-169">See notes.</span></span>      | <span data-ttu-id="6da54-170">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6da54-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="6da54-171">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6da54-172">NULL</span><span class="sxs-lookup"><span data-stu-id="6da54-172">NULL</span></span>            | <span data-ttu-id="6da54-173">Optionsfeld-Steuerelemente werden durch ihren Inhalt selbst beschriftet.</span><span class="sxs-lookup"><span data-stu-id="6da54-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="6da54-174">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6da54-175">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-175">See notes.</span></span>      | <span data-ttu-id="6da54-176">Lokalisierte Zeichenfolge, die dem **RadioButton** -Steuer Elementtyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="6da54-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="6da54-177">Der Standardwert ist "Optionsfeld" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="6da54-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="6da54-178">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6da54-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6da54-179">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-179">See notes.</span></span>      | <span data-ttu-id="6da54-180">Der Name des Optionsfeld-Steuer Elements ist der Text, der neben der Schaltfläche angezeigt wird, die den Auswahl Zustand beibehält.</span><span class="sxs-lookup"><span data-stu-id="6da54-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6da54-181">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6da54-181">Required Control Patterns</span></span>

<span data-ttu-id="6da54-182">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Optionsfeld-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="6da54-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="6da54-183">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6da54-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6da54-184">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="6da54-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="6da54-185">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="6da54-185">Support/Value</span></span> | <span data-ttu-id="6da54-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="6da54-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6da54-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="6da54-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="6da54-188">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6da54-188">Required</span></span>      | <span data-ttu-id="6da54-189">Alle Optionsfeld-Steuerelemente müssen das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützen, damit die Auswahl aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6da54-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6da54-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="6da54-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="6da54-191">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6da54-191">See notes.</span></span>    | <span data-ttu-id="6da54-192">Die [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) -Eigenschaft muss immer abgeschlossen werden, damit ein Benutzeroberflächenautomatisierungs-Client ermitteln kann, welche anderen Options Felder in einem bestimmten Kontext zueinander zueinander stehen.</span><span class="sxs-lookup"><span data-stu-id="6da54-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="6da54-193">Für die Microsoft Win32-Version des Options Felds wird diese Eigenschaft nicht unterstützt, da es nicht möglich ist, diese Informationen von diesem Legacy Framework abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6da54-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="6da54-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="6da54-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="6da54-195">Nie</span><span class="sxs-lookup"><span data-stu-id="6da54-195">Never</span></span>         | <span data-ttu-id="6da54-196">Das Optionsfeld kann seinen Zustand nicht durchlaufen, nachdem es festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6da54-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="6da54-197">Das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster darf von einem Optionsfeld nie unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6da54-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="6da54-198">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6da54-198">Required Events</span></span>

<span data-ttu-id="6da54-199">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Schaltflächen-</span><span class="sxs-lookup"><span data-stu-id="6da54-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="6da54-200">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6da54-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6da54-201">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="6da54-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="6da54-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="6da54-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6da54-203">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="6da54-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="6da54-204">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6da54-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="6da54-205">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6da54-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="6da54-206">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6da54-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="6da54-207">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6da54-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="6da54-208">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6da54-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="6da54-209">**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**</span><span class="sxs-lookup"><span data-stu-id="6da54-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="6da54-210">Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6da54-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="6da54-211">**UIA \_ SelectionItem \_ elementselectedebug**</span><span class="sxs-lookup"><span data-stu-id="6da54-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="6da54-212">Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6da54-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="6da54-213">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="6da54-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="6da54-214">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6da54-214">Remarks</span></span>

<span data-ttu-id="6da54-215">Ein Optionsfeld stellt eine einzelne auswählbare Option für eine Gruppe von Peer Options Feldern dar.</span><span class="sxs-lookup"><span data-stu-id="6da54-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="6da54-216">Im Idealfall sollten Options Felder über ein Gruppierungs Element verfügen, das die Grenzen der Peer Options Felder verdeutlicht.</span><span class="sxs-lookup"><span data-stu-id="6da54-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="6da54-217">Häufig wird die Grenze jedoch von der Benutzeroberflächen-Elementstruktur impliziert.</span><span class="sxs-lookup"><span data-stu-id="6da54-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="6da54-218">Beispielsweise kann ein Menü eine Reihe von aufeinander folgenden Options Feldern anstelle von Menü Elementen oder eine Reihe von Options Feldern enthalten, die nach einer Gruppen Bezeichnung, aber vor einem handlungsfähigen Element wie Schaltfläche auftreten.</span><span class="sxs-lookup"><span data-stu-id="6da54-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6da54-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6da54-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6da54-220">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6da54-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6da54-221">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6da54-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6da54-222">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6da54-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




