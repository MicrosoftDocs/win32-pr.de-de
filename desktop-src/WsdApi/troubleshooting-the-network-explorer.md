---
description: Listet die bei der Problembehandlung für den Netzwerk-Explorer zu verwendenden Diagnoseverfahren auf.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Problembehandlung für den Netzwerk-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958919"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="4f4b7-103">Problembehandlung für den Netzwerk-Explorer</span><span class="sxs-lookup"><span data-stu-id="4f4b7-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="4f4b7-104">Der Netzwerk-Explorer:</span><span class="sxs-lookup"><span data-stu-id="4f4b7-104">The Network Explorer:</span></span>

-   <span data-ttu-id="4f4b7-105">Verwendet für die Geräte Ermittlung immer UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="4f4b7-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="4f4b7-106">Initiiert immer eine HTTP-oder HTTPS-Verbindung für den Metadatenaustausch.</span><span class="sxs-lookup"><span data-stu-id="4f4b7-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="4f4b7-107">Verwendet manchmal einen sicheren Kanal (HTTPS) für den Metadatenaustausch</span><span class="sxs-lookup"><span data-stu-id="4f4b7-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="4f4b7-108">Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit dem Netzwerk-Explorer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4f4b7-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="4f4b7-109">**So beheben Sie Probleme mit dem Netzwerk-Explorer**</span><span class="sxs-lookup"><span data-stu-id="4f4b7-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="4f4b7-110">Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="4f4b7-111">[Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="4f4b7-112">[Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="4f4b7-113">[Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="4f4b7-114">[Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="4f4b7-115">[Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="4f4b7-116">[Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="4f4b7-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="4f4b7-117">Der Netzwerk-Explorer verwendet die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlung zum Auflisten von Netzwerkgeräten.</span><span class="sxs-lookup"><span data-stu-id="4f4b7-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="4f4b7-118">Weitere Informationen zur Problembehandlung finden Sie unter Problembehandlung bei [Funktions Ermittlungs Clients](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="4f4b7-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="4f4b7-119">Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="4f4b7-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f4b7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f4b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f4b7-121">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="4f4b7-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="4f4b7-122">Problembehandlung bei Funktions Ermittlungs Clients</span><span class="sxs-lookup"><span data-stu-id="4f4b7-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
