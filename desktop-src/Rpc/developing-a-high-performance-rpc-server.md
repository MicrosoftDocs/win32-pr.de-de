---
title: Entwickeln eines Hochleistungs-RPC-Servers
description: Die Informationen in diesem Abschnitt gelten für Remote Protokoll Sequenzen ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ NP und Windows 2000 und Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, entwickeln eines Hochleistungs Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473989"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="3d0e8-104">Entwickeln eines Hochleistungs-RPC-Servers</span><span class="sxs-lookup"><span data-stu-id="3d0e8-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="3d0e8-105">Die Informationen in diesem Abschnitt gelten für Remote Protokoll Sequenzen: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)und Windows 2000 und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="3d0e8-106">In diesem Abschnitt werden drei Hauptaspekte der RPC-Serverleistung behandelt:</span><span class="sxs-lookup"><span data-stu-id="3d0e8-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="3d0e8-107">Netzwerk Latenz und Durchsatz</span><span class="sxs-lookup"><span data-stu-id="3d0e8-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="3d0e8-108">Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="3d0e8-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="3d0e8-109">Sonstige RPC-Leistungs Tipps</span><span class="sxs-lookup"><span data-stu-id="3d0e8-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="3d0e8-110">Die Codepfad-Länge ist eine weitere primäre Leistungs Überlegung für RPC.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="3d0e8-111">Die Länge des Codepfade ist im Allgemeinen gut verständlich, und da Literatur und Tools in diesem Thema allgemein verfügbar sind, wird es in diesem Artikel nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="3d0e8-112">Eine wichtige und bewährte allgemeine Leistungs Regel, die bei der Betrachtung der RPC-Leistung beachtet werden muss, ist dies: ermitteln Sie den Engpass im System, und arbeiten Sie daran, diesen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="3d0e8-113">Beim Gating-Engpass darf es sich nicht um die RPC-Programmierung handeln. wenn dies der Fall ist, führt die Leistungsoptimierung in RPC nicht zu einer verbesserten Leistung, bis der Engpass behoben wird.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="3d0e8-114">Beispielsweise muss ein System, das von Ressourcenkonflikten geplagt ist, nicht die effizientere Verwendung des Netzwerks durchführen.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="3d0e8-115">Wenn Ihr System in verschiedenen Umgebungen bereitgestellt wird, ist es ratsam, sicherzustellen, dass alle Aspekte des IT-Systems gut optimiert sind, da unterschiedliche Umgebungen zu unterschiedlichen Leistungs Engpässen führen können.</span><span class="sxs-lookup"><span data-stu-id="3d0e8-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 