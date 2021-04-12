---
title: Übersicht über die Benutzeroberflächenautomatisierung
description: Die Microsoft-Benutzeroberflächen Automatisierung ist ein Barrierefreiheits Framework für Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Benutzeroberflächen Automatisierung, Informationen zu
- Benutzeroberflächen Automatisierung, Barrierefreiheit
- Benutzeroberflächen Automatisierung, Komponenten
- UI-Automatisierung, Anbieter-API
- Benutzeroberflächen Automatisierung, Client-API
- Benutzeroberflächen Automatisierung, Header Dateien
- UI-Automatisierung, Modell
- components
- Barrierefreiheit
- Anbieter-API
- Client-API
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389815"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="ef9b3-115">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ef9b3-115">UI Automation Overview</span></span>

<span data-ttu-id="ef9b3-116">Die Microsoft-Benutzeroberflächen Automatisierung ist ein Barrierefreiheits Framework für Windows.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="ef9b3-117">Sie ermöglicht programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="ef9b3-118">Sie ermöglicht Hilfstechnologieprodukten, wie z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Endbenutzer bereitzustellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="ef9b3-119">Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="ef9b3-120">Die Benutzeroberflächen Automatisierung war erstmals in Windows XP als Teil des Microsoft .NET Frameworks verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="ef9b3-121">Obwohl eine nicht verwaltete C++-API zu diesem Zeitpunkt ebenfalls veröffentlicht wurde, war die Nützlichkeit von Client Funktionen aufgrund von Interoperabilitätsproblemen eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="ef9b3-122">Für Windows 7 wurde die API im Component Object Model (com) umgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="ef9b3-123">Obwohl die in der früheren Version der Benutzeroberflächen Automatisierung eingeführten Bibliotheksfunktionen weiterhin dokumentiert sind, sollten Sie in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="ef9b3-124">Benutzeroberflächenautomatisierungs-Client Anwendungen können mit der Gewissheit geschrieben werden, dass Sie an mehreren Microsoft Windows-Steuerelement-Frameworks funktionieren.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="ef9b3-125">Der Benutzeroberflächenautomatisierungs-Kern maskiert alle Unterschiede in den Frameworks, die verschiedene Teile der Benutzeroberfläche unterliegen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="ef9b3-126">Beispielsweise werden die **Content** -Eigenschaft einer Windows Presentation Foundation (WPF)-Schaltfläche, die **Caption** -Eigenschaft einer Microsoft Win32-Schaltfläche und die **alt** -Eigenschaft eines HTML-Bilds alle einer einzelnen Eigenschaft ( **Name**) in der Benutzeroberflächenautomatisierungs-Ansicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="ef9b3-127">Die Benutzeroberflächen Automatisierung bietet vollständige Funktionalität in den Betriebssystemen Windows XP, Windows Server 2003 und höher.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="ef9b3-128">Benutzeroberflächenautomatisierungs-Anbieter sind Komponenten, die die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelemente implementieren und einige Unterstützung für Microsoft Active Accessibility-Client Anwendungen über einen integrierten Überbrückungs Dienst bieten.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="ef9b3-129">Die Benutzeroberflächen Automatisierung ermöglicht keine Kommunikation zwischen Prozessen, die von verschiedenen Benutzern durch den Befehl **Ausführen als** gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="ef9b3-130">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ef9b3-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ef9b3-131">UI-Automatisierungskomponenten</span><span class="sxs-lookup"><span data-stu-id="ef9b3-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="ef9b3-132">Benutzeroberflächenautomatisierungs-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ef9b3-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="ef9b3-133">Benutzeroberflächenautomatisierungs-Modell</span><span class="sxs-lookup"><span data-stu-id="ef9b3-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="ef9b3-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef9b3-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="ef9b3-135">UI-Automatisierungskomponenten</span><span class="sxs-lookup"><span data-stu-id="ef9b3-135">UI Automation Components</span></span>

<span data-ttu-id="ef9b3-136">Die Benutzeroberflächen Automatisierung verfügt über vier Hauptkomponenten, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef9b3-137">Komponente</span><span class="sxs-lookup"><span data-stu-id="ef9b3-137">Component</span></span></th>
<th><span data-ttu-id="ef9b3-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef9b3-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef9b3-139">Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="ef9b3-139">Provider API</span></span></td>
<td><span data-ttu-id="ef9b3-140">Ein Satz von COM-Schnittstellen, die von Benutzeroberflächenautomatisierungs-Anbietern implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="ef9b3-141">Benutzeroberflächenautomatisierungs-Anbieter sind Objekte, die Informationen über Benutzeroberflächen Elemente bereitstellen und auf programmgesteuerte Eingaben reagieren.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef9b3-142">Client-API</span><span class="sxs-lookup"><span data-stu-id="ef9b3-142">Client API</span></span></td>
<td><span data-ttu-id="ef9b3-143">Ein Satz von COM-Schnittstellen, mit denen Client Anwendungen Informationen über die Benutzeroberfläche abrufen und Eingaben an Steuerelemente senden können.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ef9b3-144">Die Funktionen, die in <a href="uiauto-entry-cpfunctions.md">veralteten Steuerelement Mustern</a> und Funktionen für <a href="uiauto-entry-uianodefunctions.md">Veraltete Knoten</a> beschrieben werden, sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="ef9b3-145">Stattdessen sollten Client Anwendungen die in Benutzeroberflächenautomatisierungs- <a href="uiauto-entry-uiautoclientinterfaces.md">Element Schnittstellen für Clients</a>beschriebenen Benutzeroberflächenautomatisierungs-com-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef9b3-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="ef9b3-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="ef9b3-147">Die Lauf Zeit Bibliothek, die manchmal als Benutzeroberflächenautomatisierungs-Kern bezeichnet wird und die Kommunikation zwischen Anbietern und Clients behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef9b3-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="ef9b3-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="ef9b3-149">Die Lauf Zeit Bibliothek für Microsoft Active Accessibility und die Proxy Objekte.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="ef9b3-150">Die Bibliothek stellt auch Proxy Objekte bereit, die vom Microsoft Microsoft Active Accessibility dem Benutzeroberflächenautomatisierungs-Proxy zur Unterstützung von Win32-Steuerelementen verwendet</span><span class="sxs-lookup"><span data-stu-id="ef9b3-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ef9b3-151">Es gibt zwei Möglichkeiten zum Verwenden der Benutzeroberflächen Automatisierung: zum Erstellen von Unterstützung für benutzerdefinierte Steuerelemente mithilfe der Anbieter-API und zum Erstellen von Client Anwendungen, die den Benutzeroberflächenautomatisierungs-Kern zum kommunizieren mit und zum Abrufen von Informationen zu Benutzeroberflächen Elementen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="ef9b3-152">Abhängig von Ihren Schwerpunkten sollten Sie auf verschiedene Teile der Dokumentation zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="ef9b3-153">Wenn Sie Unterstützung für benutzerdefinierte Steuerelemente erstellen müssen, finden Sie weitere Informationen unter [Benutzeroberflächenautomatisierungs-Anbieter Handbuch](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="ef9b3-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="ef9b3-154">Informationen zu den Benutzeroberflächen Elementen finden Sie unter [Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="ef9b3-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="ef9b3-155">Benutzeroberflächenautomatisierungs-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ef9b3-155">UI Automation Header Files</span></span>

<span data-ttu-id="ef9b3-156">Die Benutzeroberflächenautomatisierungs-API ist in verschiedenen C/C++-Header Dateien definiert, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ef9b3-157">Die Header Dateien für die Benutzeroberflächen Automatisierung werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ef9b3-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="ef9b3-158">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ef9b3-158">Header file</span></span>           | <span data-ttu-id="ef9b3-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef9b3-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9b3-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="ef9b3-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="ef9b3-161">Definiert die von Benutzeroberflächenautomatisierungs-Clients verwendeten Schnittstellen und zugehörigen Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="ef9b3-162">Uiautomationcore. h</span><span class="sxs-lookup"><span data-stu-id="ef9b3-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="ef9b3-163">Definiert die Schnittstellen und zugehörigen Programmier Elemente, die von Benutzeroberflächenautomatisierungs-Anbietern verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ef9b3-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="ef9b3-164">Uiautomationcoreapi. h</span><span class="sxs-lookup"><span data-stu-id="ef9b3-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="ef9b3-165">Definiert allgemeine Konstanten, GUIDs, Datentypen und Strukturen, die von Benutzeroberflächenautomatisierungs-Clients und-Anbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="ef9b3-166">Sie enthält auch Definitionen für die veralteten Knoten-und Steuerelement Muster Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="ef9b3-167">Uiautomation. h</span><span class="sxs-lookup"><span data-stu-id="ef9b3-167">UIAutomation.h</span></span>        | <span data-ttu-id="ef9b3-168">Schließt alle anderen Header Dateien der Benutzeroberflächen Automatisierung ein.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="ef9b3-169">Da die meisten Benutzeroberflächenautomatisierungs-Anwendungen Elemente aus allen Header Dateien für die Benutzeroberflächen Automatisierung benötigen, empfiehlt es sich, "uiautomation. h" in Ihre Benutzeroberflächenautomatisierungs-Anwendungsprojekte einzubeziehen, anstatt jede Datei einzeln zu</span><span class="sxs-lookup"><span data-stu-id="ef9b3-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="ef9b3-170">Wenn Sie eine Anwendung entwickeln, die die Benutzeroberflächenautomatisierungs-API verwendet, sollten Sie "uiautomation. h" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="ef9b3-171">Wenn Ihre Anwendung Microsoft Active Accessibility unterstützt, schließen Sie die Header Datei "Oleacc. h" ein.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="ef9b3-172">Benutzeroberflächenautomatisierungs-Anwendungen, die GUIDs verwenden, benötigen auch die Header Datei "Initguid. h".</span><span class="sxs-lookup"><span data-stu-id="ef9b3-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="ef9b3-173">Bei Bedarf sollte Initguid. h vor "uiautomation. h" eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="ef9b3-174">Benutzeroberflächenautomatisierungs-Modell</span><span class="sxs-lookup"><span data-stu-id="ef9b3-174">UI Automation Model</span></span>

<span data-ttu-id="ef9b3-175">Die Benutzeroberflächen Automatisierung macht alle Elemente der Benutzeroberfläche für Client Anwendungen als Objekt verfügbar, das von der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="ef9b3-176">Elemente sind in einer Baumstruktur, mit dem Desktop als Stammelement, enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="ef9b3-177">Clients können die „Rohdatenansicht“ der Struktur als „Steuerelementansicht“ oder „Inhaltsansicht“ filtern.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="ef9b3-178">Diese Standard Sichten der Struktur können problemlos mithilfe der in der Windows SDK enthaltenen Anwendung "über [prüfen](inspect-objects.md) " angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="ef9b3-179">Anwendungen können auch benutzerdefinierte Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-179">Applications can also create custom views.</span></span>

<span data-ttu-id="ef9b3-180">Ein Benutzeroberflächenautomatisierungs-Element macht Eigenschaften des Steuer Elements oder des Benutzeroberflächen Elements verfügbar, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="ef9b3-181">Eine dieser Eigenschaften ist der Steuer Elementtyp, der die grundlegende Darstellung und die Funktionalität des Steuer Elements oder des Benutzeroberflächen Elements als einzelne erkennbare Entität definiert, z. b. eine Schaltfläche oder ein Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="ef9b3-182">Weitere Informationen zu Steuerelement Typen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ef9b3-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="ef9b3-183">Außerdem stellt ein Benutzeroberflächenautomatisierungs-Element ein oder mehrere Steuerelement Muster zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="ef9b3-184">Ein-Steuerelement Muster stellt einen Satz von Eigenschaften bereit, die für einen bestimmten Steuerelement Typen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="ef9b3-185">Ein Steuerelement Muster macht auch Methoden verfügbar, mit denen Client Anwendungen Weitere Informationen über das Element erhalten und Eingaben für das Element bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="ef9b3-186">Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ef9b3-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef9b3-187">Es gibt keine eins-zu-eins-Entsprechung zwischen Steuerelement Typen und Steuerelement Mustern.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="ef9b3-188">Ein Steuerelementmuster kann von mehreren Steuerelementtypen unterstützt werden, und ein Steuerelement kann mehrere Steuerelementmuster unterstützen, von denen jedes einen anderen Aspekt des Verhaltens verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="ef9b3-189">Ein Kombinationsfeld hat beispielsweise mindestens zwei Steuerelementmuster: eines mit der Fähigkeit zum Erweitern und Reduzieren und ein anderes, das den Auswahlmechanismus darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="ef9b3-190">Ein Steuerelement kann jedoch nur einen einzigen Steuerelement Typen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="ef9b3-191">Die Benutzeroberflächen Automatisierung stellt mithilfe von Ereignissen Informationen für Client Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="ef9b3-192">Im Gegensatz zu WinEvents basieren Benutzeroberflächenautomatisierungs-Ereignisse nicht auf einem Übertragungsmechanismus.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="ef9b3-193">Benutzeroberflächenautomatisierungs-Clients registrieren sich für bestimmte Ereignis Benachrichtigungen und können anfordern, dass bestimmte Eigenschaften und Steuerelement Muster Informationen an Ihre Ereignishandler übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="ef9b3-194">Außerdem enthält ein Benutzeroberflächenautomatisierungs-Ereignis einen Verweis auf das Element, das es ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="ef9b3-195">Anbieter können die Leistung verbessern, indem sie Ereignisse selektiv abhängig davon auslösen, ob Clients zuhören.</span><span class="sxs-lookup"><span data-stu-id="ef9b3-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="ef9b3-196">Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ef9b3-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef9b3-197">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef9b3-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef9b3-198">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ef9b3-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef9b3-199">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ef9b3-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ef9b3-200">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ef9b3-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ef9b3-201">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ef9b3-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





