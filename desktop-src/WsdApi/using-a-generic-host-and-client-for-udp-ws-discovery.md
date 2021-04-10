---
description: Wenn der Client und der Host sich nicht im Netzwerk befinden, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214978"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="363dd-103">Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="363dd-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="363dd-104">Wenn der Client und der Host sich nicht im Netzwerk befinden, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="363dd-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="363dd-105">Wenn die Geräteadresse nicht in der WSD-debugclientausgabe angezeigt wird, verursacht die Netzwerkumgebung wahrscheinlich den Fehler.</span><span class="sxs-lookup"><span data-stu-id="363dd-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="363dd-106">Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="363dd-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="363dd-107">Wenn entweder der Host oder der Client eine Anwendung ist, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="363dd-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="363dd-108">Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="363dd-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="363dd-109">Auch wenn der Host oder der Client ein eigenständiges Gerät ist, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="363dd-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="363dd-110">**So verwenden Sie einen generischen Host und Client für die Problembehandlung von UDP-WS-Discovery**</span><span class="sxs-lookup"><span data-stu-id="363dd-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="363dd-111">Öffnen Sie ein Eingabeaufforderungsfenster.</span><span class="sxs-lookup"><span data-stu-id="363dd-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="363dd-112">Führen Sie den folgenden Befehl aus: **wsddebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="363dd-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="363dd-113">Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="363dd-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="363dd-114">Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-debughosts zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="363dd-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="363dd-115">Dieser Befehl generiert eine Ausgabe ähnlich der folgenden.</span><span class="sxs-lookup"><span data-stu-id="363dd-115">This command generates output similar to the following.</span></span> <span data-ttu-id="363dd-116">Notieren Sie sich die Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="363dd-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="363dd-117">Führen Sie den folgenden Befehl **aus: wsddebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="363dd-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="363dd-118">Ersetzen Sie *<id>* durch die in Schritt 2 identifizierte Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="363dd-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="363dd-119">Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="363dd-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="363dd-120">Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-Debugclients zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="363dd-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="363dd-121">Der WSD-Debugclient generiert eine Ausgabe ähnlich der folgenden.</span><span class="sxs-lookup"><span data-stu-id="363dd-121">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

<span data-ttu-id="363dd-122">Der WSD-Debugclient generiert möglicherweise eine Menge Ausgabe in einem Netzwerk mit vielen DPWS-Geräten.</span><span class="sxs-lookup"><span data-stu-id="363dd-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="363dd-123">Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="363dd-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="363dd-124">Geben Sie **Log Tee** *<filename>* an der WSD Debug Client-Eingabeaufforderung ein, um die Ausgabe an eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="363dd-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="363dd-125">Die Ausgabe Umleitung kann beendet werden, indem Sie an der WSD-Debug-Client-Eingabeaufforderung " **Log Tee-Stopp**</span><span class="sxs-lookup"><span data-stu-id="363dd-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="363dd-126">Notieren Sie sich die Endpunkt Verweisadresse (EPR).</span><span class="sxs-lookup"><span data-stu-id="363dd-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="363dd-127">Diese EPR-Adresse sollte mit der in Schritt 2 oben identifizierten Geräte-ID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="363dd-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="363dd-128">Wenn dies der Fall ist, ist der Anwendungsfehler wahrscheinlich nicht mit dem Betriebssystem oder der Netzwerkumgebung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="363dd-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="363dd-129">Ersetzen Sie den generischen Host und den generischen Client durch den benutzerdefinierten Host und Client, und setzen Sie die Problembehandlung fort, indem Sie die Schritte unter [Verwenden des WSD-Debugclients zum Überprüfen](using-wsddebug-client-to-verify-multicast-traffic.md)</span><span class="sxs-lookup"><span data-stu-id="363dd-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="363dd-130">Wenn die Geräte-ID nicht mit der EPR-Adresse identisch ist, ist der Anwendungsfehler wahrscheinlich mit dem Betriebssystem oder der Netzwerkumgebung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="363dd-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="363dd-131">Der Fehler kann eine oder mehrere der folgenden Gründe haben:</span><span class="sxs-lookup"><span data-stu-id="363dd-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="363dd-132">Die Anwendung wird im falschen Sicherheitskontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="363dd-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="363dd-133">Vergewissern Sie sich, dass die Anwendung die richtigen Anmelde Informationen verwendet und dass der Client und der Host über ausreichende Zugriffsberechtigungen für das Netzwerk verfügen.</span><span class="sxs-lookup"><span data-stu-id="363dd-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="363dd-134">Die Firewallkonfiguration ist falsch.</span><span class="sxs-lookup"><span data-stu-id="363dd-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="363dd-135">Befolgen Sie die Anweisungen unter Überprüfen der [Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md) , um sicherzustellen, dass die Windows-Firewall-Einstellungen korrekt sind und keine anderen Regeln zum Löschen der Pakete vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="363dd-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="363dd-136">Der Client und der Host können auch auf einen "unverfälschten" Computer kopiert werden (einer mit einer Standardinstallation des Betriebssystems, der noch nie einer Domäne hinzugefügt wurde), um den Fehler zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="363dd-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="363dd-137">Eine IPSec-Richtlinie blockiert die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="363dd-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="363dd-138">Kopieren Sie Client und Host auf einen Computer, der nicht den IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="363dd-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="363dd-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="363dd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="363dd-140">WSDAPI-Diagnose Prozeduren</span><span class="sxs-lookup"><span data-stu-id="363dd-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="363dd-141">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="363dd-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



