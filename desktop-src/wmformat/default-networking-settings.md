---
title: Standard Netzwerkeinstellungen
description: Standard Netzwerkeinstellungen
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media-Format-SDK, standardmäßige Netzwerkeinstellungen
- Advanced Systems Format (ASF), Standard Netzwerkeinstellungen
- ASF (Advanced Systems Format), standardmäßige Netzwerkeinstellungen
- Windows Media-Format-SDK, Netzwerkeinstellungen
- Advanced Systems Format (ASF), Netzwerkeinstellungen
- ASF (Advanced Systems Format), Netzwerkeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856924"
---
# <a name="default-networking-settings"></a><span data-ttu-id="2ca00-109">Standard Netzwerkeinstellungen</span><span class="sxs-lookup"><span data-stu-id="2ca00-109">Default Networking Settings</span></span>

<span data-ttu-id="2ca00-110">In den folgenden Tabellen werden die Standardeinstellungen der Netzwerkparameter im Windows Media-Format-SDK, gruppiert nach Schnittstelle, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2ca00-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="2ca00-111">Iwmreadernetworkconfig</span><span class="sxs-lookup"><span data-stu-id="2ca00-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="2ca00-112">Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="2ca00-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="2ca00-113">Pufferzeit</span><span class="sxs-lookup"><span data-stu-id="2ca00-113">Buffering time</span></span>                        | <span data-ttu-id="2ca00-114">5 Sekunden</span><span class="sxs-lookup"><span data-stu-id="2ca00-114">5 seconds</span></span>                    |
| <span data-ttu-id="2ca00-115">Usefixedudpport</span><span class="sxs-lookup"><span data-stu-id="2ca00-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="2ca00-116">false</span><span class="sxs-lookup"><span data-stu-id="2ca00-116">FALSE</span></span>                        |
| <span data-ttu-id="2ca00-117">Fixedudpport</span><span class="sxs-lookup"><span data-stu-id="2ca00-117">FixedUDPPort</span></span>                          | <span data-ttu-id="2ca00-118">0 (ungültig)</span><span class="sxs-lookup"><span data-stu-id="2ca00-118">0 (not valid)</span></span>                |
| <span data-ttu-id="2ca00-119">Proxysetting: http</span><span class="sxs-lookup"><span data-stu-id="2ca00-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="2ca00-120">WMT- \_ Proxy \_ Einstellungs \_ Browser</span><span class="sxs-lookup"><span data-stu-id="2ca00-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="2ca00-121">Proxysetting: MMS</span><span class="sxs-lookup"><span data-stu-id="2ca00-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="2ca00-122">WMT- \_ Proxy \_ Einstellung \_ None</span><span class="sxs-lookup"><span data-stu-id="2ca00-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="2ca00-123">Proxysetting: RTSP</span><span class="sxs-lookup"><span data-stu-id="2ca00-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="2ca00-124">WMT- \_ Proxy \_ Einstellung \_ None</span><span class="sxs-lookup"><span data-stu-id="2ca00-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="2ca00-125">Proxyhostname (http, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="2ca00-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="2ca00-126">""</span><span class="sxs-lookup"><span data-stu-id="2ca00-126">""</span></span>                           |
| <span data-ttu-id="2ca00-127">Proxyport: http</span><span class="sxs-lookup"><span data-stu-id="2ca00-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="2ca00-128">80</span><span class="sxs-lookup"><span data-stu-id="2ca00-128">80</span></span>                           |
| <span data-ttu-id="2ca00-129">Proxyport: MMS</span><span class="sxs-lookup"><span data-stu-id="2ca00-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="2ca00-130">1755</span><span class="sxs-lookup"><span data-stu-id="2ca00-130">1755</span></span>                         |
| <span data-ttu-id="2ca00-131">Proxtport: RTSP</span><span class="sxs-lookup"><span data-stu-id="2ca00-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="2ca00-132">554</span><span class="sxs-lookup"><span data-stu-id="2ca00-132">554</span></span>                          |
| <span data-ttu-id="2ca00-133">Proxyexceptionlist (http, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="2ca00-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="2ca00-134">""</span><span class="sxs-lookup"><span data-stu-id="2ca00-134">""</span></span>                           |
| <span data-ttu-id="2ca00-135">Proxybypassforlocal (http, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="2ca00-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="2ca00-136">false</span><span class="sxs-lookup"><span data-stu-id="2ca00-136">FALSE</span></span>                        |
| <span data-ttu-id="2ca00-137">Forcererunautoerkennungs</span><span class="sxs-lookup"><span data-stu-id="2ca00-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="2ca00-138">false</span><span class="sxs-lookup"><span data-stu-id="2ca00-138">FALSE</span></span>                        |
| <span data-ttu-id="2ca00-139">Enablemulticast</span><span class="sxs-lookup"><span data-stu-id="2ca00-139">EnableMulticast</span></span>                       | <span data-ttu-id="2ca00-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-140">TRUE</span></span>                         |
| <span data-ttu-id="2ca00-141">Enablehttp</span><span class="sxs-lookup"><span data-stu-id="2ca00-141">EnableHTTP</span></span>                            | <span data-ttu-id="2ca00-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-142">TRUE</span></span>                         |
| <span data-ttu-id="2ca00-143">Enabletcp</span><span class="sxs-lookup"><span data-stu-id="2ca00-143">EnableTCP</span></span>                             | <span data-ttu-id="2ca00-144">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-144">TRUE</span></span>                         |
| <span data-ttu-id="2ca00-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="2ca00-145">EnableUDP</span></span>                             | <span data-ttu-id="2ca00-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-146">TRUE</span></span>                         |
| <span data-ttu-id="2ca00-147">Verbindungs Bandbreite</span><span class="sxs-lookup"><span data-stu-id="2ca00-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="2ca00-148">0 (automatische Erkennung)</span><span class="sxs-lookup"><span data-stu-id="2ca00-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="2ca00-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="2ca00-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="2ca00-150">Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="2ca00-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="2ca00-151">Beschleunigte streamingdauer</span><span class="sxs-lookup"><span data-stu-id="2ca00-151">Accelerated streaming duration</span></span> | <span data-ttu-id="2ca00-152">100 Millionen (10 Sekunden)</span><span class="sxs-lookup"><span data-stu-id="2ca00-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="2ca00-153">Zwischenspeichern von Inhalt aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ca00-153">Enable content caching</span></span>         | <span data-ttu-id="2ca00-154">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-154">TRUE</span></span>                   |
| <span data-ttu-id="2ca00-155">Schnellen Cache aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ca00-155">Enable fast cache</span></span>              | <span data-ttu-id="2ca00-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-156">TRUE</span></span>                   |
| <span data-ttu-id="2ca00-157">Erneute Sende Vorgänge aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ca00-157">Enable resends</span></span>                 | <span data-ttu-id="2ca00-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-158">TRUE</span></span>                   |
| <span data-ttu-id="2ca00-159">Inhalts Verdünnung aktivieren</span><span class="sxs-lookup"><span data-stu-id="2ca00-159">Enable content thinning</span></span>        | <span data-ttu-id="2ca00-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ca00-160">TRUE</span></span>                   |
| <span data-ttu-id="2ca00-161">Limit für erneute Verbindungs Herstellung</span><span class="sxs-lookup"><span data-stu-id="2ca00-161">Reconnect limit</span></span>                | <span data-ttu-id="2ca00-162">25</span><span class="sxs-lookup"><span data-stu-id="2ca00-162">25</span></span>                     |



 



| <span data-ttu-id="2ca00-163">Iwmschreiternetworksink</span><span class="sxs-lookup"><span data-stu-id="2ca00-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="2ca00-164">Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="2ca00-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="2ca00-165">Max. Anzahl von Clients</span><span class="sxs-lookup"><span data-stu-id="2ca00-165">Maximum clients</span></span>      | <span data-ttu-id="2ca00-166">5</span><span class="sxs-lookup"><span data-stu-id="2ca00-166">5</span></span>                       |
| <span data-ttu-id="2ca00-167">Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="2ca00-167">Network protocol</span></span>     | <span data-ttu-id="2ca00-168">0 (WMT- \_ Protokoll \_ http)</span><span class="sxs-lookup"><span data-stu-id="2ca00-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="2ca00-169">Host-URL</span><span class="sxs-lookup"><span data-stu-id="2ca00-169">Host URL</span></span>             | <span data-ttu-id="2ca00-170">0 (ungültig)</span><span class="sxs-lookup"><span data-stu-id="2ca00-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="2ca00-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="2ca00-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="2ca00-172">Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="2ca00-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="2ca00-173">Maximale Paketgröße</span><span class="sxs-lookup"><span data-stu-id="2ca00-173">Maximum packet size</span></span> | <span data-ttu-id="2ca00-174">1400</span><span class="sxs-lookup"><span data-stu-id="2ca00-174">1400</span></span>                        |
| <span data-ttu-id="2ca00-175">Protokoll Client-ID</span><span class="sxs-lookup"><span data-stu-id="2ca00-175">Log client ID</span></span>       | <span data-ttu-id="2ca00-176">false</span><span class="sxs-lookup"><span data-stu-id="2ca00-176">FALSE</span></span>                       |
| <span data-ttu-id="2ca00-177">Wiedergabemodus</span><span class="sxs-lookup"><span data-stu-id="2ca00-177">Play mode</span></span>           | <span data-ttu-id="2ca00-178">WMT- \_ Wiedergabe \_ Modus \_ Autoselect</span><span class="sxs-lookup"><span data-stu-id="2ca00-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2ca00-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ca00-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca00-180">**Implementieren von Netzwerkfunktionen**</span><span class="sxs-lookup"><span data-stu-id="2ca00-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




