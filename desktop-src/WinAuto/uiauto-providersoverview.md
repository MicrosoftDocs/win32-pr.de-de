---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter
description: Dieses Thema bietet einen Überblick darüber, wie Steuerelement Entwickler Benutzeroberflächenautomatisierungs-Anbieter implementieren.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Benutzeroberflächen Automatisierung, Übersicht über Anbieter
- Benutzeroberflächenautomatisierungs, Anbieter Typen
- Benutzeroberflächenautomatisierungs, Anbieter Konzepte
- Anbieter, Informationen zu
- Anbieter, Typen
- Anbieter, Konzepte
- Anbieter, Elemente
- Anbieter, Navigation
- Anbieter, Ansichten
- Anbieter, Frameworks
- Anbieter, Fragmente
- Anbieter, Hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947599"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="8b065-115">Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b065-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="8b065-116">Ein Microsoft-Benutzeroberflächenautomatisierungs-Anbieter ist ein Software Objekt, das ein Element der Benutzeroberfläche einer Anwendung verfügbar macht, damit Client Anwendungen für die Barrierefreiheit Informationen über das Element abrufen und seine Funktionalität aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="8b065-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="8b065-117">Im allgemeinen verfügt jedes Steuerelement oder ein anderes unterschiedliches Element in einer Benutzeroberfläche über einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="8b065-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="8b065-118">Microsoft umfasst einen Anbieter für alle Standard Steuerelemente, die mit Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b065-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="8b065-119">Dies bedeutet, dass die Standard Steuerelemente automatisch für Benutzeroberflächenautomatisierungs-Clients verfügbar gemacht werden. Sie müssen keine Barrierefreiheits Schnittstellen für die Standard Steuerelemente implementieren.</span><span class="sxs-lookup"><span data-stu-id="8b065-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="8b065-120">Wenn Ihre Anwendung benutzerdefinierte Steuerelemente enthält, müssen Sie Benutzeroberflächenautomatisierungs-Anbieter für diese Steuerelemente implementieren, um Sie für Client Anwendungen für Barrierefreiheit zugänglich zu machen.</span><span class="sxs-lookup"><span data-stu-id="8b065-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="8b065-121">Außerdem müssen Sie Anbieter für alle Steuerelemente von Drittanbietern implementieren, die keinen Anbieter enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b065-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="8b065-122">Sie implementieren einen Anbieter durch Implementierung von Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen und Steuerelement Muster-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="8b065-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="8b065-123">Dieses Thema bietet einen Überblick darüber, wie Steuerelement Entwickler Benutzeroberflächenautomatisierungs-Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8b065-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="8b065-124">Dies umfasst die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="8b065-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="8b065-125">Anbietertypen</span><span class="sxs-lookup"><span data-stu-id="8b065-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="8b065-126">Konzepte für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b065-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="8b065-127">Elemente</span><span class="sxs-lookup"><span data-stu-id="8b065-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="8b065-128">Frameworks</span><span class="sxs-lookup"><span data-stu-id="8b065-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="8b065-129">Fragmente</span><span class="sxs-lookup"><span data-stu-id="8b065-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="8b065-130">Hosts</span><span class="sxs-lookup"><span data-stu-id="8b065-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="8b065-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b065-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="8b065-132">Anbietertypen</span><span class="sxs-lookup"><span data-stu-id="8b065-132">Types of Providers</span></span>

<span data-ttu-id="8b065-133">Benutzeroberflächenautomatisierungs-Anbieter werden in zwei Kategorien unterteilt: serverseitige Anbieter und Client seitige (oder *Proxy*-) Anbieter.</span><span class="sxs-lookup"><span data-stu-id="8b065-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="8b065-134">Ein serverseitiger Anbieter ist ein Objekt, z. b. ein benutzerdefiniertes Steuerelement, das seine eigene systemeigene Implementierung der relevanten Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen enthält.</span><span class="sxs-lookup"><span data-stu-id="8b065-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="8b065-135">Ein serverseitiger Anbieter kommuniziert mit Client Anwendungen über die Prozess Grenze hinweg, indem er seine Implementierung der Anbieter Schnittstellen dem Benutzeroberflächenautomatisierungs-Kern bereitstellt, der Anforderungen von Clients verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8b065-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="8b065-136">Weitere Informationen zu serverseitigen Anbietern finden Sie unter [Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="8b065-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="8b065-137">Bei einem Client seitigen Anbieter oder Proxy handelt es sich um ein Objekt, das Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen implementiert, wenn ein Steuerelement keine eigene vollständige Anbieter Implementierung enthält.</span><span class="sxs-lookup"><span data-stu-id="8b065-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="8b065-138">Ohne einen Proxy ist ein solches Steuerelement für die Automatisierung der Benutzeroberfläche größtenteils nicht transparent, sodass nur grundlegende Informationen, die über das Fenster Handle (**HWND**) verfügbar sind, bereitgestellt werden können, z. b. die Steuerungs Position</span><span class="sxs-lookup"><span data-stu-id="8b065-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="8b065-139">In der Regel kommunizieren Proxy Anbieter über die Prozess Grenze hinweg mit der Anwendung, indem Sie Windows-Nachrichten senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="8b065-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="8b065-140">Weitere Informationen finden Sie unter [Implementieren eines Client-Side-Benutzeroberflächenautomatisierungs-Anbieters (Proxy)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="8b065-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="8b065-141">Konzepte für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b065-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="8b065-142">Dieser Abschnitt bietet kurze Erläuterungen zu einer Auswahl von Schlüsselkonzepten, die Sie kennen müssen, um Benutzeroberflächenautomatisierungs-Anbieter implementieren zu können.</span><span class="sxs-lookup"><span data-stu-id="8b065-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="8b065-143">Elemente</span><span class="sxs-lookup"><span data-stu-id="8b065-143">Elements</span></span>

<span data-ttu-id="8b065-144">Benutzeroberflächenautomatisierungs-Elemente sind Teile der Benutzeroberfläche – normalerweise Windows oder Steuerelemente –, die für Benutzeroberflächenautomatisierungs-Clients sichtbar sind</span><span class="sxs-lookup"><span data-stu-id="8b065-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="8b065-145">Zu den entsprechenden Beispielen zählen Anwendungsfenster, Bereiche, Schaltflächen, QuickInfos, Listenfelder und Listenelemente.</span><span class="sxs-lookup"><span data-stu-id="8b065-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="8b065-146">Benutzeroberflächenautomatisierungs-Elemente werden für Clients als-Struktur verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="8b065-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="8b065-147">Die Benutzeroberflächen Automatisierung erstellt die Struktur durch Navigieren von einem Element zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="8b065-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="8b065-148">Die Navigation wird vom Anbieter für jedes Element aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b065-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="8b065-149">Jedes Element kann auf sein eigenes übergeordnetes Element, seine gleich geordneten Elemente und die ersten und letzten untergeordneten Elemente verweisen.</span><span class="sxs-lookup"><span data-stu-id="8b065-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="8b065-150">Ein Client kann die Benutzeroberflächenautomatisierungs-Struktur in drei Prinzipal Ansichten sehen, wie in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8b065-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="8b065-151">Sicht</span><span class="sxs-lookup"><span data-stu-id="8b065-151">View</span></span>         | <span data-ttu-id="8b065-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b065-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="8b065-153">Rohdatenansicht</span><span class="sxs-lookup"><span data-stu-id="8b065-153">Raw view</span></span>     | <span data-ttu-id="8b065-154">Schließt alle-Elemente ein.</span><span class="sxs-lookup"><span data-stu-id="8b065-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="8b065-155">Steuerelementansicht</span><span class="sxs-lookup"><span data-stu-id="8b065-155">Control view</span></span> | <span data-ttu-id="8b065-156">Schließt Elemente ein, die Steuerelemente sind.</span><span class="sxs-lookup"><span data-stu-id="8b065-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="8b065-157">Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="8b065-157">Content view</span></span> | <span data-ttu-id="8b065-158">Schließt Steuerelemente ein, die dem Benutzerinformationen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="8b065-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="8b065-159">Für die Definition eines Elements als Inhaltselement oder Steuerelement ist die Anbieterimplementierung zuständig.</span><span class="sxs-lookup"><span data-stu-id="8b065-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="8b065-160">Steuerelemente können auch Inhaltselemente sein, aber alle Inhaltselemente sind auch Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="8b065-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="8b065-161">Weitere Informationen zur Client Ansicht der-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8b065-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="8b065-162">Frameworks</span><span class="sxs-lookup"><span data-stu-id="8b065-162">Frameworks</span></span>

<span data-ttu-id="8b065-163">Ein Framework ist eine Komponente, die untergeordneten Steuerelemente, Treffertests und das Rendering in einem Bereich des Bildschirms verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8b065-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="8b065-164">Beispielsweise kann ein Win32-Fenster, das häufig als **HWND** bezeichnet wird, als Framework fungieren, das mehrere Benutzeroberflächenautomatisierungs-Elemente enthält, z. b. eine Menüleiste, eine Statusleiste und Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="8b065-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="8b065-165">Win32-Container Steuerelemente, wie z. b. Listenfelder und Strukturansicht-Steuerelemente, werden als Frameworks betrachtet, da Sie Ihren eigenen Code zum Rendern von untergeordneten Elementen und zum Ausführen von Treffer Tests enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b065-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="8b065-166">Im Gegensatz dazu ist ein WPF-Listenfeld kein Framework, da Rendering und Treffer Tests vom enthaltenden Fenster behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8b065-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="8b065-167">Die Benutzeroberfläche in einer Anwendung kann aus verschiedenen Frameworks bestehen.</span><span class="sxs-lookup"><span data-stu-id="8b065-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="8b065-168">Beispielsweise kann ein **HWND** in einer Anwendung dynamisches HTML (DHTML) enthalten, das wiederum eine Komponente (z. b. ein Kombinations Feld in einem **HWND**) enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="8b065-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="8b065-169">Fragments</span><span class="sxs-lookup"><span data-stu-id="8b065-169">Fragments</span></span>

<span data-ttu-id="8b065-170">Eine komplette Teilstruktur von Elementen eines bestimmten Frameworks wird als Fragment bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b065-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="8b065-171">Das Element im Stammknoten der Unterstruktur wird als Fragmentstamm bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b065-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="8b065-172">Ein Fragmentstamm besitzt kein übergeordnetes Element, wird aber innerhalb eines anderen Frameworks gehostet, in der Regel in einem Win32-Fenster (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="8b065-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="8b065-173">Hosts</span><span class="sxs-lookup"><span data-stu-id="8b065-173">Hosts</span></span>

<span data-ttu-id="8b065-174">Der Stamm Knoten jedes Fragments muss in einem-Element gehostet werden, in der Regel in einem Win32-Fenster (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="8b065-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="8b065-175">Die Ausnahme stellt der Desktop dar, der in keinem anderen Element gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="8b065-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="8b065-176">Der Host eines benutzerdefinierten Steuer Elements ist das **HWND** des Steuer Elements selbst, nicht das Anwendungsfenster oder ein anderes Fenster, das möglicherweise Gruppen von Steuerelementen der obersten Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="8b065-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="8b065-177">Der Host eines Fragments spielt eine wichtige Rolle beim Bereitstellen von Benutzeroberflächenautomatisierungs-Diensten.</span><span class="sxs-lookup"><span data-stu-id="8b065-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="8b065-178">Er ermöglicht die Navigation zum Fragmentstamm und stellt einige Standardeigenschaften bereit, damit diese nicht vom benutzerdefinierten Anbieter implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8b065-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b065-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b065-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8b065-180">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8b065-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b065-181">Implementieren eines Client-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="8b065-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="8b065-182">Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="8b065-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="8b065-183">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="8b065-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




