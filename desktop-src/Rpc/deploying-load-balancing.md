---
title: Bereitstellen des Lasten Ausgleichs
description: Bereitstellen des Lasten Ausgleichs
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206550"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="7c94f-103">Bereitstellen des Lasten Ausgleichs</span><span class="sxs-lookup"><span data-stu-id="7c94f-103">Deploying Load Balancing</span></span>

<span data-ttu-id="7c94f-104">Die typische Bereitstellungs Umgebung und der Anwendungsfall, in der der RPC-Lastenausgleich verwendet wird, finden Sie unten:</span><span class="sxs-lookup"><span data-stu-id="7c94f-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![RPC-Lastenausgleich](images/rpc-load-balancing.png)

1.  <span data-ttu-id="7c94f-106">Der RPC-Client stellt eine RPC/HTTP-Verbindung mit der Serverfarm her.</span><span class="sxs-lookup"><span data-stu-id="7c94f-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="7c94f-107">Die Verbindung wird über das Netzwerk an ein Front-End-Lasten Ausgleichs Modul weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c94f-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="7c94f-108">Der Front-End-Load Balancer wählt einen Server aus, um die Anforderung zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="7c94f-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="7c94f-109">In diesem Beispiel leitet der Front-End-Load Balancer die Verbindung an Server 1 weiter.</span><span class="sxs-lookup"><span data-stu-id="7c94f-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="7c94f-110">Der RPC-Lasten Ausgleichs Dienst gibt die Verbindung aus.</span><span class="sxs-lookup"><span data-stu-id="7c94f-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="7c94f-111">Dabei wird festgelegt, dass es sich hierbei um die erste Verbindung vom Client handelt, und die Verbindung wird dem lokalen Server Server 1 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7c94f-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="7c94f-112">Der Client sendet eine zweite RPC/HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7c94f-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="7c94f-113">Die Anforderung wird über das Netzwerk an das Front-End-Lasten Ausgleichs Modul weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c94f-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="7c94f-114">Der Front-End-Load Balancer wählt einen Server aus, um die Anforderung zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="7c94f-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="7c94f-115">In diesem Fall wählt der Front-End-Lastenausgleich Server 2 aus, um die Anforderung zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="7c94f-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="7c94f-116">Der RPC-Load Balancer Dienst gibt die Verbindung aus.</span><span class="sxs-lookup"><span data-stu-id="7c94f-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="7c94f-117">Es wird erkannt, dass Verbindungen von diesem Client von Server 1 bedient werden.</span><span class="sxs-lookup"><span data-stu-id="7c94f-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="7c94f-118">Die Verbindung wird an Server 1 weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c94f-118">The connection is forwarded to Server 1.</span></span>

 

 




