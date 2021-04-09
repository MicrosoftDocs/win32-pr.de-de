---
title: Grundlegendes zu Threading Problemen
description: In diesem Thema werden häufige Threading Szenarios für Microsoft Benutzeroberflächenautomatisierungs-Client Implementierungen beschrieben und erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client fälschlicherweise Threading verwendet.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- Clients, Benutzeroberflächenautomatisierungs-Threading Probleme
- Clients, Threading Probleme
- Clients, ereignishandlerthreading-Modell
- Clients, Benutzeroberflächenautomatisierungs-ereignishandlerthreading Modell
- Clients, Benutzeroberflächenautomatisierungs-Affinität
- Clients, Affinität
- Benutzeroberflächenautomatisierungs, Threading Probleme
- UI-Automatisierung, ereignishandlerthreading-Modell
- Benutzeroberflächen Automatisierung, Affinität
- Threadingprobleme
- ereignishandlerthreading-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039043"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="b1d0a-114">Grundlegendes zu Threading Problemen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-114">Understanding Threading Issues</span></span>

<span data-ttu-id="b1d0a-115">In diesem Thema werden häufige Threading Szenarios für Microsoft Benutzeroberflächenautomatisierungs-Client Implementierungen beschrieben und erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client fälschlicherweise Threading verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="b1d0a-116">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b1d0a-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b1d0a-117">Benutzeroberflächen Automatisierung und der UI-Thread</span><span class="sxs-lookup"><span data-stu-id="b1d0a-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="b1d0a-118">Threading Modell für Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="b1d0a-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="b1d0a-119">COM-Apartment Affinität auf 64-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="b1d0a-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="b1d0a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="b1d0a-121">Benutzeroberflächen Automatisierung und der UI-Thread</span><span class="sxs-lookup"><span data-stu-id="b1d0a-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="b1d0a-122">Aufgrund der Art und Weise, wie die Benutzeroberflächen Automatisierung Windows-Meldungen verwendet, können Konflikte auftreten, wenn eine Client Anwendung versucht, mit ihrer eigenen Benutzeroberfläche im UI-Thread zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="b1d0a-123">Diese Konflikte können zu einer sehr langsamen Leistung führen oder sogar dazu führen, dass die Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="b1d0a-124">Wenn Ihre Client Anwendung mit allen Elementen auf dem Desktop interagieren soll, einschließlich der eigenen Benutzeroberfläche, sollten Sie alle Aufrufe der Benutzeroberflächen Automatisierung von einem separaten Thread ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="b1d0a-125">Dies umfasst das Auffinden von Elementen, z. b. durch die Verwendung von [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) oder der [**iuiautomationelement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) -Methode und die Verwendung von Steuerelement Mustern.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="b1d0a-126">Dieser Thread sollte keine Fenster besitzen und sollte ein Component Object Model (com) Multithread-Apartment (MTA)-Modell Thread sein (einer, der com initialisiert, indem er [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ multithreadflag** aufruft).</span><span class="sxs-lookup"><span data-stu-id="b1d0a-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="b1d0a-127">Es ist sicher, Benutzeroberflächenautomatisierungs-Aufrufe in einem Benutzeroberflächenautomatisierungs-Ereignishandler durchzuführen, da der Ereignishandler immer für einen nicht-UI-Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="b1d0a-128">Wenn Sie jedoch Ereignisse abonnieren, die von der Benutzeroberfläche der Client Anwendung stammen können, müssen Sie den Aufruf von [**iuiautomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)oder einer verknüpften Methode in einem nicht-UI-Thread durchführen (der auch ein MTA-Thread sein sollte).</span><span class="sxs-lookup"><span data-stu-id="b1d0a-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="b1d0a-129">Entfernen Sie Ereignishandler im gleichen Thread.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="b1d0a-130">Ein Benutzeroberflächenautomatisierungs-Client sollte nicht mehrere Threads verwenden, um Ereignishandler hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="b1d0a-131">Unerwartetes Verhalten kann auftreten, wenn ein Ereignishandler hinzugefügt oder entfernt wird, während ein anderer in demselben Client Prozess hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="b1d0a-132">Threading Modell für Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="b1d0a-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="b1d0a-133">Ein Benutzeroberflächenautomatisierungs-Client sollte das com MTA-Threading Modell für Threads verwenden, die Ereignishandler implementieren.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="b1d0a-134">Das STA-Modell (Single Thread-Apartment) kann Probleme verursachen, z. b. das Entfernen von Ereignis Handlern durch Clients aus dem Thread.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="b1d0a-135">COM-Apartment Affinität auf 64-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="b1d0a-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="b1d0a-136">Gemäß der com-Spezifikation wird die Lebensdauer eines Remote Objekts von der Lebensdauer des Apartment gesteuert, in dem die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufgerufen wird, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="b1d0a-137">Wenn das Original Apartment heruntergefahren wird, wird auch das Remote Objekt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="b1d0a-138">Für Benutzeroberflächenautomatisierungs-Clients kann dieses com-Verhalten bedeuten, dass die Lebensdauer des von einem 32-Bit-Element verwendeten Remote-32/64-Hilfsprogramms (von UIAutomationCore.dll) von der Lebensdauer des Threads gesteuert wird, der das Element erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="b1d0a-139">Wenn der Benutzeroberflächenautomatisierungs-Client das Element an einen anderen Thread marshundiert, kann das Element ungültig werden, wenn das ursprüngliche Apartment heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="b1d0a-140">Der Benutzeroberflächenautomatisierungs-Client sollte diese Probleme durch Abfangen von Fehlern bei der Verwendung von gemarshallten Automatisierungs Elementen ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="b1d0a-141">Das gleiche Problem kann bei einem 32-Bit-Benutzeroberflächenautomatisierungs-Client auftreten, der 64-Bit-Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="b1d0a-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1d0a-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b1d0a-143">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b1d0a-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d0a-144">Abrufen von Benutzeroberflächenautomatisierungs-Elementen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="b1d0a-145">Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="b1d0a-146">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b1d0a-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="b1d0a-147">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="b1d0a-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d0a-148">Info: Beschreibungen und Funktionsweise von OLE Threading-Modellen</span><span class="sxs-lookup"><span data-stu-id="b1d0a-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 