---
title: Button-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Button-Steuerelement-Typ.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Button-Steuerelement Typen
- UI-Automatisierung, Struktur für Schaltflächen-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Button-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Button-Steuerelement Typen
- UI-Automatisierung, Ereignisse für Button-Steuerelement Typen
- Struktur Strukturen, Schaltflächen-Steuerelement Typen
- Eigenschaften, Schaltflächen-Steuerelement Typen
- Steuerelement Muster, Button-Steuerelement Typen
- Ereignisse, Button-Steuerelement Typen
- Unterstützung für Button-Steuerelement Typen
- Button-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Schaltflächen-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Button-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Schaltfläche
- Steuerelement Typen, Schaltfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207440"
---
# <a name="button-control-type"></a><span data-ttu-id="9f54f-119">Button-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="9f54f-119">Button Control Type</span></span>

<span data-ttu-id="9f54f-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Button** -Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="9f54f-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="9f54f-121">Eine Schaltfläche ist ein Objekt, das ein Benutzer dazu verwendet, eine Aktion auszuführen, z. B. die Schaltflächen OK und Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9f54f-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="9f54f-122">Das Schaltflächen-Steuerelement ist hinsichtlich des Verfügbarmachens ein einfaches Steuerelement, weil es einem einzelnen Befehl zugeordnet ist, den der Benutzer ausführen möchte.</span><span class="sxs-lookup"><span data-stu-id="9f54f-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="9f54f-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Button** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="9f54f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="9f54f-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schaltflächen-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="9f54f-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9f54f-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9f54f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9f54f-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9f54f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9f54f-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f54f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9f54f-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9f54f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9f54f-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9f54f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9f54f-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f54f-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9f54f-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9f54f-131">Typical Tree Structure</span></span>

<span data-ttu-id="9f54f-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Schaltflächen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f54f-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9f54f-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9f54f-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f54f-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="9f54f-134">Control View</span></span></th>
<th><span data-ttu-id="9f54f-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="9f54f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9f54f-136">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9f54f-136">Button</span></span>
<ul>
<li><span data-ttu-id="9f54f-137">Bild (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="9f54f-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="9f54f-138">Text (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="9f54f-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9f54f-139">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9f54f-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="9f54f-140">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f54f-140">Relevant Properties</span></span>

<span data-ttu-id="9f54f-141">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für **die Steuerelemente, die den** Steuerelement-Steuerelement Typen (z. b. Schaltflächen-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9f54f-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="9f54f-142">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9f54f-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9f54f-143">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f54f-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9f54f-144">Wert</span><span class="sxs-lookup"><span data-stu-id="9f54f-144">Value</span></span>      | <span data-ttu-id="9f54f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f54f-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f54f-146">**UIA \_ acceleratorkeypropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9f54f-147">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-147">See notes.</span></span> | <span data-ttu-id="9f54f-148">Ein Schaltflächen-Steuerelement unterstützt in der Regel eine Zugriffstaste, damit der Endbenutzer die durch die Schaltfläche auf der Tastatur dargestellte Aktion schnell ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9f54f-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="9f54f-149">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9f54f-150">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-150">See notes.</span></span> | <span data-ttu-id="9f54f-151">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9f54f-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="9f54f-152">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9f54f-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-153">See notes.</span></span> | <span data-ttu-id="9f54f-154">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="9f54f-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="9f54f-155">**UIA \_ clickablepointpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9f54f-156">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-156">See notes.</span></span> | <span data-ttu-id="9f54f-157">Unterstützt, wenn es ein umschließendes Rechteck gibt.</span><span class="sxs-lookup"><span data-stu-id="9f54f-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9f54f-158">Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="9f54f-159">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9f54f-160">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="9f54f-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="9f54f-161">**UIA \_ helptextpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="9f54f-162">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-162">See notes.</span></span> | <span data-ttu-id="9f54f-163">Der Hilfetext sollte angeben, wie das Endergebnis der Schaltfläche aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9f54f-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="9f54f-164">Dabei handelt es sich in der Regel um dieselben Informationen, die über eine QuickInfo angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f54f-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="9f54f-165">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9f54f-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f54f-166">TRUE</span></span>       | <span data-ttu-id="9f54f-167">Das Schaltflächen-Steuerelement muss immer ein Inhalt sein.</span><span class="sxs-lookup"><span data-stu-id="9f54f-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="9f54f-168">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9f54f-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f54f-169">TRUE</span></span>       | <span data-ttu-id="9f54f-170">Das Schaltflächen-Steuerelement muss immer ein Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="9f54f-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="9f54f-171">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9f54f-172">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-172">See notes.</span></span> | <span data-ttu-id="9f54f-173">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="9f54f-174">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9f54f-175">Null</span><span class="sxs-lookup"><span data-stu-id="9f54f-175">Null</span></span>       | <span data-ttu-id="9f54f-176">Schaltflächen-Steuerelemente werden durch ihren Inhalt selbstbeschriftet.</span><span class="sxs-lookup"><span data-stu-id="9f54f-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="9f54f-177">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9f54f-178">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-178">See notes.</span></span> | <span data-ttu-id="9f54f-179">Lokalisierte Zeichenfolge, die dem **Button** -Steuerelement Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="9f54f-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="9f54f-180">Der Standardwert ist "Button" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="9f54f-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="9f54f-181">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9f54f-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9f54f-182">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-182">See notes.</span></span> | <span data-ttu-id="9f54f-183">Der Name des Schaltflächen-Steuer Elements ist der Text, der für die Bezeichnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f54f-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="9f54f-184">Wenn ein Bild zum Bezeichnen einer Schaltfläche verwendet wird, muss für die **Name** -Eigenschaft der Schaltfläche alternativer Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f54f-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9f54f-185">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9f54f-185">Required Control Patterns</span></span>

<span data-ttu-id="9f54f-186">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Schaltflächen-Steuerelementen unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f54f-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="9f54f-187">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9f54f-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9f54f-188">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f54f-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="9f54f-189">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="9f54f-189">Support/Value</span></span> | <span data-ttu-id="9f54f-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f54f-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f54f-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9f54f-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9f54f-192">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-192">See notes.</span></span>    | <span data-ttu-id="9f54f-193">Wenn eine Schaltfläche als untergeordnetes Element einer unterteilten Schaltfläche gehostet wird, kann die untergeordnete Schaltfläche das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster anstelle des [Aufruf](uiauto-implementinginvoke.md) -oder [Toggle](uiauto-implementingtoggle.md) -Steuerelement Musters unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="9f54f-194">Das ExpandCollapse-Steuerelement Muster kann zum Öffnen oder Schließen eines Menüs oder einer anderen Unterstruktur verwendet werden, die dem Schaltflächen Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f54f-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="9f54f-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="9f54f-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="9f54f-196">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-196">See notes.</span></span>    | <span data-ttu-id="9f54f-197">Alle Schaltflächen sollten das Steuerelement "Start" oder das [Toggle](uiauto-implementingtoggle.md) [-Steuerelement](uiauto-implementinginvoke.md) Muster unterstützen, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="9f54f-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="9f54f-198">Das Aufruf Steuerelement-Muster muss unterstützt werden, wenn die Schaltfläche einen Befehl bei der Anforderung des Benutzers ausführt.</span><span class="sxs-lookup"><span data-stu-id="9f54f-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="9f54f-199">Dieser Befehl ist einem einzelnen Vorgang zugeordnet, etwa Ausschneiden, Kopieren, Einfügen oder Löschen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="9f54f-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="9f54f-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="9f54f-201">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9f54f-201">See notes.</span></span>    | <span data-ttu-id="9f54f-202">Alle Schaltflächen sollten das Steuerelement "Start" oder das [Toggle](uiauto-implementingtoggle.md) [-Steuerelement](uiauto-implementinginvoke.md) Muster unterstützen, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="9f54f-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="9f54f-203">Das Toggle-Steuerelement Muster muss unterstützt werden, wenn die Schaltfläche eine Reihe von bis zu drei Zuständen durchlaufen kann.</span><span class="sxs-lookup"><span data-stu-id="9f54f-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="9f54f-204">In der Regel ist dies als Ein-/Ausschalter für bestimmte Features zu sehen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="9f54f-205">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9f54f-205">Required Events</span></span>

<span data-ttu-id="9f54f-206">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Schaltflächen-</span><span class="sxs-lookup"><span data-stu-id="9f54f-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="9f54f-207">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9f54f-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9f54f-208">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="9f54f-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="9f54f-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f54f-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f54f-210">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="9f54f-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="9f54f-211">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9f54f-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="9f54f-212">**UIA \_ aufrufen \_ invokedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="9f54f-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="9f54f-213">Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="9f54f-214">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9f54f-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="9f54f-215">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="9f54f-216">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9f54f-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="9f54f-217">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="9f54f-218">[**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9f54f-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="9f54f-219">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="9f54f-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="9f54f-220">[**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9f54f-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="9f54f-221">Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f54f-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="9f54f-222">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f54f-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9f54f-223">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9f54f-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f54f-224">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9f54f-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9f54f-225">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9f54f-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




