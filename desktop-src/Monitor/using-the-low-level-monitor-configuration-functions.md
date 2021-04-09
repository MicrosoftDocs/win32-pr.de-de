---
title: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
description: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- überwachen, Funktionen
- Überwachen von Konfigurationsfunktionen auf niedriger Ebene
- überwachen, DDC/CI
- überwachen, Anzeigen der Datenkanal-Befehlsschnittstelle
- Überwachen der Konfiguration, Low-Level-Konfigurationsfunktionen
- Monitor Konfiguration, Funktionen
- Monitor Konfiguration, DDC/CI
- Überwachen der Konfiguration, Anzeigen der Datenkanal-Befehlsschnittstelle
- Konfigurationsfunktionen auf niedriger Ebene
- Anzeigen der Datenkanal-Befehlsschnittstelle
- DDC/CI
- VESA-Monitor-Steuerungs Befehlssatz (MCCS)
- Monitor Steuerungs-Befehlssatz (MCCS)
- MCCS (Befehlssatz der Überwachungs Steuerung)
- Virtuelle Systemsteuerung (VCP)
- VCP (virtuelle Systemsteuerung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948685"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="23dd2-119">Verwenden der Low-Level Monitor-Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="23dd2-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="23dd2-120">Bevor Sie die Konfigurationsfunktionen auf niedriger Ebene verwenden, sollten Sie mit diesen Standards vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="23dd2-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="23dd2-121">Datenkanal Befehlsschnittstelle anzeigen (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="23dd2-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="23dd2-122">VESA-Monitor-Steuerungs Befehlssatz (MCCS)</span><span class="sxs-lookup"><span data-stu-id="23dd2-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="23dd2-123">Die Low-Level-Funktionen funktionieren, indem Sie die Werte von VCP-Codes (Virtual Control Panel) erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="23dd2-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="23dd2-124">Ein VCP-Code kann *kontinuierlich* oder *nicht fortlaufend* sein.</span><span class="sxs-lookup"><span data-stu-id="23dd2-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="23dd2-125">Fortlaufende Codes können einen beliebigen Wert zwischen 0 (null) und einem anbieterspezifischen maximalen Wert annehmen.</span><span class="sxs-lookup"><span data-stu-id="23dd2-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="23dd2-126">Nicht kontinuierliche Codes unterstützen einen definierten Satz von Werten, der auch für den Anbieter spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="23dd2-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="23dd2-127">Führen Sie die folgenden Schritte aus, um die Überwachungs Konfigurationsfunktionen auf niedriger Ebene zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="23dd2-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="23dd2-128">Rufen Sie ein **Hmonitor** -Handle durch Aufrufen von [**enumdisplaymonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) oder [**monitorfromwindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)ab.</span><span class="sxs-lookup"><span data-stu-id="23dd2-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="23dd2-129">Aufrufen von [**getnumofphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) zum Abrufen der Anzahl der physischen Monitore, die dem **Hmonitor** -Handle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="23dd2-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="23dd2-130">Aufrufen von [**getphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) , um eine Liste von Handles für die physischen Monitore zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23dd2-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="23dd2-131">Aufrufen von [**getcapabilitiesstringlength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) zum Abrufen der Länge der DDC/CI-Funktions Zeichenfolge eines Monitors.</span><span class="sxs-lookup"><span data-stu-id="23dd2-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="23dd2-132">Die Funktions Zeichenfolge ist eine ASCII-Zeichenfolge, die statische Informationen über den Monitor enthält.</span><span class="sxs-lookup"><span data-stu-id="23dd2-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="23dd2-133">Ein Teil der Zeichenfolge listet die VCP-Codes auf, die der Monitor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23dd2-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="23dd2-134">In der Zeichenfolge werden auch die unterstützten Werte der nicht kontinuierlichen VCP-Codes aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="23dd2-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="23dd2-135">Zuordnen eines Puffers zum Speichern der Funktions Zeichenfolge und Aufrufen von [**capabilitiesrequestandcapabilitiesreply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) zum Abrufen der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="23dd2-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="23dd2-136">Analysieren Sie die Funktions Zeichenfolge, um zu bestimmen, welche VCP-Codes der Monitor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23dd2-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="23dd2-137">Bei einem kontinuierlichen VCP-Code wird [**getvcpfeatureandvcpfeaturereply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) aufgerufen, um den aktuellen und den maximalen Wert des Codes zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23dd2-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="23dd2-138">Analysieren Sie für einen nicht kontinuierlichen VCP-Code die Funktions Zeichenfolge, um die unterstützten Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23dd2-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="23dd2-139">Aufrufen von [**setvcpfeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) , um einen neuen Wert für einen VCP-Code festzulegen.</span><span class="sxs-lookup"><span data-stu-id="23dd2-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23dd2-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23dd2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23dd2-141">**Verwenden der Monitor Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="23dd2-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 