---
title: Appbar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den appbar-Steuerelement-Typ.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für appbar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, appbar-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den appbar-Steuerelement
- Steuerelement Muster, appbar-Steuerelement Typen
- Unterstützung für appbar-Steuerelement Typen
- Appbar-Steuerelement Typen
- Steuerelement Typen, appbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473860"
---
# <a name="appbar-control-type"></a><span data-ttu-id="9c708-110">Appbar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="9c708-110">AppBar Control Type</span></span>

<span data-ttu-id="9c708-111">Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **appbar** -Steuerelement-Typ.</span><span class="sxs-lookup"><span data-stu-id="9c708-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="9c708-112">Eine APP-Leiste ist ein Benutzeroberflächen Element, das dem Benutzernavigation, Befehle und Tools präsentiert.</span><span class="sxs-lookup"><span data-stu-id="9c708-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="9c708-113">Für Windows Store-Apps können APP-leisten für Apps durch Drücken von Windows-Taste + Z angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c708-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="9c708-114">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **appbar** -Steuerelement-Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="9c708-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="9c708-115">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9c708-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9c708-116">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9c708-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9c708-117">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c708-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9c708-118">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9c708-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9c708-119">Relevante Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9c708-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="9c708-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c708-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9c708-121">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="9c708-121">Typical Tree Structure</span></span>

<span data-ttu-id="9c708-122">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für **appbar** -Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c708-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9c708-123">**Schaltfläche** ist das gängigste Element innerhalb einer **appbar** , aber andere Steuerelemente, die Aktionen für eine APP aufrufen, sind ebenfalls möglich.</span><span class="sxs-lookup"><span data-stu-id="9c708-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="9c708-124">Eine **appbar** kann auch 0 oder mehr Trennzeichen (**Trenn** Zeichentyp) enthalten, die in der Steuerelement Ansicht als zwischen den anderen Steuerelementen platziert werden.</span><span class="sxs-lookup"><span data-stu-id="9c708-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="9c708-125">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9c708-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c708-126">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="9c708-126">Control View</span></span></th>
<th><span data-ttu-id="9c708-127">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="9c708-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9c708-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="9c708-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="9c708-129">Schaltfläche (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="9c708-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="9c708-130">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="9c708-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c708-131">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9c708-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="9c708-132">Schaltfläche (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="9c708-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="9c708-133">Andere Steuerelemente (0 oder viele)</span><span class="sxs-lookup"><span data-stu-id="9c708-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="9c708-134">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c708-134">Relevant Properties</span></span>

<span data-ttu-id="9c708-135">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente besonders relevant ist, die den **appbar** -Steuerelement Typen implementieren</span><span class="sxs-lookup"><span data-stu-id="9c708-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="9c708-136">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9c708-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9c708-137">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9c708-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9c708-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9c708-138">Value</span></span>      | <span data-ttu-id="9c708-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c708-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c708-140">**UIA \_ automationidpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9c708-141">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c708-141">See notes.</span></span> | <span data-ttu-id="9c708-142">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9c708-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="9c708-143">**UIA \_ boundingrechglepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9c708-144">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c708-144">See notes.</span></span> | <span data-ttu-id="9c708-145">Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.</span><span class="sxs-lookup"><span data-stu-id="9c708-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="9c708-146">**UIA \_ controltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9c708-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="9c708-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="9c708-148">**UIA \_ iscontentelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9c708-149">false</span><span class="sxs-lookup"><span data-stu-id="9c708-149">FALSE</span></span>      | <span data-ttu-id="9c708-150">Ein App-leisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c708-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="9c708-151">**UIA \_ iscontrolelementpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9c708-152">TRUE</span><span class="sxs-lookup"><span data-stu-id="9c708-152">TRUE</span></span>       | <span data-ttu-id="9c708-153">Ein App-leisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c708-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="9c708-154">**UIA \_ iskeyboardfocus ablepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9c708-155">Siehe Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c708-155">See notes</span></span>  | <span data-ttu-id="9c708-156">Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9c708-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="9c708-157">Steuerelemente in der APP-Leiste können in der Regel den Tastaturfokus haben.</span><span class="sxs-lookup"><span data-stu-id="9c708-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="9c708-158">**UIA \_ isoffscreenpropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9c708-159">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c708-159">See notes.</span></span> | <span data-ttu-id="9c708-160">Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c708-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="9c708-161">**UIA \_ labeledbypropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9c708-162">Null</span><span class="sxs-lookup"><span data-stu-id="9c708-162">Null</span></span>       | <span data-ttu-id="9c708-163">Die Steuerelemente der APP-Leiste haben in der Regel keine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="9c708-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="9c708-164">**UIA \_ localizedcontroltypepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9c708-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c708-165">See notes.</span></span> | <span data-ttu-id="9c708-166">Lokalisierte Zeichenfolge, die dem **appbar** -Steuerelement entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c708-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="9c708-167">Der Standardwert ist "App-Leiste" für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="9c708-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="9c708-168">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="9c708-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9c708-169">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c708-169">See notes.</span></span> | <span data-ttu-id="9c708-170">Das Steuerelement der APP-Leiste benötigt keinen Namen, es sei denn, eine Anwendung verfügt über mehr als eine APP-Leiste.</span><span class="sxs-lookup"><span data-stu-id="9c708-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="9c708-171">Wenn in einer Anwendung mehr als eine APP-Leiste vorhanden ist, verwenden Sie diese Eigenschaft, um Unterscheidungs Namen verfügbar zu machen, z. b. "Top" oder "Bottom".</span><span class="sxs-lookup"><span data-stu-id="9c708-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="9c708-172">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9c708-172">Required Events</span></span>

<span data-ttu-id="9c708-173">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von App-Bar-</span><span class="sxs-lookup"><span data-stu-id="9c708-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="9c708-174">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9c708-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9c708-175">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="9c708-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="9c708-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c708-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c708-177">**UIA \_ automationfocuschangedebug-ID**</span><span class="sxs-lookup"><span data-stu-id="9c708-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="9c708-178">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9c708-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="9c708-179">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9c708-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="9c708-180">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9c708-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="9c708-181">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9c708-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="9c708-182">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9c708-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="9c708-183">**UIA \_ structurechangedebug**</span><span class="sxs-lookup"><span data-stu-id="9c708-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="9c708-184">Relevante Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9c708-184">Relevant Events</span></span>

<span data-ttu-id="9c708-185">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Steuerelemente, die den **appbar** -Steuerelement Typen implementieren, jedoch nicht unbedingt erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="9c708-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="9c708-186">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="9c708-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="9c708-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c708-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c708-188">**UIA \_ menuclosedebug**</span><span class="sxs-lookup"><span data-stu-id="9c708-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="9c708-189">Platt Form Implementierungen können dieses Ereignis auslösen, wenn das Steuerelement der APP-Leiste geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9c708-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="9c708-190">**UIA \_ menuopenedeventid**</span><span class="sxs-lookup"><span data-stu-id="9c708-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="9c708-191">Platt Form Implementierungen können dieses Ereignis auslösen, wenn das Steuerelement der APP-Leiste geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9c708-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="9c708-192">**Iuiautomationpropertychangeabventhandler**</span><span class="sxs-lookup"><span data-stu-id="9c708-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="9c708-193">Ereignishandler für geänderte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c708-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9c708-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c708-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9c708-195">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9c708-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c708-196">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9c708-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9c708-197">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9c708-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="9c708-198">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9c708-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c708-199">**Appbar-XAML-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="9c708-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="9c708-200">[**Winjs. UI. appbar-Objekt**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9c708-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 