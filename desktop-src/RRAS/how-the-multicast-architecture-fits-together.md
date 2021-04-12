---
title: Kombinieren der Multicast Architektur
description: In diesem Abschnitt wird eine Beispielkonfiguration und die Kombinieren der Hauptkomponenten beschrieben.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207003"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="ed53a-103">Kombinieren der Multicast Architektur</span><span class="sxs-lookup"><span data-stu-id="ed53a-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="ed53a-104">In diesem Abschnitt wird eine Beispielkonfiguration und die Kombinieren der Hauptkomponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed53a-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="ed53a-105">Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.</span><span class="sxs-lookup"><span data-stu-id="ed53a-105">The following illustration shows the relationship between the various components of a router.</span></span>

![Beziehung zwischen Komponenten des Windows 2000-Routers](images/mrarch1.png)

<span data-ttu-id="ed53a-107">Der Multicast-Gruppen-Manager ist Teil des RRAS-Dienstanbieter, der auf einem Server ausgeführt wird, der als Router betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ed53a-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="ed53a-108">Der angezeigte Router verfügt über drei Multicast Routing Protokolle (Protokoll 1, Protokoll 2, Protokoll 3), die darauf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ed53a-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="ed53a-109">Jedes Protokoll kann eine oder mehrere Schnittstellen besitzen (in dieser Abbildung besitzt Protokoll 1 Schnittstelle 1, Protokoll 2 besitzt Schnittstelle 2, und Protokoll 3 besitzt Schnittstelle 3).</span><span class="sxs-lookup"><span data-stu-id="ed53a-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="ed53a-110">Jede Schnittstelle kann nur im Besitz eines Routing Protokolls sein (zusätzlich zu IGMP, was ein Sonderfall ist).</span><span class="sxs-lookup"><span data-stu-id="ed53a-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="ed53a-111">Der Multicast-Gruppen-Manager wird auf dem Router ausgeführt und koordiniert die Verteilung der Gruppeninformationen zwischen den Routing Protokollen.</span><span class="sxs-lookup"><span data-stu-id="ed53a-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="ed53a-112">Die folgende Abbildung zeigt die Beziehung zwischen zwei Routern in einer Multicast Architektur.</span><span class="sxs-lookup"><span data-stu-id="ed53a-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![Beziehung zwischen zwei Routern in der Multicast Architektur](images/mrarch2.png)

<span data-ttu-id="ed53a-114">In der vorherigen Abbildung sendet Router 2 eine Multicast Nachricht an Netzwerk 2 an Schnittstelle 3.</span><span class="sxs-lookup"><span data-stu-id="ed53a-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="ed53a-115">Router 1 empfängt die Multicast Nachricht von Netzwerk 2 an Schnittstelle 3.</span><span class="sxs-lookup"><span data-stu-id="ed53a-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="ed53a-116">Auf beiden Routern besitzt Protokoll 3 die jeweilige Schnittstelle 3.</span><span class="sxs-lookup"><span data-stu-id="ed53a-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="ed53a-117">Die folgende Abbildung zeigt den Pfad einer Nachricht von einer Multicast Quelle (an eine Multicast Gruppe), um den Host zu erreichen, der der Multicast Gruppe beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ed53a-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="ed53a-118">Die Router in der Abbildung verwenden die gleiche Konfiguration wie vorherige Abbildungen. die Schnittstellen-und Protokoll Details werden jedoch nicht angezeigt, um die Abbildung einfach zu halten.</span><span class="sxs-lookup"><span data-stu-id="ed53a-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![der Pfad der Nachricht von der Multicast Quelle zum Zielhost.](images/mrarch3.png)

<span data-ttu-id="ed53a-120">Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn ein Host einer Multicast Gruppe Beitritt.</span><span class="sxs-lookup"><span data-stu-id="ed53a-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="ed53a-121">Informationen zu den Beziehungen zwischen den verschiedenen Entitäten finden Sie in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="ed53a-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="ed53a-122">Host 1 wird der Multicast Gruppe G in Netzwerk 3 beitreten.</span><span class="sxs-lookup"><span data-stu-id="ed53a-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="ed53a-123">Router 3 erfährt ungefähr G über IGMP.</span><span class="sxs-lookup"><span data-stu-id="ed53a-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="ed53a-124">Der Multicast-Gruppen-Manager auf Router 3 benachrichtigt Protokoll 3 auf Router 3, dass neue Empfänger für G vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ed53a-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="ed53a-125">Protokoll 3 auf Router 3 benachrichtigt dann Protokoll 3 auf Router 1 über G.</span><span class="sxs-lookup"><span data-stu-id="ed53a-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="ed53a-126">Das Protokoll 3 auf Router 1 benachrichtigt wiederum den Multicast-Gruppen-Manager auf Router 1 über G.</span><span class="sxs-lookup"><span data-stu-id="ed53a-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="ed53a-127">Der Multicast-Gruppen-Manager auf Router 1 benachrichtigt dann Protokoll 1 und Protokoll 2 über G.</span><span class="sxs-lookup"><span data-stu-id="ed53a-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="ed53a-128">In Protokoll 2 kann Router 2 über G informiert werden, wenn das Protokoll dafür konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed53a-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="ed53a-129">Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn eine Nachricht an eine Multicast Gruppe gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed53a-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="ed53a-130">Informationen zu den Beziehungen zwischen den verschiedenen Entitäten finden Sie in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="ed53a-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="ed53a-131">Eine Quelle in Netzwerk 1 sendet eine Nachricht an die Gruppe G.</span><span class="sxs-lookup"><span data-stu-id="ed53a-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="ed53a-132">Die von Quelldateien gesendete Nachricht wechselt zunächst zu Router 2, der Sie dann mithilfe von Schnittstelle 2 an Router 1 weiterleitet (da Router 2 von Protokoll 2 informiert wurde, dass Empfänger nach dem downstreamvorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="ed53a-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="ed53a-133">Router 1 leitet die Nachricht an Router 3 weiter (da Router 1 von Protokoll 2 informiert wurde, dass die Empfänger nach dem Downstreamdienst vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="ed53a-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="ed53a-134">Router 3 leitet die Nachricht an Netzwerk 3 weiter und wird daher bei Host 1 eintreffen.</span><span class="sxs-lookup"><span data-stu-id="ed53a-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="ed53a-135">Weitere Informationen zur Multicast Routing Protokoll-Interaktion finden Sie unter [RFC 2715](routing-protocols-request-for-comments.md), Interoperabilitäts Regeln für Multicast Routing Protokolle.</span><span class="sxs-lookup"><span data-stu-id="ed53a-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




