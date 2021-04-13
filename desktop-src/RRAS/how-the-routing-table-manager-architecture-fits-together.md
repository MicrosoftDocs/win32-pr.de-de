---
title: Kombinieren der Architektur des Routing Tabellen-Managers
description: Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311592"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="dc686-104">Kombinieren der Architektur des Routing Tabellen-Managers</span><span class="sxs-lookup"><span data-stu-id="dc686-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="dc686-105">Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.</span><span class="sxs-lookup"><span data-stu-id="dc686-105">The following illustration shows the relationship between the different components of a router.</span></span>

![Beziehung zwischen Routerkomponenten](images/rtsrvarch.png)

<span data-ttu-id="dc686-107">Wenn der Router bootstrapped ist, wird der routermanager-Dienst sowie ein oder mehrere Routing Protokolle gestartet.</span><span class="sxs-lookup"><span data-stu-id="dc686-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="dc686-108">Routing Protokolle werden den verschiedenen Schnittstellen auf dem Router zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dc686-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="dc686-109">Der routermanager startet auch den Routing Tabellen-Manager.</span><span class="sxs-lookup"><span data-stu-id="dc686-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="dc686-110">Die folgende Abbildung zeigt die Beziehung zwischen Clients und den verschiedenen Komponenten des Routing Tabellen-Managers.</span><span class="sxs-lookup"><span data-stu-id="dc686-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![Beziehung zwischen Clients und Komponenten des Routing Tabellen-Managers](images/rtmentrel.png)

<span data-ttu-id="dc686-112">Der routermanager startet eine oder mehrere Instanzen des Routing Tabellen-Managers.</span><span class="sxs-lookup"><span data-stu-id="dc686-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="dc686-113">Wenn mehrere Instanzen des Routing Tabellen-Managers gestartet werden, wurde der Router so konfiguriert, dass er als ein oder mehrere virtuelle Router fungiert.</span><span class="sxs-lookup"><span data-stu-id="dc686-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="dc686-114">Jede Instanz des Routing Tabellen-Managers besitzt mindestens eine Schnittstelle. jede Schnittstelle kann nur einer Instanz des Routing Tabellen-Managers gehören.</span><span class="sxs-lookup"><span data-stu-id="dc686-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="dc686-115">Jede Instanz des Routing Tabellen-Managers ist unabhängig von den anderen. zwischen den Instanzen werden keine Informationen ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="dc686-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="dc686-116">Jede Instanz des Routing Tabellen-Managers enthält eine oder mehrere Routing Tabellen.</span><span class="sxs-lookup"><span data-stu-id="dc686-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="dc686-117">Jede Routing Tabelle ist einer Adressfamilie zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dc686-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="dc686-118">Jede Routing Tabelle enthält eine oder mehrere Ansichten.</span><span class="sxs-lookup"><span data-stu-id="dc686-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="dc686-119">In diesem Beispiel wird die Routing Tabelle mit einer Unicast-und Multicast Ansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dc686-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="dc686-120">Jede Ansicht ist eine Teilmenge der Routing Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc686-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="dc686-121">Die folgende Abbildung zeigt die Beziehung zwischen Clients und mehreren Instanzen des Routing Tabellen-Managers, Routing Tabellen und Sichten.</span><span class="sxs-lookup"><span data-stu-id="dc686-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![Beziehungs Clients, Routing Tabellen-Manager, Routing Tabellen, Sichten](images/multrtabrel.png)

<span data-ttu-id="dc686-123">Eine Instanz des Clients kann mehrmals bei einer Instanz des Routing Tabellen-Managers registriert werden – einmal pro Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="dc686-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="dc686-124">Ein Client kann sich bei jeder Instanz des Routing Tabellen-Managers registrieren.</span><span class="sxs-lookup"><span data-stu-id="dc686-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="dc686-125">In der folgenden Abbildung wird gezeigt, wie die Routing Tabelleneinträge verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="dc686-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="dc686-126">Weitere Informationen zu Routing Tabellen Einträgen finden Sie unter [Routing Table Entries](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="dc686-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![Beziehung zwischen Routing Tabellen Einträgen](images/nexthop.png)

<span data-ttu-id="dc686-128">Die Routing Tabelle enthält Ziele.</span><span class="sxs-lookup"><span data-stu-id="dc686-128">The routing table contains destinations.</span></span> <span data-ttu-id="dc686-129">Jedes Ziel bezieht sich auf eine oder mehrere Routen.</span><span class="sxs-lookup"><span data-stu-id="dc686-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="dc686-130">Jede Route verfügt über NULL, einen oder mehrere Zeiger auf die nächsten Hops, die der Route zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dc686-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="dc686-131">Jeder Zeiger verweist auf den eigentlichen nächsten Hop in der Liste der nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="dc686-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="dc686-132">Jeder Client, der beim Routing Tabellen-Manager registriert wird, erstellt eine Liste der nächsten Hops, die der Client besitzt.</span><span class="sxs-lookup"><span data-stu-id="dc686-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="dc686-133">Routen können nur Zeiger auf die Liste der nächsten Hops enthalten, die dem Client zugeordnet ist, der die Route besitzt.</span><span class="sxs-lookup"><span data-stu-id="dc686-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




