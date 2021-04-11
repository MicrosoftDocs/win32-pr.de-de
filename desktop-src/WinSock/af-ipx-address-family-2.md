---
description: Die IPX-Adressfamilie definiert die Adressierungs Struktur für Protokolle, die die IPX-Standard socketadressierung verwenden. Für diese Transporte besteht eine Endpunkt Adresse aus einer Netzwerk Nummer, einer Knotenadresse und einer Socketnummer.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX-Adressfamilie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129228"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="cf8b4-104">AF- \_ IPX-Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="cf8b4-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="cf8b4-105">Die IPX-Adressfamilie definiert die Adressierungs Struktur für Protokolle, die die IPX-Standard socketadressierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="cf8b4-106">Für diese Transporte besteht eine Endpunkt Adresse aus einer Netzwerk Nummer, einer Knotenadresse und einer Socketnummer.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="cf8b4-107">Die Netzwerk Nummer ist eine administrative Domäne und benennt in der Regel ein einzelnes Ethernet-oder tokenringsegment.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="cf8b4-108">Die Knotennummer ist die physische Adresse einer Station.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-108">The node number is a station's physical address.</span></span> <span data-ttu-id="cf8b4-109">Die Kombination aus Netz und Knoten bildet eine eindeutige Stationsadresse, die in der Welt als eindeutig angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="cf8b4-110">NET-und Knoten Nummern werden in ASCII-Text entweder in Block-oder gestrichelte Notation wie folgt dargestellt: "0101a040, 00001b498765" oder "01-01-a0-40, 00-00-1B-49-87-65".</span><span class="sxs-lookup"><span data-stu-id="cf8b4-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="cf8b4-111">Führende Nullen müssen nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="cf8b4-112">Die IPX-Socketnummer ist eine Netzwerk-/transportdienstnummer ähnlich einer TCP-Portnummer und sollte nicht mit dem Winsock-socketdeskriptor verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="cf8b4-113">IPX-Socketnummern sind global für die Endstation und können nicht an bestimmte Netzwerk-/Knoten-Adressen gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="cf8b4-114">Wenn die Endstation beispielsweise über zwei Netzwerkschnittstellenkarten verfügt, kann ein gebundener Socket beide Karten senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="cf8b4-115">Insbesondere Datagramm-Sockets würden Broadcast Datagramme auf beiden Karten empfangen.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="cf8b4-116">SOCKADDR \_ IPX beträgt 14 Bytes und ist kürzer als die 16-Byte- [**sockaddr**](sockaddr-2.md) -Referenzstruktur.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="cf8b4-117">IPX/SPX-Implementierungen akzeptieren möglicherweise die Länge von 16 Byte und die tatsächliche Länge.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="cf8b4-118">Wenn Sie sockaddr \_ IPX und eine hart codierte Länge von 16 Bytes verwenden, kann die Implementierung davon ausgehen, dass Sie Zugriff auf die 2 Bytes nach ihrer Struktur hat.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="cf8b4-119">Feld</span><span class="sxs-lookup"><span data-stu-id="cf8b4-119">Field</span></span>           | <span data-ttu-id="cf8b4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cf8b4-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="cf8b4-121">**Sa- \_ Familie**</span><span class="sxs-lookup"><span data-stu-id="cf8b4-121">**sa\_family**</span></span>  | <span data-ttu-id="cf8b4-122">Adressfamilie AF \_ IPX in der Host Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="cf8b4-123">**Sa \_ netnum**</span><span class="sxs-lookup"><span data-stu-id="cf8b4-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="cf8b4-124">IPX-Netzwerk Bezeichner in der Netzwerk Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="cf8b4-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="cf8b4-125">**Sa- \_ nodenum**</span><span class="sxs-lookup"><span data-stu-id="cf8b4-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="cf8b4-126">Station-Knotenadresse, rechts geleert.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="cf8b4-127">**Sa- \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="cf8b4-127">**Sa\_socket**</span></span>  | <span data-ttu-id="cf8b4-128">IPX-Socketnummer in der Netzwerk Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="cf8b4-128">IPX socket number in network order.</span></span>      |



 

 

 



