---
description: Clouds werden von den Peer Gruppierungs-und graphinginfrastrukturen verwendet.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131696"
---
# <a name="clouds"></a><span data-ttu-id="b77cf-103">Clouds</span><span class="sxs-lookup"><span data-stu-id="b77cf-103">Clouds</span></span>

<span data-ttu-id="b77cf-104">Clouds werden von den Peer [Gruppierungs](grouping-api.md) -und [graphinginfrastrukturen](graphing-api.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b77cf-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="b77cf-105">Das [Peer Name Resolution-Protokoll (PNRP)](pnrp-namespace-provider-api.md) identifiziert eine Cloud als Gruppe von Peers, die innerhalb desselben IPv6-Bereichs kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="b77cf-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="b77cf-106">Clouds sind eng mit den IPv6-Bereichen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b77cf-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="b77cf-107">In der folgenden Liste sind einige der eindeutigen Cloud-Features aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b77cf-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="b77cf-108">Eine Cloud wird durch einen Namen identifiziert, und die verfügbaren Clouds können mithilfe von [**wsalookupservicebegin**](pnrp-and-wsalookupservicebegin.md)aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="b77cf-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="b77cf-109">Wenn ein Computer mit dem Internet verbunden ist, ist er Teil einer globalen Cloud, der durch die Zeichenfolge "Global" gekennzeichnet ist \_ .</span><span class="sxs-lookup"><span data-stu-id="b77cf-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="b77cf-110">Wenn ein Computer mit einem oder mehreren LAN (Local Area Networks) verbunden ist, sind für jeden Link individuelle Clouds verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b77cf-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="b77cf-111">Ein Computer kann mit vielen Netzwerken verbunden werden, indem mehrere Netzwerkadapter oder ein virtuelles privates Netzwerk (VPN) verwendet werden. Dies bedeutet, dass ein Computer mit einer Schnittstelle in vielen Clouds sichtbar sein kann.</span><span class="sxs-lookup"><span data-stu-id="b77cf-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="b77cf-112">Sie können PNRP zum Registrieren und Auflösen von Peernamen in einer bestimmten Cloud verwenden.</span><span class="sxs-lookup"><span data-stu-id="b77cf-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



