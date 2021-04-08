---
title: Schnittstelle (RRAS)
description: Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Index identifiziert. Multicast Routing Protokolle (z. b. "MUF") befassen sich ähnlich mit allen Schnittstellentypen.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949316"
---
# <a name="interface-rras"></a><span data-ttu-id="fe43e-105">Schnittstelle (RRAS)</span><span class="sxs-lookup"><span data-stu-id="fe43e-105">Interface (RRAS)</span></span>

<span data-ttu-id="fe43e-106">Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fe43e-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="fe43e-107">Jede Schnittstelle wird durch einen eindeutigen Index identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fe43e-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="fe43e-108">Multicast Routing Protokolle (z. b. "MUF") befassen sich ähnlich mit allen Schnittstellentypen.</span><span class="sxs-lookup"><span data-stu-id="fe43e-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="fe43e-109">Im Fall einer LAN-Schnittstelle entspricht die Schnittstelle einem tatsächlichen physischen Gerät auf dem Computer (dem LAN-Adapter).</span><span class="sxs-lookup"><span data-stu-id="fe43e-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="fe43e-110">Bei einer WAN-Schnittstelle wird die Schnittstelle einem Port zugeordnet, wenn eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe43e-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="fe43e-111">WAN-Schnittstellen können auf Tunneln basieren, und der Port könnte ein VPN-Port (virtuelles privates Netzwerk) sein.</span><span class="sxs-lookup"><span data-stu-id="fe43e-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="fe43e-112">Windows 2000 und spätere Betriebssysteme unterstützen eine Point-to-Multipoint-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fe43e-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="fe43e-113">Diese Art von Schnittstelle kann als eine Auflistung von Punkt-zu-Punkt-Links angezeigt werden, die einen einzelnen Beendigungs Punkt aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe43e-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="fe43e-114">Zur eindeutigen Identifizierung einer exakten Verknüpfung in einer Punkt-zu-Multipoint-Schnittstelle verwendet die MGM-API die Adresse des nächsten Hops der Schnittstellen-ID.</span><span class="sxs-lookup"><span data-stu-id="fe43e-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="fe43e-115">Zur Unterstützung dieser Identifizierung verwendet die MGM-API eine erweiterte Schnittstellen-ID, die eine Adresse für den [nächsten Hop](next-hop.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="fe43e-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




