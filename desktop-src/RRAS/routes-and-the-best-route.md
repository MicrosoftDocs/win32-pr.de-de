---
title: Routen und die beste Route
description: Eine Route ist "\ 0034; Netzwerkpfad \ 0034;". an ein Ziel, dem bestimmte Kosten zugeordnet sind. Die Kosten werden durch die administrative Präferenz und die Protokoll spezifische Metrik repräsentiert. Routen mit geringeren Kosten werden gegenüber allen anderen Routen bevorzugt.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339450"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="21c28-105">Routen und die beste Route</span><span class="sxs-lookup"><span data-stu-id="21c28-105">Routes and the Best Route</span></span>

<span data-ttu-id="21c28-106">Eine Route ist ein "Netzwerkpfad" zu einem Ziel, dem bestimmte Kosten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="21c28-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="21c28-107">Die Kosten werden durch die administrative Präferenz und die Protokoll spezifische Metrik repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="21c28-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="21c28-108">Routen mit geringeren Kosten werden gegenüber allen anderen Routen bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="21c28-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="21c28-109">Ein Routen Eintrag in der Routing Tabelle umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="21c28-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="21c28-110">Ein Handle für das Ziel.</span><span class="sxs-lookup"><span data-stu-id="21c28-110">A handle to the destination</span></span>
-   <span data-ttu-id="21c28-111">Der Besitzer dieser Route.</span><span class="sxs-lookup"><span data-stu-id="21c28-111">The owner of this route</span></span>
-   <span data-ttu-id="21c28-112">Der Nachbar (Peer), der die Routeninformationen bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="21c28-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="21c28-113">Flags, die dem Zustand der Route zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="21c28-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="21c28-114">Der Route zugeordnete Flags</span><span class="sxs-lookup"><span data-stu-id="21c28-114">Flags associated with the route</span></span>
-   <span data-ttu-id="21c28-115">Die bevorzugte und Metrik für die Route</span><span class="sxs-lookup"><span data-stu-id="21c28-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="21c28-116">Die Liste der Sichten, zu denen die Route gehört.</span><span class="sxs-lookup"><span data-stu-id="21c28-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="21c28-117">Informationen, die für den Besitzer der Route privat sind</span><span class="sxs-lookup"><span data-stu-id="21c28-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="21c28-118">Eine Liste der nächsten Hops, die zum Erreichen des Ziels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21c28-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="21c28-119">In den folgenden Werten wird eine Route in der Routing Tabelle eindeutig identifiziert:</span><span class="sxs-lookup"><span data-stu-id="21c28-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="21c28-120">Das Zielnetzwerk</span><span class="sxs-lookup"><span data-stu-id="21c28-120">The destination network</span></span>
-   <span data-ttu-id="21c28-121">Der Besitzer der Route.</span><span class="sxs-lookup"><span data-stu-id="21c28-121">The owner of the route</span></span>
-   <span data-ttu-id="21c28-122">Der Nachbar, der die Route bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="21c28-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="21c28-123">Metriken und Vorlieben</span><span class="sxs-lookup"><span data-stu-id="21c28-123">Metrics and Preference</span></span>

<span data-ttu-id="21c28-124">Jede Route verfügt über eine administrative Präferenz (angegeben durch die Routing Richtlinie) und eine Client abhängige Metrik.</span><span class="sxs-lookup"><span data-stu-id="21c28-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="21c28-125">Der Routing Tabellen-Manager verwendet diese Informationen, um zu bestimmen, welche Route die bessere Route zu einem Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="21c28-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="21c28-126">Routen mit niedrigerer Vorliebe sind bessere Routen (eine niedrigste und somit am besten).</span><span class="sxs-lookup"><span data-stu-id="21c28-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="21c28-127">Wenn zwei Routen die gleiche Einstellung aufweisen, ist die Route mit der niedrigeren Metrik die bessere Route.</span><span class="sxs-lookup"><span data-stu-id="21c28-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="21c28-128">Normalerweise wird eine Route durch die bevorzugte Einstellung des Clients bestimmt, der die Route hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="21c28-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="21c28-129">Allerdings kann für alle Routen, die mithilfe des Netsh.exe Verwaltungs Tools hinzugefügt werden, ein bevorzugter Wert pro Route angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="21c28-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="21c28-130">Preference wird normalerweise verwendet, um die Priorität zwischen Clients anzugeben.</span><span class="sxs-lookup"><span data-stu-id="21c28-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="21c28-131">Ein Administrator kann z. b. OSPF eine niedrigere (bessere) Einstellung als RIP zuweisen.</span><span class="sxs-lookup"><span data-stu-id="21c28-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="21c28-132">In diesem Fall sind OSPF-Routen für das Weiterleiten von Routen vorzuziehen.</span><span class="sxs-lookup"><span data-stu-id="21c28-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




