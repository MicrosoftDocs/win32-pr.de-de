---
title: Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten
description: Die Zuordnung von Knoten zu Knoten und die Aufhebung der Zuordnung von Datenstrukturen durch die stusb ist die Standardmethode der Speicherverwaltung für alle Parameter auf dem Client und dem Server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473637"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="eba20-103">Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten</span><span class="sxs-lookup"><span data-stu-id="eba20-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="eba20-104">Die Zuordnung von Knoten zu Knoten und die Aufhebung der Zuordnung von Datenstrukturen durch die stusb ist die Standardmethode der Speicherverwaltung für alle Parameter auf dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="eba20-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="eba20-105">Auf der Clientseite ordnet der Stub jeden Knoten einem separaten aufrufszuordnungs- [ \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1)Namen zu.</span><span class="sxs-lookup"><span data-stu-id="eba20-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="eba20-106">Auf der Serverseite wird anstelle des Aufrufs von " **Mittel l- \_ Benutzer \_**" der private Arbeitsspeicher verwendet, wann immer dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="eba20-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="eba20-107">Wenn die **mittlere \_ Benutzer \_** Zuordnungen aufgerufen werden, ruft der serverstubvorgang die **\_ Benutzer \_ kostenlos** auf, um die Daten freizugeben.</span><span class="sxs-lookup"><span data-stu-id="eba20-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="eba20-108">In den meisten Fällen führt die Verwendung der Zuordnung von Knoten zu Knoten und das Aufheben der Zuordnung anstelle der Verwendung von " **\[ zuordnen" (alle \_ Knoten) \]** zu einer verbesserten Leistung der serverseitigen Stubdaten.</span><span class="sxs-lookup"><span data-stu-id="eba20-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 