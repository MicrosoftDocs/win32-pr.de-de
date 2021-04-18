---
title: SelectionItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ISelectionItemProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des SelectionItem-Steuerelement Musters
- UI-Automatisierung, SelectionItem-Steuerelement Muster
- Benutzeroberflächenautomatisierung, ISelectionItemProvider
- ISelectionItemProvider
- Implementieren von SelectionItem-Steuerelement Mustern für Benutzeroberflächen
- SelectionItem-Steuerelement Muster
- Steuerelement Muster, ISelectionItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-SelectionItem
- Steuerelement Muster, SelectionItem
- Schnittstellen, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340816"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="05723-113">SelectionItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="05723-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="05723-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="05723-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="05723-115">Das **SelectionItem** -Steuerelement Muster dient zur Unterstützung von Steuerelementen, die als einzelne, auswählbare untergeordnete Elemente von Container Steuerelementen fungieren, die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="05723-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="05723-116">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="05723-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="05723-117">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="05723-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="05723-118">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="05723-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="05723-119">Erforderliche Member für **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="05723-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="05723-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05723-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="05723-121">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="05723-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="05723-122">Beachten Sie beim Implementieren des **SelectionItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="05723-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="05723-123">Steuerelemente mit einfacher Auswahl, die untergeordnete Steuerelemente verwalten, die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)implementieren, wie z. b. der Schieberegler **Bildschirmauflösung** im Dialogfeld **Anzeigeeigenschaften** für Windows, sollten [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); implementieren. die untergeordneten Elemente sollten sowohl " [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) " als auch " [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)" implementieren.</span><span class="sxs-lookup"><span data-stu-id="05723-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="05723-124">Erforderliche Member für **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="05723-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="05723-125">Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="05723-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="05723-126">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="05723-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="05723-127">Memberart</span><span class="sxs-lookup"><span data-stu-id="05723-127">Member type</span></span> | <span data-ttu-id="05723-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05723-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="05723-129">**Addzu Selection**</span><span class="sxs-lookup"><span data-stu-id="05723-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="05723-130">Methode</span><span class="sxs-lookup"><span data-stu-id="05723-130">Method</span></span>      | <span data-ttu-id="05723-131">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-131">None</span></span>  |
| [<span data-ttu-id="05723-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="05723-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="05723-133">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05723-133">Property</span></span>    | <span data-ttu-id="05723-134">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-134">None</span></span>  |
| [<span data-ttu-id="05723-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="05723-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="05723-136">Methode</span><span class="sxs-lookup"><span data-stu-id="05723-136">Method</span></span>      | <span data-ttu-id="05723-137">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-137">None</span></span>  |
| [<span data-ttu-id="05723-138">**Select**</span><span class="sxs-lookup"><span data-stu-id="05723-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="05723-139">Methode</span><span class="sxs-lookup"><span data-stu-id="05723-139">Method</span></span>      | <span data-ttu-id="05723-140">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-140">None</span></span>  |
| [<span data-ttu-id="05723-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="05723-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="05723-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05723-142">Property</span></span>    | <span data-ttu-id="05723-143">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-143">None</span></span>  |
| [<span data-ttu-id="05723-144">**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**</span><span class="sxs-lookup"><span data-stu-id="05723-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="05723-145">Ereignis</span><span class="sxs-lookup"><span data-stu-id="05723-145">Event</span></span>       | <span data-ttu-id="05723-146">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-146">None</span></span>  |
| [<span data-ttu-id="05723-147">**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**</span><span class="sxs-lookup"><span data-stu-id="05723-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="05723-148">Ereignis</span><span class="sxs-lookup"><span data-stu-id="05723-148">Event</span></span>       | <span data-ttu-id="05723-149">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-149">None</span></span>  |
| [<span data-ttu-id="05723-150">**UIA \_ SelectionItem \_ elementselectedebug**</span><span class="sxs-lookup"><span data-stu-id="05723-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="05723-151">Ereignis</span><span class="sxs-lookup"><span data-stu-id="05723-151">Event</span></span>       | <span data-ttu-id="05723-152">Keine</span><span class="sxs-lookup"><span data-stu-id="05723-152">None</span></span>  |



 

<span data-ttu-id="05723-153">Wenn das Ergebnis einer [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)-, [**addabselection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)-oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) -Option ein einzelnes ausgewähltes Element ist, ein **Element selected** -Ereignis ([**UIA \_ SelectionItem \_ elementselectedeventid**](uiauto-event-ids.md)) sollte ausgelöst werden. andernfalls werden die Ereignisse **elementaddeddeselection** ([**UIA \_ SelectionItem \_ elementaddeddeselectioneventid**](uiauto-event-ids.md)) oder **elementremovedfromselection** ([**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)) nach Bedarf ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="05723-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05723-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05723-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05723-155">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="05723-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="05723-156">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="05723-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="05723-157">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="05723-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




