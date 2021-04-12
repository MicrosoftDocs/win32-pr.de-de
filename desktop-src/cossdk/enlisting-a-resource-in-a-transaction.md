---
description: Eintragen einer Ressource in eine Transaktion
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Eintragen einer Ressource in eine Transaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393229"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="83089-103">Eintragen einer Ressource in eine Transaktion</span><span class="sxs-lookup"><span data-stu-id="83089-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="83089-104">Nachdem eine Ressource zugewiesen wurde, aber kurz vor der Rückgabe der Ressource an den Ressourcen Verteiler, prüft der Dispenser-Manager mit com+, ob das aufrufende Objekt innerhalb einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83089-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="83089-105">Wenn das Aufruf Objekt innerhalb einer Transaktion ausgeführt wird, ruft der Dispenser-Manager den Ressourcen Verteiler zurück und fordert ihn auf, die Ressource in der Transaktion einzutragen.</span><span class="sxs-lookup"><span data-stu-id="83089-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="83089-106">Anschließend wird die Ressource an den Ressourcen Verteiler zurückgegeben, der Sie an die aufrufenden Instanz zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="83089-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="83089-107">Der Ressourcen Verteiler muss in der Lage sein, sich in einer OLE-Transaktion mit dem Distributed Transaction Coordinator (DTC) anzumelden.</span><span class="sxs-lookup"><span data-stu-id="83089-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="83089-108">Die Transaktions Eintragung ist optional, wenn ein Ressourcen Spender nicht transaktionale Ressourcen (z. b. Arbeitsspeicher oder Threads) ausgibt.</span><span class="sxs-lookup"><span data-stu-id="83089-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="83089-109">Wenn eine Transaktion abgeschlossen ist, benachrichtigt com+ den Verteiler-Manager darüber, ob er zugesichert oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="83089-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="83089-110">Anschließend benachrichtigt der Dispenser Manager den Besitzer jedes Ressourcen Verteilers, dass alle in dieser Transaktion eingetragenen Ressourcen nun in den allgemeinen bestand verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="83089-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83089-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83089-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83089-112">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="83089-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="83089-113">In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar</span><span class="sxs-lookup"><span data-stu-id="83089-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="83089-114">Ressourcen Zuordnungs Prozess Ressourcen Verteiler</span><span class="sxs-lookup"><span data-stu-id="83089-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



