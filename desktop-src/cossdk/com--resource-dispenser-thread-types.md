---
description: Com+-ressourcendispenser-Thread Typen
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Com+-ressourcendispenser-Thread Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393009"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="6b7fa-103">Com+-ressourcendispenser-Thread Typen</span><span class="sxs-lookup"><span data-stu-id="6b7fa-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="6b7fa-104">Aufrufe eines com+-Ressourcen Verteilers können aus einem der folgenden Thread Typen stammen:</span><span class="sxs-lookup"><span data-stu-id="6b7fa-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="6b7fa-105">Apartment Thread (STA)</span><span class="sxs-lookup"><span data-stu-id="6b7fa-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="6b7fa-106">Freier Thread (MTA)</span><span class="sxs-lookup"><span data-stu-id="6b7fa-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="6b7fa-107">Nicht-com-Thread (Anwendung oder der Garbage Collector-Thread des [Dispenser-Managers](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="6b7fa-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="6b7fa-108">Wenn ein Ressourcen Verteiler kein COM-Objekt ist, muss es in der Lage sein, Aufrufe zu verarbeiten, die von einem beliebigen Thread empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="6b7fa-109">Wenn ein Ressourcen Verteiler ein COM-Objekt ist, sollte das COM-Objekt mit einem Threading Modell von **beidem** registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="6b7fa-110">Dies ermöglicht es STA-oder MTA-Threads, den Ressourcen Verteiler ohne Thread Wechsel zu erstellen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="6b7fa-111">Wenn ein Ressourcen Verteiler ein anderes com-Objekt erstellt und verwendet (z. b. einen Out-of-Process-Ressourcen-Manager), muss der Ressourcen Verteiler möglicherweise mehrere Proxys für dieses andere COM-Objekt verwalten und sicherstellen, dass Aufrufe des Objekts mithilfe des entsprechenden Proxys für den aufrufenden Thread durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="6b7fa-112">Wenn der Ressourcen Spender dieses Objekt erstellt, Marshalls und speichert es den Verweis.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="6b7fa-113">Vor dem erneuten Aufrufen des Objekts muss das Marshalling durchlaufen werden, um einen Proxy für den aufrufenden Thread zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="6b7fa-114">Es ist möglicherweise effizienter, diese Thread bezogenen Proxys zwischenzuspeichern, indem eine Zuordnung von der Thread-ID zu einem Proxy Zeiger beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="6b7fa-115">Diese Zuordnung wird erweitert, wenn im Prozess neue Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b7fa-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b7fa-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b7fa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7fa-117">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="6b7fa-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



