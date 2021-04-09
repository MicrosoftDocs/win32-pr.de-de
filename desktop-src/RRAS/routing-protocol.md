---
title: Routing Protokoll
description: Bei einem Routing Protokoll handelt es sich um einen Clienttyp, der beim Routing Tabellen-Manager registriert wird. Router verwenden Routing Protokolle zum Austauschen von Informationen zu Routen zu einem Ziel.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036867"
---
# <a name="routing-protocol"></a><span data-ttu-id="d6fa2-104">Routing Protokoll</span><span class="sxs-lookup"><span data-stu-id="d6fa2-104">Routing Protocol</span></span>

<span data-ttu-id="d6fa2-105">Bei einem Routing Protokoll handelt es sich um einen Clienttyp, der beim Routing Tabellen-Manager registriert wird.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-105">A routing protocol is a type of client that registers with the routing table manager.</span></span> <span data-ttu-id="d6fa2-106">Router verwenden Routing Protokolle zum Austauschen von Informationen zu Routen zu einem Ziel.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-106">Routers use routing protocols to exchange information regarding routes to a destination.</span></span>

<span data-ttu-id="d6fa2-107">Routing Protokolle sind entweder Unicast oder Multicast.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-107">Routing protocols are either unicast or multicast.</span></span> <span data-ttu-id="d6fa2-108">Routing Protokolle ankündigen Routen zu einem Ziel.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-108">Routing protocols advertise routes to a destination.</span></span>

<span data-ttu-id="d6fa2-109">Eine unicastroute zu einem Ziel wird von einem Unicastrouting-Protokoll verwendet, um Unicastdaten an dieses Ziel weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-109">A unicast route to a destination is used by a unicast routing protocol to forward unicast data to that destination.</span></span> <span data-ttu-id="d6fa2-110">Beispiele für Unicast-Routing Protokolle sind: Routing Information Protocol (RIP), Open kürzeste Path First (OSPF) und Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-110">Examples of unicast routing protocols include: Routing Information Protocol (RIP), Open Shortest Path First (OSPF), and Border Gateway Protocol (BGP).</span></span>

<span data-ttu-id="d6fa2-111">Eine Multicast Route zu einem Ziel wird von einigen Multicast Routing Protokollen verwendet, um die Informationen zu erstellen, die zum Weiterleiten von Multicast Daten von Hosts im Zielnetzwerk der Route verwendet werden (als umgekehrte Pfad Weiterleitung bezeichnet). Beispiele für Multicast-Routing Protokolle: Multicast Open kürzeste Path First (MUF), Distance Vector Multicast Routing Protocol (DVMRP) und Protocol Independent Multicast (PIM).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-111">A multicast route to a destination is used by some multicast routing protocols to create the information that is used to forward multicast data from hosts on the destination network of the route (known as reverse path forwarding).Examples of multicast routing protocols include: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP), and Protocol Independent Multicast (PIM).</span></span>

<span data-ttu-id="d6fa2-112">Der Routing Tabellen-Manager unterstützt mehrere Instanzen desselben Protokolls (z. b. die Implementierung von OSPF von Microsoft und eine OSPF eines Drittanbieters), die auf dem Router ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-112">The routing table manager supports multiple instances of the same protocol (such as Microsoft's implementation of OSPF and a third-party OSPF) running on the router.</span></span> <span data-ttu-id="d6fa2-113">Dadurch können Router die verschiedenen Funktionen jeder Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-113">This allows routers to use the different capabilities of each version.</span></span> <span data-ttu-id="d6fa2-114">Diese Protokolle verfügen über unterschiedliche Protokoll Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-114">These protocols have different protocol identifiers.</span></span>

<span data-ttu-id="d6fa2-115">Protokoll Bezeichner bestehen aus einer Hersteller-ID und einem Protokoll spezifischen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-115">Protocol identifiers are comprised of a vendor identifier and a protocol-specific identifier.</span></span> <span data-ttu-id="d6fa2-116">Der Protokoll spezifische Bezeichner ist für verschiedene Implementierungen des Protokolls identisch, wie z. b. die Implementierung von OSPF von Microsoft und die Implementierung von OSPF von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-116">The protocol-specific identifier is the same for different implementations of the protocol, such as Microsoft's implementation of OSPF and a third-party implementation of OSPF.</span></span> <span data-ttu-id="d6fa2-117">Nur wenn der Anbieter und die Protokoll spezifischen Bezeichner kombiniert werden, gibt es einen eindeutigen Bezeichner für ein Routing Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-117">Only when the vendor and protocol-specific identifiers are combined is there a unique identifier for a routing protocol.</span></span>

<span data-ttu-id="d6fa2-118">Ein Protokoll mit der gleichen Protokoll Kennung (d. h. dem gleichen Hersteller Bezeichner und Protokoll spezifischen Bezeichner) kann mehrmals beim Routing Tabellen-Manager registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-118">A protocol with the same protocol identifier (that is, the same vendor identifier and protocol-specific identifier) can register with the routing table manager multiple times.</span></span> <span data-ttu-id="d6fa2-119">Jedes Mal wird das Protokoll mithilfe eines anderen protokollinstanzbezeichners registriert.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-119">Each time, the protocol registers using a different protocol instance identifier.</span></span> <span data-ttu-id="d6fa2-120">Beispielsweise kann eine Implementierung von OSPF von einem bestimmten Hersteller als "Vendor-OSPF-1" und "Vendor-OSPF-2" registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-120">For example, an implementation of OSPF from a particular vendor can register as Vendor-OSPF-1 and Vendor-OSPF-2.</span></span> <span data-ttu-id="d6fa2-121">Dies ermöglicht einer bestimmten Protokoll Implementierung, die in der Routing Tabelle beibehaltenen Informationen zu partitionieren.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-121">This enables a specific protocol implementation to partition the information that it keeps in the routing table.</span></span>

 

 




