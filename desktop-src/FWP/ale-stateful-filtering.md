---
title: Status behaftete ALE Filterung
description: Filter, die auf der Ebene (Application Layer Enforcement) der Windows-Filter Plattform (WFP) installiert sind, führen eine Zustands behaftete Netzwerk Filterung durch.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038987"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="ee42d-103">Status behaftete ALE Filterung</span><span class="sxs-lookup"><span data-stu-id="ee42d-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="ee42d-104">Filter, die auf der Ebene (Application Layer Enforcement) der Windows-Filter Plattform (WFP) installiert sind, führen eine Zustands behaftete Netzwerk Filterung durch.</span><span class="sxs-lookup"><span data-stu-id="ee42d-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="ee42d-105">Ein *ALE Datenfluss* wird als Grundlage für die Zustands behaftete ALE-Filterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee42d-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="ee42d-106">Ein ALE Fluss ist eine Möglichkeit zur Klassifizierung von Netzwerk Datenverkehr, indem er basierend auf einer Quell-IP-Adresse, einer Ziel-IP-Adresse, einem Quellport, einem Zielport und einem Protokoll gruppiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee42d-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="ee42d-107">Ein ALE-Datenfluss könnte generisch sein, d. h. mindestens einer der Deskriptoren kann alles (oder Platzhalter Zeichen \* ) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ee42d-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="ee42d-108">Beispielsweise würde ein generischer UDP-ALE-Datenfluss als Quell-IP-Adresse = \* , Ziel-IP-Adresse = \* , Quellport = \* , Zielport = \* und Protokoll = UDP beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ee42d-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="ee42d-109">Nachdem eine Verbindung autorisiert wurde (eingehende Verbindungen werden auf der Ebene der BPM-Schicht der Ebene [**\_ \_ \_ auth \_ recv \_ akzeptieren \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ) und ausgehende Verbindungen auf der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene ein ALE Datenfluss wird so erstellt, dass bei einer Richtlinien Änderung alle Pakete, die ein-und ausgehenden Datenverkehr aufweisen und zum gleichen ALE Datenfluss gehören, automatisch zugelassen werden. **\_ \_ \_ \_ \_ \|**</span><span class="sxs-lookup"><span data-stu-id="ee42d-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="ee42d-110">Da eine Richtlinien Änderung möglicherweise die Blockierung zuvor zulässiger Verbindungen erfordert, müssen bei einer Richtlinien Änderung eine [erneute Autorisierung](ale-re-authorization.md) durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee42d-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="ee42d-111">Die Zustands behaftete ALE-Filterung reduziert die Anzahl der erforderlichen Klassifizierungen drastisch, indem nur das erste Paket klassifiziert wird, das zu einem ALE-Datenfluss gehört.</span><span class="sxs-lookup"><span data-stu-id="ee42d-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="ee42d-112">Im Vergleich dazu erfordert eine nicht Zustands behaftete Filterung die Klassifizierung jedes Pakets, das das Netzwerk durchläuft.</span><span class="sxs-lookup"><span data-stu-id="ee42d-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="ee42d-113">Ein ALE-Datenfluss hat eine zugeordnete Richtung, die die Richtung des ersten Pakets des Flows ist.</span><span class="sxs-lookup"><span data-stu-id="ee42d-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="ee42d-114">Dies ermöglicht flexiblere Richtlinien, indem es eingehende initiierte Verbindungen zulässt, dass Sie über unterschiedliche Richtlinien von ausgehenden, initiierten Verbindungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="ee42d-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="ee42d-115">TCP-ALE-Fluss</span><span class="sxs-lookup"><span data-stu-id="ee42d-115">TCP ALE Flow</span></span>

<span data-ttu-id="ee42d-116">Ein ALE Datenverkehr für TCP-Datenverkehr wird durch das fünf-Tupel von TCP/IP (Quell-IP-Adresse, Ziel-IP-Adresse, Quellport, Zielport und Protokoll) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ee42d-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="ee42d-117">Ein TCP-ALE-Datenfluss hat die gleiche Lebensdauer wie ein verbundener TCP-Socket.</span><span class="sxs-lookup"><span data-stu-id="ee42d-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="ee42d-118">Ein verbundener TCP-Socket kann entweder ein mit [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) erstellter Socket oder ein Socket sein, der als Ergebnis eines [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Aufrufes erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee42d-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="ee42d-119">ALE verwaltet eine 1:1-Beziehung zwischen einem TCP-ALE-Datenfluss und einem TCP-Kontroll Block (TCB).</span><span class="sxs-lookup"><span data-stu-id="ee42d-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="ee42d-120">UDP-ALE-Fluss</span><span class="sxs-lookup"><span data-stu-id="ee42d-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="ee42d-121">Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.</span><span class="sxs-lookup"><span data-stu-id="ee42d-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="ee42d-122">Ein ALE Fluss für UDP-Datenverkehr wird durch das fünf-Tupel von TCP/IP identifiziert (Quell-IP-Adresse, Ziel-IP-Adresse, Quellport, Zielport und Protokoll).</span><span class="sxs-lookup"><span data-stu-id="ee42d-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="ee42d-123">Ein UDP-ALE-Datenfluss wird auf Grundlage eines UDP-Sockets erstellt und stellt den Remotepeer dar, mit dem die Anwendung kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="ee42d-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="ee42d-124">Ein Remotepeer wird durch ein Tupel (Ziel-IP-Adresse und Zielport) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ee42d-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="ee42d-125">Zwischen einem UDP-Socket und den Remote Peers, mit denen er kommuniziert, besteht eine 1: n-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="ee42d-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="ee42d-126">Wenn der lokale UDP-Socket geschlossen wird, werden alle damit verknüpften ALE Flows gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee42d-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="ee42d-127">Wenn keine socketabschlüsse vorhanden sind, haben UDP-Unicast-ALE-Flows ein [konfigurierbares](ale-flow-customization.md) Leerlauf Timeout, das standardmäßig 60 Sekunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="ee42d-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="ee42d-128">Wenn in diesem Fenster keine Pakete gesendet oder empfangen werden, wird der ALE Flow gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee42d-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="ee42d-129">Dieses Standard Timeout wird progressiv verkürzt, wenn die Anzahl der von der systemweiten ALE-Abläufe einen bestimmten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="ee42d-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="ee42d-130">ICMP-ALE-Datenfluss</span><span class="sxs-lookup"><span data-stu-id="ee42d-130">ICMP ALE Flow</span></span>

<span data-ttu-id="ee42d-131">Ein ALE Fluss für ICMP-Datenverkehr wird durch das sechs-Tupel (Quell-IP-Adresse, Ziel-IP-Adresse, ICMP-Typ, ICMP-Code, Protokoll und ICMP-ID) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ee42d-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="ee42d-132">Die ICMP-ID ist Teil des ALE-Flows nur für ICMP-Echo-/Antwort-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="ee42d-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="ee42d-133">Wenn keine socketsperrungen vorhanden sind, haben ICMP-Unicast-ALE-Flows ein [konfigurierbares](ale-flow-customization.md) Leerlauf Timeout, das standardmäßig 60 Sekunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="ee42d-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="ee42d-134">Wenn in diesem Fenster keine Pakete gesendet oder empfangen werden, wird der ALE Flow gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee42d-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="ee42d-135">Dieses Standard Timeout wird progressiv verkürzt, wenn die Anzahl der von der systemweiten ALE-Abläufe einen bestimmten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="ee42d-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="ee42d-136">Nur ICMP-Fehlermeldungen, die nicht fehlerhaft sind, werden für ALE Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee42d-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="ee42d-137">ICMP-Fehlermeldungen können auf ICMP- \_ Fehler Ebenen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ee42d-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee42d-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee42d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee42d-139">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="ee42d-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="ee42d-140">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="ee42d-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ee42d-141">ALE Multicast-/Broadcast Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="ee42d-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="ee42d-142">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="ee42d-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ee42d-143">Anpassung des ALE-Flows</span><span class="sxs-lookup"><span data-stu-id="ee42d-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="ee42d-144">TCP-paketflows</span><span class="sxs-lookup"><span data-stu-id="ee42d-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="ee42d-145">UDP-paketflows</span><span class="sxs-lookup"><span data-stu-id="ee42d-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="ee42d-146">Winsock-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee42d-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 