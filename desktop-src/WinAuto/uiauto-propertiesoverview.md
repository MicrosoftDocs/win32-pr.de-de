---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften
description: Microsoft UI Automation-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierungs-Elemente verfügbar. Eigenschaften ermöglichen Client Anwendungen das Abrufen von Informationen zu Steuerelementen.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Benutzeroberflächenautomatisierungs, Übersicht über Eigenschaften
- Benutzeroberflächen Automatisierung, Eigenschaften und Ereignisse
- UI-Automatisierung, Ereignisse und Eigenschaften
- Eigenschaften, Informationen zu
- Eigenschaften, Bezeichner
- Eigenschaften, Werte
- Eigenschaften, Ereignisse
- Ereignisse, Eigenschaften
- Eigenschaften, dynamisch
- Dynamische Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206192"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="dc476-114">Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc476-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="dc476-115">Microsoft UI Automation-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierungs-Elemente verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc476-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="dc476-116">Eigenschaften ermöglichen Client Anwendungen das Abrufen von Informationen zu Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="dc476-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="dc476-117">Die Benutzeroberflächen Automatisierung bietet zwei verschiedene Arten von Eigenschaften: *Automatisierungs Element Eigenschaften* und *Steuerelement Muster* Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc476-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="dc476-118">Die Automatisierungs Element Eigenschaften bestehen aus einem gemeinsamen Satz von Eigenschaften, z. b. "Name", "AcceleratorKey" und "ClassName", die unabhängig vom Steuer Elementtyp von allen Benutzeroberflächenautomatisierungs-Elementen verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="dc476-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="dc476-119">Die meisten Automatisierungs Element Eigenschaften sind statische Werte.</span><span class="sxs-lookup"><span data-stu-id="dc476-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="dc476-120">Steuerelement Muster Eigenschaften sind solche, die von einem Steuerelement verfügbar gemacht werden, das ein bestimmtes Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc476-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="dc476-121">Jedes Steuerelement Muster verfügt über einen entsprechenden Satz von Steuerelement Mustern-Eigenschaften, die das Steuerelement verfügbar machen muss.</span><span class="sxs-lookup"><span data-stu-id="dc476-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="dc476-122">Ein Steuerelement, das das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster unterstützt, macht z. b. die Eigenschaften ColumnCount und RowCount verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc476-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="dc476-123">Die meisten Steuerelement Muster Eigenschaften sind dynamische Werte.</span><span class="sxs-lookup"><span data-stu-id="dc476-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="dc476-124">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dc476-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dc476-125">Eigenschaftsbezeichner</span><span class="sxs-lookup"><span data-stu-id="dc476-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="dc476-126">Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="dc476-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="dc476-127">Eigenschaften und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dc476-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="dc476-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc476-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="dc476-129">Eigenschaftsbezeichner</span><span class="sxs-lookup"><span data-stu-id="dc476-129">Property Identifiers</span></span>

<span data-ttu-id="dc476-130">Jede Eigenschaft wird durch einen numerischen **PropertyId** -Wert identifiziert, der als *Eigenschaften Bezeichner* (ID) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="dc476-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="dc476-131">Anbieter und Clients verwenden die numerischen IDs in Methoden aufrufen wie [**irawelementprovideradviseevents:: adviseeventadded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) und [**iuiautomationelement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) , um Eigenschafts Anforderungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dc476-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="dc476-132">Eine ausführliche Beschreibung der einzelnen Eigenschaften Bezeichner für die Benutzeroberflächen Automatisierung, einschließlich des Datentyps und des Standardwerts der einzelnen Eigenschaften, finden Sie unter [Eigenschaften](uiauto-entry-propids.md)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dc476-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="dc476-133">Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="dc476-133">Property Values</span></span>

<span data-ttu-id="dc476-134">Alle Eigenschaften sind schreibgeschützt, auch wenn einige geändert werden können, indem Sie Methoden verwenden, die auf das Steuerelement reagieren, wie z. b. [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) oder [**iuiautomationdockpattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).</span><span class="sxs-lookup"><span data-stu-id="dc476-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="dc476-135">Weitere Informationen zum Abrufen von Eigenschafts Werten finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="dc476-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="dc476-136">Eigenschaften und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dc476-136">Properties and Events</span></span>

<span data-ttu-id="dc476-137">Die Eigenschaften in der Benutzeroberflächen Automatisierung sind eng mit den Eigenschaften für *geänderte Ereignisse* verknüpft.</span><span class="sxs-lookup"><span data-stu-id="dc476-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="dc476-138">Bei dynamischen Eigenschaften muss eine Client Anwendung wissen, dass sich ein Eigenschafts Wert geändert hat, damit er den Informations Cache aktualisieren oder auf andere Weise auf die neuen Informationen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="dc476-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="dc476-139">Clients können sich registrieren, um auf Eigenschaften geänderte Ereignisse für jede Eigenschaft zu lauschen.</span><span class="sxs-lookup"><span data-stu-id="dc476-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="dc476-140">Anbieter rufen Ereignisse auf, wenn etwas in der Benutzeroberfläche geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dc476-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="dc476-141">Wenn beispielsweise ein Kontrollkästchen aktiviert oder deaktiviert ist, wird ein Eigenschaften Änderungs Ereignis von der Anbieter Implementierung des [Toggle](uiauto-implementingtoggle.md) -Steuerelement Musters ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc476-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="dc476-142">Anbieter können abhängig davon, ob Clients Ereignissen oder bestimmten Ereignissen lauschen, selektiv Ereignisse auslösen.</span><span class="sxs-lookup"><span data-stu-id="dc476-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="dc476-143">Es werden nicht für alle Eigenschaftenänderung Ereignisse ausgelöst. Dies ist vollständig von der Implementierung des Benutzeroberflächenautomatisierungs-Anbieters für das Element abhängig.</span><span class="sxs-lookup"><span data-stu-id="dc476-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="dc476-144">Beispielsweise wird durch die Standard Proxy Anbieter für Listenfelder nicht ein Eigenschaften Änderungs Ereignis, wenn die Auswahl Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dc476-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="dc476-145">In diesem Fall muss die Anwendung auf das Ereignis lauschen, das ausgelöst wird, wenn die Auswahl geändert wird ([**UIA \_ SelectionItem \_ elementselectedebug-**](uiauto-event-ids.md)ID).</span><span class="sxs-lookup"><span data-stu-id="dc476-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="dc476-146">Clients lauschen auf Ereignisse, indem Sie Sie abonnieren, wie unter Abonnieren von Benutzeroberflächenautomatisierungs- [Ereignissen](uiauto-eventsforclients.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dc476-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="dc476-147">Insbesondere bei Eigenschaften geänderten Ereignissen müssen Clients [**iuiautomationpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) implementieren und die Schnittstelle an [**iuiautomation:: addpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) oder [**iuiautomation:: addpropertychangedeventhandlernativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)übergeben.</span><span class="sxs-lookup"><span data-stu-id="dc476-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc476-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc476-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dc476-149">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="dc476-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc476-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="dc476-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="dc476-151">**Getcurrentpropertyvalueex**</span><span class="sxs-lookup"><span data-stu-id="dc476-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="dc476-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="dc476-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="dc476-153">**Getcachedpropertyvalueex**</span><span class="sxs-lookup"><span data-stu-id="dc476-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="dc476-154">**Licher**</span><span class="sxs-lookup"><span data-stu-id="dc476-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc476-155">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="dc476-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="dc476-156">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="dc476-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="dc476-157">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dc476-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




