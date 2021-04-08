---
title: Registrierungs Einstellungen für den Firewallport
description: Registrierungs Einstellungen für den Firewallport
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, Registrierungs Einstellungen für Firewallports
- Windows Media Player, Port Registrierungs Einstellungen
- Windows Media Player, Registrierung
- Registrierung, firewallporteinstellungen
- Registrierung, Port Einstellungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für den Firewallport
- Port Registrierungs Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855564"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="521e7-111">Registrierungs Einstellungen für den Firewallport</span><span class="sxs-lookup"><span data-stu-id="521e7-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="521e7-112">Windows Media Player fügt Einträge in die Registrierung ein, damit Firewalls feststellen können, ob die von der Medien Bibliotheks Freigabe verwendeten Ports geöffnet oder geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="521e7-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="521e7-113">**Registrierungs Eintrag "akzeptede"**</span><span class="sxs-lookup"><span data-stu-id="521e7-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="521e7-114">Windows Media Player verwendet den folgenden Registrierungs Eintrag, um anzugeben, ob der Benutzer den Endbenutzer-Lizenzvertrag (EULA) akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="521e7-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="521e7-115">Der Wert 1 gibt an, dass der Benutzer den Lizenzvertrag akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="521e7-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="521e7-116">Der Wert 0 gibt an, dass der Benutzer den Lizenzvertrag nicht akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="521e7-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="521e7-117">**Wmpnssfirewallportsopen-Registrierungs Eintrag**</span><span class="sxs-lookup"><span data-stu-id="521e7-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="521e7-118">Windows Media Player verwendet den folgenden Registrierungs Eintrag, um anzugeben, ob der Benutzer seine Medienbibliothek auf anderen Computern in einem Heimnetzwerk freigeben möchte.</span><span class="sxs-lookup"><span data-stu-id="521e7-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="521e7-119">Der Wert 1 gibt an, dass der Benutzer die Bibliothek freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="521e7-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="521e7-120">Der Wert 0 gibt an, dass der Benutzer die Bibliothek nicht freigeben möchte.</span><span class="sxs-lookup"><span data-stu-id="521e7-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="521e7-121">**Ports im Zusammenhang mit der Medien Bibliotheks Freigabe**</span><span class="sxs-lookup"><span data-stu-id="521e7-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="521e7-122">Wenn unter Windows Vista der Registrierungs Eintrag **wmpnssfirewallportsopen** den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="521e7-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="521e7-123">Port</span><span class="sxs-lookup"><span data-stu-id="521e7-123">Port</span></span>          | <span data-ttu-id="521e7-124">Protocol</span><span class="sxs-lookup"><span data-stu-id="521e7-124">Protocol</span></span>                  | <span data-ttu-id="521e7-125">Prozess</span><span class="sxs-lookup"><span data-stu-id="521e7-125">Process</span></span>                         | <span data-ttu-id="521e7-126">Richtung</span><span class="sxs-lookup"><span data-stu-id="521e7-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="521e7-127">554</span><span class="sxs-lookup"><span data-stu-id="521e7-127">554</span></span>           | <span data-ttu-id="521e7-128">TCP-RTSP</span><span class="sxs-lookup"><span data-stu-id="521e7-128">TCP RTSP</span></span>                  | <span data-ttu-id="521e7-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-130">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-130">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="521e7-131">8554 - 8558</span></span>   | <span data-ttu-id="521e7-132">TCP-RTSP</span><span class="sxs-lookup"><span data-stu-id="521e7-132">TCP RTSP</span></span>                  | <span data-ttu-id="521e7-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-134">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-134">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="521e7-135">5004, 5005</span></span>    | <span data-ttu-id="521e7-136">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="521e7-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="521e7-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-138">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-138">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="521e7-139">50004 - 50013</span></span> | <span data-ttu-id="521e7-140">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="521e7-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="521e7-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-142">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-142">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-143">1.900</span><span class="sxs-lookup"><span data-stu-id="521e7-143">1900</span></span>          | <span data-ttu-id="521e7-144">UDP-SSDP</span><span class="sxs-lookup"><span data-stu-id="521e7-144">UDP SSDP</span></span>                  | <span data-ttu-id="521e7-145">SSDPSRV in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="521e7-146">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-146">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-147">2869</span><span class="sxs-lookup"><span data-stu-id="521e7-147">2869</span></span>          | <span data-ttu-id="521e7-148">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="521e7-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="521e7-149">SSDPSRV/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="521e7-150">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-150">inbound</span></span>              |
| <span data-ttu-id="521e7-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="521e7-151">10280 - 10284</span></span> | <span data-ttu-id="521e7-152">UDP WMDRM-ND-Registrierung</span><span class="sxs-lookup"><span data-stu-id="521e7-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="521e7-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-154">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-154">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-155">10243</span><span class="sxs-lookup"><span data-stu-id="521e7-155">10243</span></span>         | <span data-ttu-id="521e7-156">TCP http</span><span class="sxs-lookup"><span data-stu-id="521e7-156">TCP HTTP</span></span>                  | <span data-ttu-id="521e7-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-158">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-158">inbound</span></span>              |
| <span data-ttu-id="521e7-159">2177</span><span class="sxs-lookup"><span data-stu-id="521e7-159">2177</span></span>          | <span data-ttu-id="521e7-160">TCP-UDP-qWave</span><span class="sxs-lookup"><span data-stu-id="521e7-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="521e7-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-161">svchost.exe</span></span>                     | <span data-ttu-id="521e7-162">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-162">inbound and outbound</span></span> |



 

<span data-ttu-id="521e7-163">Wenn unter Windows Vista der Registrierungs Eintrag " **akzeptedeula** " den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="521e7-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="521e7-164">Port</span><span class="sxs-lookup"><span data-stu-id="521e7-164">Port</span></span>          | <span data-ttu-id="521e7-165">Protocol</span><span class="sxs-lookup"><span data-stu-id="521e7-165">Protocol</span></span>       | <span data-ttu-id="521e7-166">Prozess</span><span class="sxs-lookup"><span data-stu-id="521e7-166">Process</span></span>                         | <span data-ttu-id="521e7-167">Richtung</span><span class="sxs-lookup"><span data-stu-id="521e7-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="521e7-168">Alle UDP-Ports</span><span class="sxs-lookup"><span data-stu-id="521e7-168">All UDP ports</span></span> | <span data-ttu-id="521e7-169">UDP RTP, MSB</span><span class="sxs-lookup"><span data-stu-id="521e7-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="521e7-170">wmplayer.exe, alle Subnetze</span><span class="sxs-lookup"><span data-stu-id="521e7-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="521e7-171">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-171">inbound</span></span>              |
| <span data-ttu-id="521e7-172">1.900</span><span class="sxs-lookup"><span data-stu-id="521e7-172">1900</span></span>          | <span data-ttu-id="521e7-173">UDP-SSDP</span><span class="sxs-lookup"><span data-stu-id="521e7-173">UDP SSDP</span></span>       | <span data-ttu-id="521e7-174">SSDPSRV/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="521e7-175">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-175">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-176">2869</span><span class="sxs-lookup"><span data-stu-id="521e7-176">2869</span></span>          | <span data-ttu-id="521e7-177">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="521e7-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="521e7-178">SSDPSRV, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="521e7-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="521e7-179">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-179">inbound</span></span>              |



 

<span data-ttu-id="521e7-180">Wenn unter Microsoft Windows XP der Registrierungs Eintrag **wmpnssfirewallportsopen** den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="521e7-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="521e7-181">Port</span><span class="sxs-lookup"><span data-stu-id="521e7-181">Port</span></span>          | <span data-ttu-id="521e7-182">Protocol</span><span class="sxs-lookup"><span data-stu-id="521e7-182">Protocol</span></span>                  | <span data-ttu-id="521e7-183">Prozess</span><span class="sxs-lookup"><span data-stu-id="521e7-183">Process</span></span>                         | <span data-ttu-id="521e7-184">Richtung</span><span class="sxs-lookup"><span data-stu-id="521e7-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="521e7-185">1.900</span><span class="sxs-lookup"><span data-stu-id="521e7-185">1900</span></span>          | <span data-ttu-id="521e7-186">UDP-SSDP</span><span class="sxs-lookup"><span data-stu-id="521e7-186">UDP SSDP</span></span>                  | <span data-ttu-id="521e7-187">SSDPSRV in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="521e7-188">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-188">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-189">2869</span><span class="sxs-lookup"><span data-stu-id="521e7-189">2869</span></span>          | <span data-ttu-id="521e7-190">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="521e7-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="521e7-191">SSDPSRV/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="521e7-192">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-192">inbound</span></span>              |
| <span data-ttu-id="521e7-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="521e7-193">10280 - 10284</span></span> | <span data-ttu-id="521e7-194">UDP WMDRM-ND-Registrierung</span><span class="sxs-lookup"><span data-stu-id="521e7-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="521e7-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-196">eingehende und ausgehende Daten</span><span class="sxs-lookup"><span data-stu-id="521e7-196">inbound and outbound</span></span> |
| <span data-ttu-id="521e7-197">10243</span><span class="sxs-lookup"><span data-stu-id="521e7-197">10243</span></span>         | <span data-ttu-id="521e7-198">TCP http</span><span class="sxs-lookup"><span data-stu-id="521e7-198">TCP HTTP</span></span>                  | <span data-ttu-id="521e7-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="521e7-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="521e7-200">stadteinwärts</span><span class="sxs-lookup"><span data-stu-id="521e7-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="521e7-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="521e7-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="521e7-202">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="521e7-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




