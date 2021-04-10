---
title: Typ des semanticzoom-Steuer Elements
description: Dieses Thema enthält Informationen zur Benutzeroberflächenautomatisierungs-Unterstützung für den semanticzoom-Steuerelement.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs-Steuerelement (semanticzoom)
- UI-Automatisierung, Baumstruktur für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für semanticzoom-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für semanticzoom-Steuerelement Typen
- Struktur Strukturen, semanticzoom-Steuerelement Typen
- Eigenschaften, semanticzoom-Steuerelement Typen
- Steuerelement Muster, semanticzoom-Steuerelement Typen
- Ereignisse, semanticzoom-Steuerelement Typen
- Unterstützung für semanticzoom-Steuerelement Typen
- Typ des semanticzoom-Steuer Elements
- Steuerelement Typen, Baumstruktur für semanticzoom-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für semanticzoom-Steuerelement Typen
- Steuerelement Typen, Unterstützung für semanticzoom
- Steuerelement Typen, semanticzoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101682"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="e5d23-119">Typ des semanticzoom-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="e5d23-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="e5d23-120">Dieses Thema enthält Informationen zur Benutzeroberflächenautomatisierungs-Unterstützung für den **semanticzoom** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e5d23-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="e5d23-121">Der semantische Zoom ist eine Technik, die in Windows 8 eingeführt wurde, um große Mengen verwandter Daten oder Inhalte in einer einzelnen Ansicht, z. b. ein Foto Album, eine APP-Liste oder ein Adressbuch, darzustellen und zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="e5d23-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="e5d23-122">Der semantische Zoom verwendet zwei verschiedene Modi für die Klassifizierung und Darstellung der Inhalte.</span><span class="sxs-lookup"><span data-stu-id="e5d23-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="e5d23-123">Der Low-Level *(oder vergrößern*)-Modus zeigt Elemente in einer flachen, "gesamten" Struktur an; und der Modus für hohe Ebene (oder *Zoom*) zeigt Elemente in Gruppen an, sodass der Benutzer schnell navigieren und den Inhalt durchsuchen kann.</span><span class="sxs-lookup"><span data-stu-id="e5d23-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="e5d23-124">Beispielsweise kann das Zoomen einer Liste von Städten zu einer Liste von Bundesstaaten wechseln, die diese Städte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5d23-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="e5d23-125">Das Zoomen einer Liste von Programmen kann zu einer Liste logischer Programm Gruppen wechseln.</span><span class="sxs-lookup"><span data-stu-id="e5d23-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="e5d23-126">Weitere Informationen zum semantischen Zoom, der speziell für Windows Store-Apps verwendet wird, finden Sie unter [Richtlinien für den semantischen Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="e5d23-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="e5d23-127">Das Verwendungs Modell des **semanticzoom** -Steuerelement Typs ist insofern ungewöhnlich, als es vor allem für den programmgesteuerten Zugriff vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e5d23-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="e5d23-128">Microsoft UI Automation-Clients können das semantische Zoom Steuerelement überwachen und bearbeiten, um den Zoomzustand der Liste zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e5d23-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="e5d23-129">Benutzer, die keine Hilfstechnologie verwenden, würden das semantische Zoom Steuerelement normalerweise direkt über Touchgesten oder Tastenkombinationen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e5d23-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="e5d23-130">In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **semanticzoom** -Steuerelement Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="e5d23-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="e5d23-131">Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle semantischen Zoom Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="e5d23-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e5d23-132">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e5d23-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e5d23-133">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="e5d23-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e5d23-134">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d23-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e5d23-135">Erforderliche Steuerelement Muster und-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d23-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="e5d23-136">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e5d23-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e5d23-137">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="e5d23-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e5d23-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5d23-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e5d23-139">Typische Baumstruktur</span><span class="sxs-lookup"><span data-stu-id="e5d23-139">Typical Tree Structure</span></span>

<span data-ttu-id="e5d23-140">In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für den **semanticzoom** -Steuerelement Typen sowie die möglichen Inhalte der Ansichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5d23-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="e5d23-141">Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e5d23-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d23-142">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="e5d23-142">Control View</span></span></th>
<th><span data-ttu-id="e5d23-143">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="e5d23-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e5d23-144">List</span><span class="sxs-lookup"><span data-stu-id="e5d23-144">List</span></span>
<ul>
<li><span data-ttu-id="e5d23-145">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="e5d23-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="e5d23-146">ListItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="e5d23-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e5d23-147">List</span><span class="sxs-lookup"><span data-stu-id="e5d23-147">List</span></span>
<ul>
<li><span data-ttu-id="e5d23-148">ListItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="e5d23-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e5d23-149">Oder:</span><span class="sxs-lookup"><span data-stu-id="e5d23-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d23-150">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="e5d23-150">Control View</span></span></th>
<th><span data-ttu-id="e5d23-151">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="e5d23-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e5d23-152">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="e5d23-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="e5d23-153">List</span><span class="sxs-lookup"><span data-stu-id="e5d23-153">List</span></span>
<ul>
<li><span data-ttu-id="e5d23-154">ListItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="e5d23-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e5d23-155">List</span><span class="sxs-lookup"><span data-stu-id="e5d23-155">List</span></span>
<ul>
<li><span data-ttu-id="e5d23-156">ListItem (beliebige Anzahl)</span><span class="sxs-lookup"><span data-stu-id="e5d23-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e5d23-157">Relevante Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d23-157">Relevant Properties</span></span>

<span data-ttu-id="e5d23-158">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente, die den Steuerelement **semanticzoom** implementieren, besonders relevant sind.</span><span class="sxs-lookup"><span data-stu-id="e5d23-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="e5d23-159">Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e5d23-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d23-160">Benutzeroberflächenautomatisierungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5d23-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="e5d23-161">Wert</span><span class="sxs-lookup"><span data-stu-id="e5d23-161">Value</span></span></th>
<th><span data-ttu-id="e5d23-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5d23-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5d23-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-164">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-164">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-165">Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="e5d23-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-167">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-167">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-168">Das äußere Rechteck, das das gesamte Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="e5d23-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-170">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-170">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-171">Wenn das Listen Steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus erhält), muss dieser Punkt durch diese Eigenschaft verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="e5d23-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="e5d23-172">Wenn der Wert der <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> -Eigenschaft <strong>true</strong>ist, führt der Versuch, diese Eigenschaft abzurufen, zu <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> Fehler.</span><span class="sxs-lookup"><span data-stu-id="e5d23-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-176">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5d23-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-178">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5d23-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-180">false</span><span class="sxs-lookup"><span data-stu-id="e5d23-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-182">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-182">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-183">Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e5d23-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-185">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-185">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-186">Eine lokalisierte Zeichenfolge, die dem Typ des <strong>semanticzoom</strong> -Steuer Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="e5d23-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="e5d23-187">Der Standardwert ist der &quot; semantische Zoom &quot; für en-US oder Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="e5d23-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e5d23-188">Einige Frameworks verkettet dies als &quot; semanticzoom &quot; .</span><span class="sxs-lookup"><span data-stu-id="e5d23-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="e5d23-190">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e5d23-190">See notes.</span></span></td>
<td><span data-ttu-id="e5d23-191">Eine leere Zeichenfolge ist zulässig, oder es kann ein hilfreicher Name bereitgestellt werden, solange Sie nicht den Begriff Semantik Zoom enthält, wodurch die Kombination aus Steuerungstyp und-Name verwirrend wäre.</span><span class="sxs-lookup"><span data-stu-id="e5d23-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="e5d23-192">Erforderliche Steuerelement Muster und-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d23-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="e5d23-193">In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Semantik Zoom Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="e5d23-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="e5d23-194">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e5d23-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="e5d23-195">Steuerelementmuster/Mustereigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5d23-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="e5d23-196">Unterstützung/Wert</span><span class="sxs-lookup"><span data-stu-id="e5d23-196">Support/Value</span></span> | <span data-ttu-id="e5d23-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5d23-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5d23-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="e5d23-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="e5d23-199">Depends (Abhängig)</span><span class="sxs-lookup"><span data-stu-id="e5d23-199">Depends</span></span>       | <span data-ttu-id="e5d23-200">Semantik Zoom Steuerelemente unterstützen das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster, um die Aktivierung oder Deaktivierung des Zoom zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="e5d23-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="e5d23-201">Objekt [**Status \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht dem flachen, dem gesamten up-Zustand und dem Wert von " [**degglestate" \_ in**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht der Ansicht "hoch", "Zoomansicht".</span><span class="sxs-lookup"><span data-stu-id="e5d23-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="e5d23-202">Erforderliche Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e5d23-202">Required Events</span></span>

<span data-ttu-id="e5d23-203">In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Semantik Zoom Steuerelementen unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="e5d23-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="e5d23-204">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e5d23-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e5d23-205">Benutzeroberflächen-Automatisierungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="e5d23-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e5d23-206">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5d23-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d23-207">[**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e5d23-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="e5d23-208">[**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e5d23-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e5d23-209">Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e5d23-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="e5d23-210">[**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e5d23-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e5d23-211">Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e5d23-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="e5d23-212">[**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e5d23-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e5d23-213">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5d23-213">Remarks</span></span>

<span data-ttu-id="e5d23-214">Wenn eine Benutzeroberfläche über eine sichtbare Schaltfläche verfügt, um das semantische Zoom Steuerelement Verhalten umzuschalten, sollte diese Schaltfläche keinen **semanticzoom** -Steuer ungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e5d23-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="e5d23-215">Dies ist kontraintuitiv, aber der **semanticzoom** -Steuer ungstyp kennzeichnet den Container des Zoom Inhalts, nicht eine Schaltfläche, die den Zoom steuert.</span><span class="sxs-lookup"><span data-stu-id="e5d23-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="e5d23-216">(Eine solche Schaltfläche könnte einfach als [Button](uiauto-supportbuttoncontroltype.md) -Steuerelement mit dem [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster dargestellt werden.)</span><span class="sxs-lookup"><span data-stu-id="e5d23-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d23-217">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5d23-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d23-218">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="e5d23-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e5d23-219">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="e5d23-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

