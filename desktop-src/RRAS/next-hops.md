---
title: Nächste Hops
description: Routen ist mindestens ein nächster Hop zugeordnet.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036441"
---
# <a name="next-hops"></a><span data-ttu-id="1a784-103">Nächste Hops</span><span class="sxs-lookup"><span data-stu-id="1a784-103">Next Hops</span></span>

<span data-ttu-id="1a784-104">Routen ist mindestens ein nächster Hop zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1a784-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="1a784-105">Wenn sich das Ziel nicht in einem direkt verbundenen Netzwerk befindet, ist der nächste Hop die Adresse des nächsten Routers (oder Netzwerks) im ausgehenden Netzwerk, der die Daten am besten an das Ziel weiterleiten kann.</span><span class="sxs-lookup"><span data-stu-id="1a784-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="1a784-106">Die beste Route ist die Route mit den geringsten Kosten, basierend auf der verwendeten Routing Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1a784-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="1a784-107">Jeder nächste Hop kann verwendet werden, um Daten auf dem Pfad an das Ziel weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="1a784-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="1a784-108">Alle Routen im Besitz eines Clients nutzen einen gemeinsamen Satz von Einträgen im nächsten Hop, die vom Client hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="1a784-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="1a784-109">Jeder nächste Hop wird durch die Adresse des nächsten Hops und den Schnittstellen Index, der zum Erreichen des nächsten Hops verwendet wird, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1a784-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="1a784-110">Wenn der nächste Hop selbst nicht direkt verbunden ist, wird er als "Remote" als nächster Hop gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a784-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="1a784-111">In diesem Fall muss die Weiterleitung mithilfe der Netzwerkadresse des nächsten Hops eine weitere Suche durchführen.</span><span class="sxs-lookup"><span data-stu-id="1a784-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="1a784-112">Diese Suche ist erforderlich, um den "lokalen" nächsten Hop zu finden, mit dem der Remote-Hop und das Ziel erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="1a784-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="1a784-113">Ein Eintrag für den nächsten Hop in der Routing Tabelle umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1a784-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="1a784-114">Die Netzwerkadresse des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="1a784-114">The network address of the next hop</span></span>
-   <span data-ttu-id="1a784-115">Der Besitzer des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="1a784-115">The owner of the next hop</span></span>
-   <span data-ttu-id="1a784-116">Der Bezeichner der ausgehenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1a784-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="1a784-117">Der Zustand des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="1a784-117">The state of the next hop</span></span>
-   <span data-ttu-id="1a784-118">Dem nächsten Hop zugeordnete Flags</span><span class="sxs-lookup"><span data-stu-id="1a784-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="1a784-119">Informationen, die für den Besitzer des nächsten Hops privat sind</span><span class="sxs-lookup"><span data-stu-id="1a784-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="1a784-120">Ein Handle für das Ziel, das dem Remote nächsten Hop entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a784-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




