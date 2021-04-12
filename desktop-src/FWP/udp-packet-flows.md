---
title: UDP-paketflows
description: Die Reihenfolge, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen UDP-Sitzung durchlaufen werden.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310695"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="f5510-103">UDP-paketflows</span><span class="sxs-lookup"><span data-stu-id="f5510-103">UDP Packet Flows</span></span>

<span data-ttu-id="f5510-104">In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen UDP-Sitzung durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5510-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="f5510-105">UDP-paketflows für IPv6 folgen dem gleichen Muster wie für IPv4.</span><span class="sxs-lookup"><span data-stu-id="f5510-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5510-106">Alle nicht-TCP-Paket Flüsse folgen dem gleichen Muster wie UDP-paketflows.</span><span class="sxs-lookup"><span data-stu-id="f5510-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="f5510-107">UDP-Verbindungs Einrichtung</span><span class="sxs-lookup"><span data-stu-id="f5510-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="f5510-108">Der Server (Empfänger) führt ein passives öffnen aus.</span><span class="sxs-lookup"><span data-stu-id="f5510-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="f5510-109">BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="f5510-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="f5510-110">BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"</span><span class="sxs-lookup"><span data-stu-id="f5510-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="f5510-111">Der Client (Absender) führt aktive offene Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="f5510-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="f5510-112">BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="f5510-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="f5510-113">BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"</span><span class="sxs-lookup"><span data-stu-id="f5510-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="f5510-114">SendTo: fwpm \_ Layer \_ ALE \_ Verbindungs \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="f5510-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="f5510-115">SendTo: fwpm \_ Layer \_ ALE \_ auth \_ Connect \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="f5510-116">Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="f5510-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="f5510-117">Daten: \_ \_ Datagramm-Daten von Datagramm-Daten, \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="f5510-118">UDP-Meldung: ausgehender Transport-WPM- \_ \_ \_ Transport \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="f5510-119">IP-Datagramme: WPM-Ebene ausgehend von \_ \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="f5510-120">Server</span><span class="sxs-lookup"><span data-stu-id="f5510-120">Server</span></span>

-   <span data-ttu-id="f5510-121">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="f5510-122">UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="f5510-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="f5510-123">UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version</span><span class="sxs-lookup"><span data-stu-id="f5510-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="f5510-124">Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="f5510-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="f5510-125">Daten: \_ \_ Datagramm-Daten von Datagramm-Daten, \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="f5510-126">Es wurde eine UDP-Nachricht empfangen, die nicht auf dem Port oder Protokoll lauscht.</span><span class="sxs-lookup"><span data-stu-id="f5510-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="f5510-127">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="f5510-127">Server (receiver)</span></span>

-   <span data-ttu-id="f5510-128">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="f5510-129">IP-Datagramme: auf der WPM- \_ Schicht \_ eingehende \_ ippacket \_ V4 \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="f5510-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="f5510-130">ICMP dest nicht erreichbar: \_ \_ \_ ICMP- \_ Fehler \_ V4 in fwpm-Schicht</span><span class="sxs-lookup"><span data-stu-id="f5510-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="f5510-131">ICMP dest nicht erreichbar: ausgehender Transport-fwpm- \_ \_ \_ Transport \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="f5510-132">ICMP dest nicht erreichbar: fwpm-Schicht ausgehend von \_ \_ \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="f5510-133">UDP ohne Endpunkt wird mit einem bestimmten Fehlerzustand in "ippacket Discard" angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5510-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="f5510-134">Blockieren Sie dieses Paket bei der "ippacket"-Verwerfungs Methode, damit der Stapel das entsprechende Ereignis nicht sendet (ICMP-Fehler).</span><span class="sxs-lookup"><span data-stu-id="f5510-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="f5510-135">Erfolgreiche erneute Autorisierung eines UDP-Pakets</span><span class="sxs-lookup"><span data-stu-id="f5510-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="f5510-136">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="f5510-136">Server (receiver)</span></span>

-   <span data-ttu-id="f5510-137">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="f5510-138">UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="f5510-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="f5510-139">UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version</span><span class="sxs-lookup"><span data-stu-id="f5510-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="f5510-140">UDP-Nachricht: \_ \_ Datagramm-Datagramm-Datagrammdaten \_ \_ V4 (eingehend)</span><span class="sxs-lookup"><span data-stu-id="f5510-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="f5510-141">Fehler bei der erneuten Autorisierung eines UDP-Pakets.</span><span class="sxs-lookup"><span data-stu-id="f5510-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="f5510-142">Server (Empfänger)</span><span class="sxs-lookup"><span data-stu-id="f5510-142">Server (receiver)</span></span>

-   <span data-ttu-id="f5510-143">IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4</span><span class="sxs-lookup"><span data-stu-id="f5510-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="f5510-144">UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht</span><span class="sxs-lookup"><span data-stu-id="f5510-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="f5510-145">UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version</span><span class="sxs-lookup"><span data-stu-id="f5510-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="f5510-146">UDP-Nachricht: die Standard Authentifizierung der \_ v-Layer- \_ \_ \_ v \_ \_ \_ -Version</span><span class="sxs-lookup"><span data-stu-id="f5510-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="f5510-147">Beenden der UDP-Verbindung</span><span class="sxs-lookup"><span data-stu-id="f5510-147">UDP Connection Termination</span></span>

<span data-ttu-id="f5510-148">Die UDP-Verbindungs Beendigung wird in keiner WFP-Schicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5510-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5510-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5510-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5510-150">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="f5510-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="f5510-151">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="f5510-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




