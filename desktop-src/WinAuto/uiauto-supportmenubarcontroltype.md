---
title: MenuBar-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den MenuBar-Steuer Elementtyp.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für MenuBar-Steuer Elementtyp
- UI-Automatisierung, MenuBar-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für den MenuBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den MenuBar-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für den MenuBar-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für den MenuBar-Steuer Elementtyp
- Struktur Strukturen, MenuBar-Steuer Elementtyp
- Eigenschaften, MenuBar-Steuer Elementtyp
- Steuerelement Muster, MenuBar-Steuer Elementtyp
- Ereignisse, MenuBar-Steuer Elementtyp
- Unterstützung für den MenuBar-Steuer Elementtyp
- MenuBar-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für den MenuBar-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den MenuBar-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für Menubar
- Steuerelement Typen, Menüleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337778"
---
# <a name="menubar-control-type"></a><span data-ttu-id="75476-119">MenuBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="75476-119">MenuBar Control Type</span></span>

<span data-ttu-id="75476-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **MenuBar** -Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="75476-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="75476-121">Menüleisten-Steuerelemente sind ein Beispiel für Steuerelemente, die den **MenuBar** -Steuer Elementtyp implementieren.</span><span class="sxs-lookup"><span data-stu-id="75476-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="75476-122">Menüleisten geben dem Benutzer die Möglichkeit, Befehle und Optionen zu aktivieren, die in einer Anwendung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="75476-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="75476-123">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **MenuBar** -Steuer Elementtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="75476-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="75476-124">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Menüleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="75476-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="75476-125">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="75476-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="75476-126">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="75476-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="75476-127">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75476-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="75476-128">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="75476-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="75476-129">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="75476-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="75476-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75476-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="75476-131">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="75476-131">Typical Tree Structure</span></span>

<span data-ttu-id="75476-132">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Menüleisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75476-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="75476-133">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="75476-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75476-134">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="75476-134">Control View</span></span></th>
<th><span data-ttu-id="75476-135">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="75476-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="75476-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="75476-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="75476-137">MenuItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="75476-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="75476-138">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="75476-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="75476-139">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="75476-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="75476-140">MenuItem (1 oder mehr)</span><span class="sxs-lookup"><span data-stu-id="75476-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="75476-141">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="75476-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75476-142">Ein Menüleisten-Steuerelement wird immer in der Steuerelement Ansicht, aber nicht in der Inhaltsansicht angezeigt, weil es in der Regel keine aussagekräftigen Informationen an den Endbenutzer weitergibt (es sei denn, die Anwendung enthält mehr als eine Menüleiste).</span><span class="sxs-lookup"><span data-stu-id="75476-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="75476-143">Benutzeroberflächenautomatisierungs-Clients können das [**UIA \_ menumodestarteventid-**](uiauto-event-ids.md) Ereignis überwachen, um sicherzustellen, dass Sie konsistent benachrichtigt werden, wenn die Benutzeroberfläche in den Menü Modus wechselt</span><span class="sxs-lookup"><span data-stu-id="75476-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="75476-144">Wenn sich die Anwendung im Menü Modus befindet, können alle Tastatureingaben für die Menü Navigation aufgezeichnet werden (z. b. können Sie das Menü **Speichern** aufrufen, anstatt das Zeichen im Anwendungs Client Bereich einzugeben).</span><span class="sxs-lookup"><span data-stu-id="75476-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="75476-145">Das **UIA \_ menumodestarteventid-** Ereignis muss vor dem ersten [**UIA \_ menuopenedeventid-**](uiauto-event-ids.md) Ereignis stehen, um die logische Konsistenz sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="75476-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="75476-146">Das [**UIA \_ menumodeendeventid-**](uiauto-event-ids.md) Ereignis folgt dem letzten [**UIA \_ menuclosedebug-**](uiauto-event-ids.md) Ereignis.</span><span class="sxs-lookup"><span data-stu-id="75476-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="75476-147">Wenn Sie auf ein Menü Element klicken, wird möglicherweise auch sofort das **UIA \_ menumodestarteventid-** Ereignis, gefolgt von einem **UIA \_ menuopenedeventid-** Ereignis, aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="75476-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="75476-148">Ein Menüleisten-Steuerelement kann in seiner Struktur andere Steuerelemente enthalten, z. b. Bearbeitungs Steuerelemente und Kombinations Felder.</span><span class="sxs-lookup"><span data-stu-id="75476-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="75476-149">Diese weiteren Steuerelemente sind oben in der Inhalts- und der Steuerelementansicht mit „Andere Steuerelemente“ gemeint.</span><span class="sxs-lookup"><span data-stu-id="75476-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="75476-150">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75476-150">Relevant Properties</span></span>

<span data-ttu-id="75476-151">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **MenuBar** -Steuer Elementtyp besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="75476-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="75476-152">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="75476-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="75476-153">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="75476-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="75476-154">Wert</span><span class="sxs-lookup"><span data-stu-id="75476-154">Value</span></span>       | <span data-ttu-id="75476-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="75476-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75476-156">**UIA \_ acceleratorkeypropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="75476-157">NULL</span><span class="sxs-lookup"><span data-stu-id="75476-157">NULL</span></span>        | <span data-ttu-id="75476-158">Menüleisten verfügen in der Regel nicht über Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="75476-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="75476-159">**UIA \_ accesskeypropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="75476-160">„ALT“</span><span class="sxs-lookup"><span data-stu-id="75476-160">"ALT"</span></span>       | <span data-ttu-id="75476-161">Durch Drücken der Alt-Taste sollte in der Regel der Fokus auf die Menüleiste innerhalb der Anwendung gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="75476-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="75476-162">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="75476-163">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75476-163">See notes.</span></span>  | <span data-ttu-id="75476-164">Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.</span><span class="sxs-lookup"><span data-stu-id="75476-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="75476-165">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="75476-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="75476-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="75476-167">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="75476-168">false</span><span class="sxs-lookup"><span data-stu-id="75476-168">FALSE</span></span>       | <span data-ttu-id="75476-169">Das Menüleisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="75476-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="75476-170">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="75476-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="75476-171">TRUE</span></span>        | <span data-ttu-id="75476-172">Das Menüleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="75476-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="75476-173">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="75476-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="75476-174">TRUE</span></span>        | <span data-ttu-id="75476-175">Menüleisten-Steuerelemente können den Tastaturfokus erhalten, da die in ihnen enthaltenen Steuerelemente den Tastaturfokus übernehmen können.</span><span class="sxs-lookup"><span data-stu-id="75476-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="75476-176">**UIA \_ isoffscreenpropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="75476-177">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75476-177">See notes.</span></span>  | <span data-ttu-id="75476-178">Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="75476-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="75476-179">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="75476-180">NULL</span><span class="sxs-lookup"><span data-stu-id="75476-180">NULL</span></span>        | <span data-ttu-id="75476-181">Menüleisten-Steuerelemente haben in der Regel keine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="75476-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="75476-182">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="75476-183">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75476-183">See notes.</span></span>  | <span data-ttu-id="75476-184">Lokalisierte Zeichenfolge für den Steuer Elementtyp " **MenuBar** ".</span><span class="sxs-lookup"><span data-stu-id="75476-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="75476-185">Der Standardwert ist "Menüleiste" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="75476-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="75476-186">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="75476-187">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75476-187">See notes.</span></span>  | <span data-ttu-id="75476-188">Das Menüleisten-Steuerelement muss nur dann einen Namen haben, wenn eine Anwendung mehrere Menüleisten hat.</span><span class="sxs-lookup"><span data-stu-id="75476-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="75476-189">Wenn in einer Anwendung mehr als eine Menüleiste vorhanden ist, verwenden Sie diese Eigenschaft, um Unterscheidungs Namen (z. b. "Formatierung" oder "Gliederung") verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="75476-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="75476-190">**UIA- \_ orientationpropertyid**</span><span class="sxs-lookup"><span data-stu-id="75476-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="75476-191">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="75476-191">Depends</span></span>     | <span data-ttu-id="75476-192">Diese Eigenschaft gibt an, ob das Menüleisten-Steuerelement horizontal oder vertikal verläuft.</span><span class="sxs-lookup"><span data-stu-id="75476-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="75476-193">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="75476-193">Required Control Patterns</span></span>

<span data-ttu-id="75476-194">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Menüleisten Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="75476-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="75476-195">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="75476-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="75476-196">Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="75476-196">Control Pattern</span></span>                                                   | <span data-ttu-id="75476-197">Support</span><span class="sxs-lookup"><span data-stu-id="75476-197">Support</span></span> | <span data-ttu-id="75476-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="75476-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75476-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="75476-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="75476-200">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="75476-200">Depends</span></span> | <span data-ttu-id="75476-201">Wenn das Steuerelement erweitert oder reduziert werden kann, muss es das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="75476-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="75476-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="75476-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="75476-203">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="75476-203">Depends</span></span> | <span data-ttu-id="75476-204">Wenn das Steuerelement an verschiedenen Teilen des Bildschirms angedockt werden kann, muss es das [Dock](uiauto-implementingdock.md) -Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="75476-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="75476-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="75476-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="75476-206">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="75476-206">Depends</span></span> | <span data-ttu-id="75476-207">Wenn die Größe des Steuer Elements geändert, gedreht oder verschoben werden kann, muss es das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="75476-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="75476-208">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="75476-208">Required Events</span></span>

<span data-ttu-id="75476-209">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Menüleisten-Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="75476-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="75476-210">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="75476-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="75476-211">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="75476-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="75476-212">Notizen</span><span class="sxs-lookup"><span data-stu-id="75476-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75476-213">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="75476-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="75476-214">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="75476-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="75476-215">[**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="75476-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="75476-216">Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="75476-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="75476-217">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="75476-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="75476-218">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="75476-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="75476-219">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="75476-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="75476-220">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="75476-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="75476-221">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="75476-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="75476-222">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75476-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="75476-223">**Licher**</span><span class="sxs-lookup"><span data-stu-id="75476-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75476-224">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="75476-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="75476-225">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="75476-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




