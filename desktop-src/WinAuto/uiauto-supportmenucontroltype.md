---
title: Menu-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Menü Steuerungstyp.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Menü Steuerungstyp
- Benutzeroberflächen Automatisierung, Menü Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Baumstruktur für Menü Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Eigenschaften für den Menü Steuerungstyp
- UI-Automatisierung, Steuerelement Muster für den Menü Steuerungstyp
- Benutzeroberflächenautomatisierungs, Ereignisse für den Menü Steuerungstyp
- Struktur Strukturen, Menü Steuerelement-Typ
- Eigenschaften, Menü Steuerelement-Typ
- Steuerelement Muster, Menü Steuerelement-Typ
- Ereignisse, Menü Steuerelement-Typ
- Unterstützung für den Menü Steuerungstyp
- Menü-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Menü Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für Menu-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Menü
- Steuerelement Typen, Menü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036854"
---
# <a name="menu-control-type"></a><span data-ttu-id="ed68e-119">Menu-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="ed68e-119">Menu Control Type</span></span>

<span data-ttu-id="ed68e-120">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Menü** Steuerungstyp.</span><span class="sxs-lookup"><span data-stu-id="ed68e-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="ed68e-121">Ein Menüsteuerelement ermöglicht die hierarchische Organisation von Elementen, die Befehlen und Ereignishandlern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ed68e-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="ed68e-122">In einer typischen Microsoft Windows-Anwendung enthält eine Menüleiste mehrere Menü Schaltflächen (z. b. **Datei**, **Bearbeiten** und **Fenster**), und jede Menü Schaltfläche zeigt ein Menü an.</span><span class="sxs-lookup"><span data-stu-id="ed68e-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="ed68e-123">Ein Menü enthält eine Sammlung von Menüelementen (z. B. **Neu**, **Öffnen** und **Schließen**), die erweitert werden können, um weitere Menüelemente anzuzeigen, oder auf die geklickt werden kann, um eine bestimmte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ed68e-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="ed68e-124">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Menü** Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ed68e-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="ed68e-125">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Menü Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und</span><span class="sxs-lookup"><span data-stu-id="ed68e-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ed68e-126">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ed68e-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ed68e-127">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ed68e-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ed68e-128">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed68e-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ed68e-129">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ed68e-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ed68e-130">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ed68e-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ed68e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed68e-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ed68e-132">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="ed68e-132">Typical Tree Structure</span></span>

<span data-ttu-id="ed68e-133">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Menü Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed68e-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ed68e-134">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ed68e-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed68e-135">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="ed68e-135">Control View</span></span></th>
<th><span data-ttu-id="ed68e-136">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="ed68e-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ed68e-137">Menü</span><span class="sxs-lookup"><span data-stu-id="ed68e-137">Menu</span></span>
<ul>
<li><span data-ttu-id="ed68e-138">MenuItem (1 oder viele)</span><span class="sxs-lookup"><span data-stu-id="ed68e-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="ed68e-139">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="ed68e-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ed68e-140">Menü</span><span class="sxs-lookup"><span data-stu-id="ed68e-140">Menu</span></span>
<ul>
<li><span data-ttu-id="ed68e-141">MenuItem (1 oder viele)</span><span class="sxs-lookup"><span data-stu-id="ed68e-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="ed68e-142">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="ed68e-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ed68e-143">Menü Steuerelemente werden immer in der Steuerelement Ansicht und in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed68e-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="ed68e-144">Menü Steuerelemente sollten unter dem Steuerelement angezeigt werden, auf das Ihre Informationen verweisen.</span><span class="sxs-lookup"><span data-stu-id="ed68e-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="ed68e-145">Benutzeroberflächenautomatisierungs-Clients können auf [**UIA \_ menuopenedeventid**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass Sie ständig von Menü Steuerelementen übermittelte Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed68e-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="ed68e-146">Kontextmenü-Steuerelemente sind ein besonderer Fall.</span><span class="sxs-lookup"><span data-stu-id="ed68e-146">Context menu controls are a special case.</span></span> <span data-ttu-id="ed68e-147">Sie können als untergeordnete Elemente des Desktops oder eines Anwendungsfensters der obersten Ebene angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed68e-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="ed68e-148">Ein Menü Steuerelement kann in seiner Struktur andere Steuerelemente enthalten, z. b. Bearbeitungs Steuerelemente und Kombinations Felder.</span><span class="sxs-lookup"><span data-stu-id="ed68e-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="ed68e-149">Diese zusätzlichen Steuerelemente entsprechen den "anderen Steuerelementen", die in der vorherigen Tabelle in der Steuerelement-und der Inhaltsansicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed68e-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ed68e-150">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed68e-150">Relevant Properties</span></span>

<span data-ttu-id="ed68e-151">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **Menü** Steuerelement-Typ besonders relevant ist.</span><span class="sxs-lookup"><span data-stu-id="ed68e-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="ed68e-152">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ed68e-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ed68e-153">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ed68e-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="ed68e-154">Wert</span><span class="sxs-lookup"><span data-stu-id="ed68e-154">Value</span></span>      | <span data-ttu-id="ed68e-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed68e-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed68e-156">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="ed68e-157">**Menü**</span><span class="sxs-lookup"><span data-stu-id="ed68e-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="ed68e-158">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ed68e-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="ed68e-159">TRUE</span></span>       | <span data-ttu-id="ed68e-160">Das Menü Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed68e-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="ed68e-161">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ed68e-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="ed68e-162">TRUE</span></span>       | <span data-ttu-id="ed68e-163">Das Menü Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed68e-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="ed68e-164">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="ed68e-165">NULL</span><span class="sxs-lookup"><span data-stu-id="ed68e-165">NULL</span></span>       | <span data-ttu-id="ed68e-166">Für ein typisches Menüsteuerelement wird keine Bezeichnung erwartet.</span><span class="sxs-lookup"><span data-stu-id="ed68e-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="ed68e-167">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="ed68e-168">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ed68e-168">See notes.</span></span> | <span data-ttu-id="ed68e-169">Für das Menü Steuerelement muss keine **Name** -Eigenschaft festgelegt werden, oder es kann derselbe Name wie das zugeordnete Steuerelement sein, z. b. ein Menü Element, das das Untermenü geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="ed68e-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ed68e-170">Erforderliche Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="ed68e-170">Required Control Patterns</span></span>

<span data-ttu-id="ed68e-171">Für den Menu-Steuerelementtyp gibt es keine erforderlichen Steuerelementmuster.</span><span class="sxs-lookup"><span data-stu-id="ed68e-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="ed68e-172">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ed68e-172">Required Events</span></span>

<span data-ttu-id="ed68e-173">Menü Steuerelemente müssen das [**UIA \_ menuopenedeventid-**](uiauto-event-ids.md) Ereignis erhöhen, wenn Sie auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed68e-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="ed68e-174">Das **UIA \_ menuopenedeventid-** Ereignis enthält den Text des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ed68e-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="ed68e-175">Das [**UIA \_ menuclosedebug-**](uiauto-event-ids.md) Ereignis muss ausgelöst werden, wenn ein Menü auf dem Bildschirm ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed68e-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="ed68e-176">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Menü Steuerelementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ed68e-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="ed68e-177">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ed68e-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ed68e-178">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="ed68e-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ed68e-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed68e-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed68e-180">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="ed68e-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ed68e-181">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ed68e-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ed68e-182">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ed68e-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ed68e-183">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed68e-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ed68e-184">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ed68e-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ed68e-185">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed68e-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="ed68e-186">**UIA \_ menuclosedebug**</span><span class="sxs-lookup"><span data-stu-id="ed68e-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="ed68e-187">**UIA \_ menuopenedeventid**</span><span class="sxs-lookup"><span data-stu-id="ed68e-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="ed68e-188">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="ed68e-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ed68e-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed68e-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ed68e-190">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ed68e-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ed68e-191">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ed68e-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ed68e-192">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ed68e-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




