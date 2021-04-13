---
title: ALE Ebenen
description: Die Durchsetzung der Anwendungsschicht (ALE) besteht aus mehreren Filter Ebenen und vielen übereinstimmenden Verwerfungs Ebenen.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314721"
---
# <a name="ale-layers"></a><span data-ttu-id="74085-103">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="74085-103">ALE Layers</span></span>

<span data-ttu-id="74085-104">Die Durchsetzung der Anwendungsschicht (ALE) besteht aus mehreren Filter Ebenen und vielen übereinstimmenden Verwerfungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="74085-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="74085-105">Alle Windows Filtering Platform (WFP)-Filter-Engine-Ebenen (einschließlich ALE) werden unter [**Filtern von ebenenbezeichern**](management-filtering-layer-identifiers-.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="74085-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="74085-106">Dieses Thema enthält eine ausführlichere Beschreibung der Filter Ebenen, die Teil von ALE sind.</span><span class="sxs-lookup"><span data-stu-id="74085-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="74085-107">Ressourcen \_ Zuweisung</span><span class="sxs-lookup"><span data-stu-id="74085-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="74085-108">Ein Filter auf der Ebene der Ebene der [**\_ Ebene der Ebene der \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) wird für Netzwerk Bindungs Vorgänge, explizit oder implizit, abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="74085-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="74085-109">Wenn ein Filter auf dieser Ebene mit der Autorisierung der rohsocket Erstellung übereinstimmt, wird das FWP-Bedingungs Kennzeichen festgelegt. [**\_ \_ \_ \_ \_**](filtering-condition-flags-.md)</span><span class="sxs-lookup"><span data-stu-id="74085-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="74085-110">Wenn ein Filter auf dieser Ebene mit dem Autorisierungs Modus für den gemischten-Modus übereinstimmt, wird das Feld [**FWP Condition ALE in der "FWP \_ Condition \_ ALE \_ \_**](filtering-condition-identifiers-.md) " auf "sio \_ rcvall" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74085-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="74085-111">Eine Beschreibung von "sio \_ rcvall" finden Sie unter [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="74085-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="74085-112">Dies ist die einzige Schicht, in der der gemischten-Modus gefiltert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74085-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="74085-113">Wenn während **Bind ()** kein Port angegeben ist, d. h., Port wird auf 0 (null) festgelegt, dann wählt der TCP/IP-Stapel einen Port aus dem dynamischen Port Bereich aus (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="74085-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="74085-114">Der ausgewählte Port wird auf dieser Ebene klassifiziert, und das FWP-Bedingungs Kennzeichen ist ein Platzhalter- [**\_ \_ \_ \_ \_ Bindungsflag**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="74085-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="74085-115">Wenn die lokale Adresse nicht im [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) -Befehl angegeben ist, wird das Feld für die lokale Adresse auf [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74085-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="74085-116">auth \_ lauschen</span><span class="sxs-lookup"><span data-stu-id="74085-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="74085-117">Bei TCP-Abhör aufrufen [**()**](/windows/desktop/api/winsock2/nf-winsock2-listen) wird ein Filter auf der Ebene der Ebene " [**lwpm \_ Layer ALE auth" der Ebene " \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) " abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="74085-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="74085-118">Autorisierung über \_ \_ nehmen</span><span class="sxs-lookup"><span data-stu-id="74085-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="74085-119">Ein Filter auf der Ebene der swpm-Layer-ALE-Authentifizierungs-e/A-Version " [**\_ \_ \_ \_ \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) " wird für TCP- [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Aufrufe mit einem eindeutigen ICMP-Paket (Unicast) aus einem eindeutigen Remote Adress-/porttupel und für erste eingehende nicht Fehler-ICMP-Nachrichten (Unicast) mit einem eindeutigen IC</span><span class="sxs-lookup"><span data-stu-id="74085-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="74085-120">Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.</span><span class="sxs-lookup"><span data-stu-id="74085-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="74085-121">Von unformatierten Sockets empfangene TCP-Pakete werden ähnlich wie UDP-Datenverkehr behandelt.</span><span class="sxs-lookup"><span data-stu-id="74085-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="74085-122">Das heißt, dass nur das erste TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und das erste TCP- [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) über Unformatierte Sockets gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="74085-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="74085-123">Authentifizierung \_ herstellen</span><span class="sxs-lookup"><span data-stu-id="74085-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="74085-124">Bei TCP [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) -aufrufen wird ein Filter auf der [**fwpm \_ Layer ALE-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) für die ersten UDP-Pakete, die an eine eindeutige Remote Adresse und einen Port-Tupel gesendet werden, sowie für erste ausgehende, nicht Fehler-ICMP-Nachrichten mit einem eindeutigen ICMP-Typ, Code und der ID abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="74085-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="74085-125">Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.</span><span class="sxs-lookup"><span data-stu-id="74085-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="74085-126">Von rohsockets gesendete TCP-Pakete werden ähnlich wie UDP-Datenverkehr behandelt.</span><span class="sxs-lookup"><span data-stu-id="74085-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="74085-127">Das heißt, dass nur das erste TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und das erste TCP- [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) über Unformatierte Sockets gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="74085-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="74085-128">Flow \_ eingerichtet</span><span class="sxs-lookup"><span data-stu-id="74085-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="74085-129">Nach erfolgreichem Abschluss eines TCP-drei-Wege-Handshakes wird ein Filter auf der Ebene der auf dem [**WPM- \_ Schicht eingerichteten Ebene, der die \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) -Schicht erreicht hat</span><span class="sxs-lookup"><span data-stu-id="74085-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="74085-130">Bei nicht-TCP-Datenverkehr wird der Filter unmittelbar nach dem Abgleich von Filtern von Authentifizierungs-oder Authentifizierungs **\_ Verbindungs** Ebenen abgeglichen. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="74085-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="74085-131">Ein Filter auf dieser Ebene sollte weder Block noch zulassen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="74085-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="74085-132">Diese Ebene wird von Legenden Treibern verwendet, um den Verbindungsstatus zu verfolgen, der in der Dokumentation zum [Windows-Treiberkit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) ausführlich beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="74085-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="74085-133">Ressourcen \_ Freigabe</span><span class="sxs-lookup"><span data-stu-id="74085-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="74085-134">Nach dem Freigeben von Ressourcen, die über die **Ressourcen \_ Zuweisung** zugewiesen wurden, wird ein Filter auf der Ebene der Ebene der Ebene der [**Ebene der Ebene der Ebene der Ebene " \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) " zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="74085-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="74085-135">Endpunkt \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="74085-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="74085-136">Beim Schließen eines verbundenen TCP-Flows oder eines UDP-Sockets-Endpunkts wird ein Filter auf der Ebene des SWF- [**Endpunkts der swpm-Ebene für den \_ \_ \_ Endpunkt \_ \_ \|**](management-filtering-layer-identifiers-.md) geschlossen.</span><span class="sxs-lookup"><span data-stu-id="74085-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="74085-137">\_Umleitung verbinden</span><span class="sxs-lookup"><span data-stu-id="74085-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="74085-138">Ein Filter auf der Ebene der Ebene der [**swpm-Schicht für die \_ \_ \_ Verbindungs \_ Umleitung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung von Remote Adressen und Ports.</span><span class="sxs-lookup"><span data-stu-id="74085-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="74085-139">Die ausgehende Verbindung wird für die Dauer der Verbindung umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74085-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="74085-140">\_Umleitung binden</span><span class="sxs-lookup"><span data-stu-id="74085-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="74085-141">Ein Filter auf der Ebene der Ebene der [**swpm-Ebene der EM- \_ \_ \_ Bindungs \_ Umleitung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung der lokalen Adresse und Ports des zugrunde liegenden Sockets.</span><span class="sxs-lookup"><span data-stu-id="74085-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="74085-142">Der lokale Socket wird für die Lebensdauer des Sockets umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74085-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="74085-143">ALE Verwerfen von Ebenen</span><span class="sxs-lookup"><span data-stu-id="74085-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="74085-144">Für jede der oben beschriebenen ALE-Ebenen enthält die Filter-Engine eine passende Verwerfungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="74085-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="74085-145">Die ALE-Verwerfungs Ebenen werden von Legenden für Protokollierungs Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="74085-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="74085-146">Pakete und Hinweise, die auf einer der ALE-Filter Ebenen verworfen wurden, werden der entsprechenden ALE-verworfungs Schicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74085-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74085-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74085-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74085-148">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="74085-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="74085-149">Status behaftete ALE Filterung</span><span class="sxs-lookup"><span data-stu-id="74085-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="74085-150">ALE Multicast-/Broadcast Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="74085-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="74085-151">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="74085-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="74085-152">Anpassung des ALE-Flows</span><span class="sxs-lookup"><span data-stu-id="74085-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="74085-153">TCP-paketflows</span><span class="sxs-lookup"><span data-stu-id="74085-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="74085-154">UDP-paketflows</span><span class="sxs-lookup"><span data-stu-id="74085-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="74085-155">Winsock-Funktionen</span><span class="sxs-lookup"><span data-stu-id="74085-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="74085-156">**Filtern von Bedingungs Flags**</span><span class="sxs-lookup"><span data-stu-id="74085-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="74085-157">**Filterbedingungen, die auf jeder Filter Ebene verfügbar sind**</span><span class="sxs-lookup"><span data-stu-id="74085-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 