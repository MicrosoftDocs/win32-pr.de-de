---
description: Listet die Diagnose Prozeduren auf, die bei der Problembehandlung von Funktions Ermittlungs Clients verwendet
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Problembehandlung bei Funktions Ermittlungs Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753665"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="147bc-103">Problembehandlung bei Funktions Ermittlungs Clients</span><span class="sxs-lookup"><span data-stu-id="147bc-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="147bc-104">Funktions Ermittlungs Clients:</span><span class="sxs-lookup"><span data-stu-id="147bc-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="147bc-105">Verwenden Sie für die Geräte Ermittlung stets UDP-WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="147bc-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="147bc-106">HTTP-oder HTTPS-Verbindungen für Metadatenaustausch immer initiieren</span><span class="sxs-lookup"><span data-stu-id="147bc-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="147bc-107">Manchmal gesteuerte Ermittlung verwenden</span><span class="sxs-lookup"><span data-stu-id="147bc-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="147bc-108">Verwenden Sie manchmal einen sicheren Kanal (HTTPS) für den Metadatenaustausch.</span><span class="sxs-lookup"><span data-stu-id="147bc-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="147bc-109">In der folgenden Liste wird die typische Abfolge von Nachrichten angezeigt, die von Funktions Ermittlungs Clients gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="147bc-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="147bc-110">Nicht alle Nachrichten sind obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="147bc-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="147bc-111">Vom Client [wird eine Testnachricht gesendet,](probe-message.md) um Geräte und Dienste zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="147bc-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="147bc-112">Wenn der Client die gesteuerte Ermittlung verwendet, wird diese Nachricht über HTTP oder HTTPS gesendet. Andernfalls wird die Nachricht von UDP-Multicast an Port 3702 gesendet.</span><span class="sxs-lookup"><span data-stu-id="147bc-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="147bc-113">Der Client empfängt [Probe Matches](probematches-message.md) -Nachrichten von übereinstimmenden Geräten oder Diensten.</span><span class="sxs-lookup"><span data-stu-id="147bc-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="147bc-114">Gesteuerte Ermittlungs Meldungen werden über HTTP oder HTTPS gesendet. Andernfalls werden diese Nachrichten von UDP-Unicast gesendet und stammen von Port 3702.</span><span class="sxs-lookup"><span data-stu-id="147bc-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="147bc-115">Wenn keine xaddrs in der probematches-Nachricht enthalten sind, sendet der Client eine [Auflösungs](resolve-message.md) Meldung von UDP-Multicast an Port 3702.</span><span class="sxs-lookup"><span data-stu-id="147bc-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="147bc-116">Wenn eine [Resolve](resolve-message.md) -Nachricht gesendet wurde, empfängt der Client eine [resolvematches](resolvematches-message.md) -Nachricht von übereinstimmenden Diensten.</span><span class="sxs-lookup"><span data-stu-id="147bc-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="147bc-117">Diese Meldung wird von UDP-Unicast von Port 3702 an den Port gesendet, von dem die Auflösungs Nachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="147bc-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="147bc-118">Der Client sendet eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht, um Metadaten vom Gerät oder Dienst anzufordern.</span><span class="sxs-lookup"><span data-stu-id="147bc-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="147bc-119">Diese Meldung wird von http oder HTTPS gesendet.</span><span class="sxs-lookup"><span data-stu-id="147bc-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="147bc-120">Der Client empfängt eine [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht mit dem Gerät oder den Dienst Metadaten.</span><span class="sxs-lookup"><span data-stu-id="147bc-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="147bc-121">Diese Meldung wird von http oder HTTPS gesendet.</span><span class="sxs-lookup"><span data-stu-id="147bc-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="147bc-122">Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einem funktionermittlungs Client zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="147bc-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="147bc-123">**So beheben Sie Probleme mit einem Funktions Ermittlungs Client**</span><span class="sxs-lookup"><span data-stu-id="147bc-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="147bc-124">Wenn die gesteuerte Ermittlung verwendet wird, beheben Sie die Fehler bei der [gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="147bc-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="147bc-125">Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="147bc-126">[Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="147bc-127">[Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="147bc-128">[Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="147bc-129">[Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="147bc-130">[Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="147bc-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="147bc-131">[Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="147bc-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="147bc-132">Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="147bc-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="147bc-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="147bc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="147bc-134">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="147bc-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



