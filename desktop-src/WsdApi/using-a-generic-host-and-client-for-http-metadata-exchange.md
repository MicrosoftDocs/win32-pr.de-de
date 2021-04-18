---
description: Wenn der Client und der Host keine Metadaten austauschen können, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345804"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="dae54-103">Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch</span><span class="sxs-lookup"><span data-stu-id="dae54-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="dae54-104">Wenn der Client und der Host keine Metadaten austauschen können, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="dae54-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="dae54-105">Wenn die Geräteadresse oder die Geräte Metadaten nicht in der WSD-debugclientausgabe angezeigt werden, kann der Fehler von den angegebenen Transport Adressen oder der Netzwerkumgebung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="dae54-106">Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dae54-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="dae54-107">Wenn überprüft wurde, ob ein generischer Host und ein Client sowohl WS-Discovery als auch http-Metadatenaustausch durchführen können, kann diese Diagnose Prozedur übersprungen und die Problembehandlung fortgesetzt werden, indem die Verfahren unter [Verwenden der WinHTTP-Protokollierung zum Überprüfen von Datenverkehr](using-winhttp-logging-to-verify-get-traffic.md)durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="dae54-108">Wenn entweder der Host oder der Client eine Anwendung ist, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="dae54-109">Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="dae54-110">Auch wenn der Host oder der Client ein eigenständiges Gerät ist, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client in einem Sicherheitskontext ausgeführt wird, der unbegrenzten Netzwerk Zugriff garantiert (z. b. als Administrator).</span><span class="sxs-lookup"><span data-stu-id="dae54-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="dae54-111">**So verwenden Sie einen generischen Host und Client für die Problembehandlung von http-Metadatenaustausch**</span><span class="sxs-lookup"><span data-stu-id="dae54-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="dae54-112">Öffnen Sie ein Eingabeaufforderungsfenster.</span><span class="sxs-lookup"><span data-stu-id="dae54-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="dae54-113">Führen Sie den folgenden Befehl aus: **wsddebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="dae54-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="dae54-114">Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dae54-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="dae54-115">Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-debughosts zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="dae54-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="dae54-116">Dieser Befehl generiert eine Ausgabe ähnlich der folgenden.</span><span class="sxs-lookup"><span data-stu-id="dae54-116">This command generates output similar to the following.</span></span> <span data-ttu-id="dae54-117">Notieren Sie sich die Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="dae54-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="dae54-118">Führen Sie den folgenden Befehl **aus: wsddebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="dae54-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="dae54-119">Ersetzen Sie *<id>* durch die in Schritt 2 identifizierte Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="dae54-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="dae54-120">Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dae54-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="dae54-121">Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-Debugclients zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="dae54-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="dae54-122">Der WSD-Debugclient generiert eine Ausgabe ähnlich der folgenden.</span><span class="sxs-lookup"><span data-stu-id="dae54-122">WSD Debug Client generates output similar to the following.</span></span>

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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="dae54-123">Der WSD-Debugclient generiert möglicherweise eine Menge Ausgabe in einem Netzwerk mit vielen DPWS-Geräten.</span><span class="sxs-lookup"><span data-stu-id="dae54-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="dae54-124">Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="dae54-125">Geben Sie **Log Tee** *<filename>* an der WSD Debug Client-Eingabeaufforderung ein, um die Ausgabe an eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="dae54-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="dae54-126">Die Ausgabe Umleitung kann beendet werden, indem Sie an der WSD-Debug-Client-Eingabeaufforderung " **Log Tee-Stopp**</span><span class="sxs-lookup"><span data-stu-id="dae54-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="dae54-127">Notieren Sie sich die Endpunkt Verweisadresse (EPR).</span><span class="sxs-lookup"><span data-stu-id="dae54-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="dae54-128">Diese EPR-Adresse sollte mit der in Schritt 2 oben identifizierten Geräte-ID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="dae54-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="dae54-129">Vergewissern Sie sich außerdem, dass der WSD-Debugclient die Metadaten für das Gerät vollständig gedruckt hat.</span><span class="sxs-lookup"><span data-stu-id="dae54-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="dae54-130">Die Geräte Metadaten beginnen mit `Metadata for host` und enden mit `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="dae54-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="dae54-131">Wenn die Geräte-ID und die Geräte Metadaten in der WSD-debugclientausgabe ordnungsgemäß angezeigt werden, ist der Anwendungsfehler wahrscheinlich nicht mit den angegebenen Transport Adressen, dem Betriebssystem oder der Netzwerkumgebung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="dae54-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="dae54-132">Ersetzen Sie den generischen Host und Client durch den benutzerdefinierten Host und Client, und setzen Sie die Problembehandlung fort, indem Sie die Schritte unter [Verwenden von WinHTTP-Protokollierung zum Überprüfen](using-winhttp-logging-to-verify-get-traffic.md)von</span><span class="sxs-lookup"><span data-stu-id="dae54-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="dae54-133">Wenn die Geräteadresse und die Geräte Metadaten nicht in der WSD-debugclientausgabe angezeigt werden, kann der Fehler eine oder mehrere der folgenden Gründe haben:</span><span class="sxs-lookup"><span data-stu-id="dae54-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="dae54-134">Die vom Host angekündigte Transport Adresse ist falsch oder falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="dae54-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="dae54-135">Der WSD-Debugclient versucht, die Geräte Metadaten aus der URL zu erhalten, die im **xaddrs** -Element einer [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Meldung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dae54-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="dae54-136">Die für den Metadatenaustausch verwendete URL wird in der WSD-debugclientausgabe angezeigt, die dem Ausdruck vorangestellt ist `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="dae54-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="dae54-137">Das folgende Beispiel zeigt die xaddrs, die für den Metadatenaustausch in der obigen WSD-debugclientausgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dae54-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="dae54-138">Wenn die angegebenen xaddrs nicht den [xaddr-Validierungsregeln](xaddr-validation-rules.md)entsprechen, kann der WSD-Debugclient die Metadaten des Geräts nicht erhalten.</span><span class="sxs-lookup"><span data-stu-id="dae54-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="dae54-139">Die Anwendung wird im falschen Sicherheitskontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dae54-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="dae54-140">Vergewissern Sie sich, dass die Anwendung die richtigen Anmelde Informationen verwendet und dass der Client und der Host über ausreichende Zugriffsberechtigungen für das Netzwerk verfügen.</span><span class="sxs-lookup"><span data-stu-id="dae54-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="dae54-141">Die Firewallkonfiguration ist falsch.</span><span class="sxs-lookup"><span data-stu-id="dae54-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="dae54-142">Befolgen Sie die Anweisungen unter Überprüfen der [Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md) , um sicherzustellen, dass die Windows-Firewall-Einstellungen korrekt sind und keine anderen Regeln zum Löschen der Pakete vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dae54-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="dae54-143">Der Client und der Host können auch auf einen "unverfälschten" Computer kopiert werden (einer mit einer Standardinstallation des Betriebssystems, der noch nie einer Domäne hinzugefügt wurde), um den Fehler zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="dae54-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="dae54-144">Eine IPSec-Richtlinie blockiert die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dae54-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="dae54-145">Kopieren Sie den Client und den Host auf einen Computer, der keine IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="dae54-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dae54-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dae54-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae54-147">WSDAPI-Diagnose Prozeduren</span><span class="sxs-lookup"><span data-stu-id="dae54-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="dae54-148">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="dae54-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



