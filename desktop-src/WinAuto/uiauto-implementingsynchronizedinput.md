---
title: SynchronizedInput-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von isynchronizedinputprovider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- UI-Automatisierung, Implementieren des SynchronizedInput-Steuerelement Musters
- Benutzeroberflächenautomatisierungs-, SynchronizedInput-Steuerelement Muster
- UI-Automatisierung, isynchronizedinputprovider
- ISynchronizedInputProvider
- Implementieren von SynchronizedInput-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- SynchronizedInput-Steuerelement Muster
- Steuerelement Muster, isynchronizedinputprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-SynchronizedInput
- Steuerelement Muster, SynchronizedInput
- Schnittstellen, isynchronizedinputprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337177"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="f892c-113">SynchronizedInput-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f892c-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="f892c-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**isynchronizedinputprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="f892c-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="f892c-115">Mit dem **SynchronizedInput** -Steuerelement Muster können Microsoft UI Automation-Client Anwendungen die Maus-oder Tastatureingaben an ein bestimmtes UI-Element weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="f892c-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="f892c-116">Dieses Steuerelement Muster wird in der Regel in automatisierten Test Skripts verwendet, um Maus-oder Tastatureingaben an ein bestimmtes Benutzeroberflächen Element zu senden und dann zu überprüfen, ob das Element die Eingabe empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="f892c-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="f892c-117">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f892c-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f892c-118">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f892c-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f892c-119">Erforderliche Member für **isynchronizedinputprovider**</span><span class="sxs-lookup"><span data-stu-id="f892c-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="f892c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f892c-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f892c-121">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f892c-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f892c-122">Beachten Sie beim Implementieren des **SynchronizedInput** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="f892c-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f892c-123">Wenn die [**isynchronizedinputprovider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) -Methode aufgerufen wird, sollte der Benutzeroberflächenautomatisierungs-Anbieter mit der Überprüfung der Eingabe des angegebenen Typs beginnen und dann eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="f892c-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="f892c-124">Wenn übereinstimmende Eingaben für das Element gefunden werden, sollte der Anbieter das [**UIA-Ereignis " \_ inputreachedtargeteventid**](uiauto-event-ids.md) " erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f892c-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="f892c-125">Wenn übereinstimmende Eingaben gefunden werden, aber ein anderes Element erreicht wurden, sollte der Anbieter das UIA-Ereignis " [**\_ inputreachedotherelementeventid**](uiauto-event-ids.md) " erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f892c-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="f892c-126">Wenn nicht übereinstimmende Eingaben gefunden werden, sollte der Anbieter die Eingabe verwerfen und das UIA-Ereignis " [**\_ inputverwerdebug-**](uiauto-event-ids.md) ID" erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f892c-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="f892c-127">Der Benutzeroberflächenautomatisierungs-Anbieter muss die Eingabe verwerfen, wenn Sie für ein anderes Element als das aktuelle Element gilt.</span><span class="sxs-lookup"><span data-stu-id="f892c-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="f892c-128">Wenn das Element die Eingabe empfängt oder wenn die [**isynchronizedinputprovider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) -Methode aufgerufen wird, beendet der Anbieter die Überprüfung der Eingabe und fährt wie gewohnt fort.</span><span class="sxs-lookup"><span data-stu-id="f892c-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="f892c-129">Wenn [**isynchronizedinputprovider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) aufgerufen wird, wenn der Anbieter bereits Eingaben abhört, sollte der Anbieter [**UIA \_ E \_ InvalidOperation**](uiauto-error-codes.md)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f892c-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="f892c-130">Erforderliche Member für **isynchronizedinputprovider**</span><span class="sxs-lookup"><span data-stu-id="f892c-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="f892c-131">Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**isynchronizedinputprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f892c-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="f892c-132">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="f892c-132">Required members</span></span>                                                                         | <span data-ttu-id="f892c-133">Memberart</span><span class="sxs-lookup"><span data-stu-id="f892c-133">Member type</span></span> | <span data-ttu-id="f892c-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f892c-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f892c-135">**Startüberwachung**</span><span class="sxs-lookup"><span data-stu-id="f892c-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="f892c-136">Methode</span><span class="sxs-lookup"><span data-stu-id="f892c-136">Method</span></span>      | <span data-ttu-id="f892c-137">Keine</span><span class="sxs-lookup"><span data-stu-id="f892c-137">None</span></span>  |
| [<span data-ttu-id="f892c-138">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="f892c-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="f892c-139">Methode</span><span class="sxs-lookup"><span data-stu-id="f892c-139">Method</span></span>      | <span data-ttu-id="f892c-140">Keine</span><span class="sxs-lookup"><span data-stu-id="f892c-140">None</span></span>  |
| [<span data-ttu-id="f892c-141">**UIA \_ inputreachedtargeteventid**</span><span class="sxs-lookup"><span data-stu-id="f892c-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="f892c-142">Ereignis</span><span class="sxs-lookup"><span data-stu-id="f892c-142">Event</span></span>       | <span data-ttu-id="f892c-143">Keine</span><span class="sxs-lookup"><span data-stu-id="f892c-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="f892c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f892c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f892c-145">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="f892c-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




