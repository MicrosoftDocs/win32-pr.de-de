---
title: RPC-Lastenausgleich
description: RPC-Lastenausgleich
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036405"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="a8d63-103">RPC-Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="a8d63-103">RPC Load Balancing</span></span>

<span data-ttu-id="a8d63-104">Der Microsoft RPC-Lastenausgleich soll eine skalierbare Lösung für Szenarien bereitstellen, die eine hohe Auslastung von [RPC-über-HTTP](remote-procedure-calls-using-rpc-over-http.md) -Datenverkehr erfordern.</span><span class="sxs-lookup"><span data-stu-id="a8d63-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="a8d63-105">Der primäre Zweck des RPC-Load Balancer besteht darin sicherzustellen, dass der RPC-/HTTP-Datenverkehr von einer Serverfarm gewartet werden kann, um die Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="a8d63-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="a8d63-106">Um dies zu erreichen, muss RPC sicherstellen, dass alle Verbindungen von einem Client Prozess durch denselben Server Endpunkt in der Serverfarm gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="a8d63-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="a8d63-107">Der RPC-Load Balancer wird als Dienst implementiert, der in Verbindung mit dem RPC-über-HTTP-Proxy Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8d63-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="a8d63-108">Um den Lastenausgleich zu ermöglichen, kommuniziert der RPC-Lasten Ausgleichs Dienst, der auf den einzelnen Servern ausgeführt wird, miteinander, um den bevorzugten Server für die anfängliche Client Verbindung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a8d63-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="a8d63-109">Dieser Vorgang wird als "Schiedsgerichtsbarkeit" bezeichnet und erfolgt zum Zeitpunkt der anfänglichen Client Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a8d63-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="a8d63-110">Um den Server übergreifenden Datenverkehr zu reduzieren, wählt der RPC-Lasten Ausgleichs Dienst den lokalen Endpunkt aus, um die Verbindung zu bedienen, wenn der Client nicht bereits einem Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a8d63-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="a8d63-111">Bei einer bestimmten Client Verbindung besteht das Ergebnis einer-Vermittlung aus zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="a8d63-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="a8d63-112">Wenn der Client bereits eine Verbindung hergestellt hat, verarbeitet der Server, auf dem die Verbindung zum ersten Mal empfangen wird, die nachfolgenden Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="a8d63-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="a8d63-113">Wenn es sich um die erste Verbindung vom Client handelt, führt die-Vermittlung dazu, dass der lokale Server die Verbindung und somit alle Verbindungen vom Client verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a8d63-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="a8d63-114">Diese Informationen werden nach der Festlegung an die anderen RPC-Load Balancer Dienste in der Serverfarm committet, sodass Sie von dem Server informiert werden, der alle Anforderungen des Clients verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a8d63-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="a8d63-115">Dieser Abschnitt bietet eine Übersicht über den RPC-Lastenausgleich in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a8d63-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="a8d63-116">Bereitstellen des Lasten Ausgleichs</span><span class="sxs-lookup"><span data-stu-id="a8d63-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="a8d63-117">Konfigurieren des Lasten Ausgleichs</span><span class="sxs-lookup"><span data-stu-id="a8d63-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="a8d63-118">Bewährte Methoden für den Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="a8d63-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="a8d63-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8d63-119">Requirements</span></span>

<span data-ttu-id="a8d63-120">Der RPC-Lasten Ausgleichs Dienst wird auf Servern unterstützt, auf denen Windows Server 2008 R2 oder höher ausgeführt wird, sowie auf Clients, auf denen Windows 7 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8d63-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="a8d63-121">Der RPC-Proxy Dienst, der RPC-Lasten Ausgleichs Dienst und die Server Endpunkte müssen alle auf dem gleichen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a8d63-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="a8d63-122">Außerdem müssen alle Server in der Serverfarm in der Lage sein, den angeforderten Endpunkt zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8d63-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="a8d63-123">Informationen zum Konfigurieren des RPC-Proxy diensdienstanbieter und des RPC-Lasten Ausgleichs Dienstanbieter finden Sie unter [Konfigurieren von Computern für RPC über HTTP](configuring-computers-for-rpc-over-http.md) und [Konfigurieren des Lasten Ausgleichs](configuring-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="a8d63-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="a8d63-124">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a8d63-124">Limitations</span></span>

<span data-ttu-id="a8d63-125">Zu diesem Zeitpunkt unterstützt der RPC-Lastenausgleich nur eine Serverfarm pro Ressource.</span><span class="sxs-lookup"><span data-stu-id="a8d63-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="a8d63-126">Alle Server in allen Serverfarmen müssen auch in der Lage sein, alle Ressourcen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8d63-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




