---
title: TCP-paketflows
description: Die Reihenfolge, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen TCP-Sitzung durchlaufen werden.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947887"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="2857a-103">TCP-paketflows</span><span class="sxs-lookup"><span data-stu-id="2857a-103">TCP Packet Flows</span></span>

<span data-ttu-id="2857a-104">In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen TCP-Sitzung durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="2857a-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="2857a-105">Bei TCP-Paket Flüssen für IPv6 folgt dasselbe Muster wie für IPv4.</span><span class="sxs-lookup"><span data-stu-id="2857a-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="2857a-106">Nicht-TCP-Paket Flüsse folgen dem gleichen Muster wie [UDP-paketflows](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="2857a-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="2857a-107">TCP-Verbindungs Einrichtung</span><span class="sxs-lookup"><span data-stu-id="2857a-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="2857a-108">Der Server (Empfänger) führt ein passives öffnen aus.</span><span class="sxs-lookup"><span data-stu-id="2857a-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="2857a-109">BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="2857a-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2857a-110">BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"</span><span class="sxs-lookup"><span data-stu-id="2857a-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="2857a-111">lauschen: lwpm \_ Layer \_ ALE \_ auth \_ hört \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="2857a-112">Der Client (Absender) führt aktive offene Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="2857a-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="2857a-113">BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="2857a-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2857a-114">BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"</span><span class="sxs-lookup"><span data-stu-id="2857a-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="2857a-115">Verbindung: swpm \_ -Schicht- \_ \_ Verbindungs \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="2857a-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2857a-116">verbinden: f-v-Schicht-Authentifizierung \_ \_ \_ \_ Connect \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="2857a-117">SYN: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-118">SYN: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2857a-119">Server</span><span class="sxs-lookup"><span data-stu-id="2857a-119">Server</span></span>

-   <span data-ttu-id="2857a-120">SYN: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-121">SYN: WPM- \_ Schicht \_ eingehender \_ Transport \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-122">SYN: Abbild-e/a- \_ Ebene der \_ \_ \_ v \_ \_ -Version</span><span class="sxs-lookup"><span data-stu-id="2857a-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2857a-123">SYN-ACK: \_ \_ ausgehender \_ Transport-Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-124">SYN-ACK: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2857a-125">Client</span><span class="sxs-lookup"><span data-stu-id="2857a-125">Client</span></span>

-   <span data-ttu-id="2857a-126">SYN-ACK: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-127">SYN-ACK: WPM- \_ Schicht \_ eingehender \_ Transport \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-128">Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="2857a-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="2857a-129">ACK: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-130">ACK: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2857a-131">Server</span><span class="sxs-lookup"><span data-stu-id="2857a-131">Server</span></span>

-   <span data-ttu-id="2857a-132">ACK: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-133">Bestätigung: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-134">Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="2857a-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="2857a-135">Lauschen ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2857a-135">Listen completes.</span></span> <span data-ttu-id="2857a-136">Der Server kann eine Annahme durchführen.</span><span class="sxs-lookup"><span data-stu-id="2857a-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="2857a-137">TCP-SYN empfangen, ohne dass der Port oder das Protokoll überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2857a-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="2857a-138">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="2857a-138">Server (receiver)</span></span>

-   <span data-ttu-id="2857a-139">SYN: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-140">SYN: WPM- \_ Schicht \_ eingehender \_ Transport \_ V4 \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="2857a-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="2857a-141">RST: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-142">RST: WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="2857a-143">TCP-SYN ohne Endpunkt wird bei Transport verwerfen mit einem bestimmten Fehlerzustand angegeben.</span><span class="sxs-lookup"><span data-stu-id="2857a-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="2857a-144">Blockieren Sie dieses Paket bei Transport verwerfen, damit der Stapel nicht das entsprechende Ereignis (RST) sendet.</span><span class="sxs-lookup"><span data-stu-id="2857a-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="2857a-145">Ein Beispiel für die Filterung im Geheimnis Modus finden Sie unter [verhindern von Port Scans](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="2857a-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="2857a-146">Über eine TCP-Verbindung übertragene Daten</span><span class="sxs-lookup"><span data-stu-id="2857a-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="2857a-147">Client (Absender)</span><span class="sxs-lookup"><span data-stu-id="2857a-147">Client (sender)</span></span>

-   <span data-ttu-id="2857a-148">Send</span><span class="sxs-lookup"><span data-stu-id="2857a-148">send</span></span>
-   <span data-ttu-id="2857a-149">Daten: WPM \_ Layer \_ Stream \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="2857a-150">TCP-Segmente: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-151">IP-Datagramme: WPM-Ebene ausgehend von \_ \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2857a-152">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="2857a-152">Server (receiver)</span></span>

-   <span data-ttu-id="2857a-153">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-154">TCP-Segmente: \_ \_ eingehender \_ Transport \_ der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-155">Daten: WPM \_ Layer \_ Stream \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="2857a-156">Daten sind zum Lesen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2857a-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="2857a-157">Erfolgreiche erneute Autorisierung eines TCP-Pakets</span><span class="sxs-lookup"><span data-stu-id="2857a-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="2857a-158">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="2857a-158">Server (receiver)</span></span>

-   <span data-ttu-id="2857a-159">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-160">TCP-Segment: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-161">TCP-Segment: Abbild-e/a-Version der Abbild Version \_ \_ \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2857a-162">Daten: WPM- \_ \_ ebenenstream \_ V4 (eingehend)</span><span class="sxs-lookup"><span data-stu-id="2857a-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="2857a-163">Fehler bei der erneuten Autorisierung eines TCP-Pakets.</span><span class="sxs-lookup"><span data-stu-id="2857a-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="2857a-164">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="2857a-164">Server (receiver)</span></span>

-   <span data-ttu-id="2857a-165">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2857a-166">TCP-Segment: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="2857a-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2857a-167">TCP-Segment: Abbild-e/a-Version der Abbild Version \_ \_ \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2857a-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2857a-168">TCP-Segment: f-v-Ebene der Abbild \_ \_ \_ \_ \_ Annahme \_ \_</span><span class="sxs-lookup"><span data-stu-id="2857a-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="2857a-169">Beenden der TCP-Verbindung</span><span class="sxs-lookup"><span data-stu-id="2857a-169">TCP Connection Termination</span></span>

<span data-ttu-id="2857a-170">Die Beendigung der TCP-Verbindung wird in keiner WFP-Schicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="2857a-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2857a-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2857a-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2857a-172">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="2857a-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="2857a-173">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="2857a-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




