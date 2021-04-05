---
title: Zugreifen auf Schnittstellen über mehrere Apartments
description: Zugreifen auf Schnittstellen über mehrere Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709258"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="f12af-103">Zugreifen auf Schnittstellen über mehrere Apartments</span><span class="sxs-lookup"><span data-stu-id="f12af-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="f12af-104">COM bietet eine Möglichkeit für jedes Apartment in einem Prozess, Zugriff auf eine Schnittstelle zu erhalten, die für ein Objekt in einem beliebigen anderen Apartment im Prozess implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f12af-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="f12af-105">Dies erfolgt über die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f12af-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="f12af-106">Diese Schnittstelle verfügt über drei Methoden, mit denen Sie die folgenden Aktionen ausführen können:</span><span class="sxs-lookup"><span data-stu-id="f12af-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="f12af-107">Registrieren Sie eine Schnittstelle als *globale* (Processwide) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f12af-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="f12af-108">Einen Zeiger auf diese Schnittstelle von einem beliebigen anderen Apartment über ein Cookie erhalten.</span><span class="sxs-lookup"><span data-stu-id="f12af-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="f12af-109">Widerrufen Sie die globale Registrierung einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f12af-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="f12af-110">Die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle ist ein effizientes Verfahren zum Speichern eines Schnittstellen Zeigers an einem Speicherort, auf den von mehreren Apartments innerhalb des Prozesses zugegriffen werden kann, z. b. Prozess weite Variablen und *Agile* -Objekte (frei Thread-, gemarshallte Objekte), die Schnittstellen Zeiger auf andere Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="f12af-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="f12af-111">Ein Agile-Objekt kennt die zugrunde liegende COM-Infrastruktur, in der es ausgeführt wird, nicht. Anders ausgedrückt: Das Apartment, der Kontext und der Thread, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f12af-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="f12af-112">Das Objekt ist möglicherweise für Schnittstellen, die für ein Apartment oder einen kontextspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f12af-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="f12af-113">Aus diesem Grund funktioniert das Aufrufen dieser Schnittstellen von überall aus, wo die Agile-Komponente ausgeführt wird, möglicherweise nicht immer ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f12af-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="f12af-114">Die globale Schnittstellen Tabelle vermeidet dieses Problem, indem Sie sicherstellt, dass ein gültiger Proxy (oder direkter Zeiger) für das-Objekt verwendet wird, je nachdem, wo das Agile-Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f12af-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="f12af-115">Die globale Schnittstellen Tabelle ist nicht über Prozess-oder Computer Grenzen hinweg portabel und kann daher nicht anstelle des normalen Parameters-Passing-Mechanismus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f12af-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="f12af-116">Weitere Informationen zum Erstellen und Verwenden einer globalen Schnittstellen Tabelle finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f12af-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="f12af-117">Erstellen der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="f12af-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="f12af-118">Verwendungszwecke der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="f12af-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="f12af-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f12af-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f12af-120">Auswählen des Threading Modells</span><span class="sxs-lookup"><span data-stu-id="f12af-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="f12af-121">Multithread-Apartments</span><span class="sxs-lookup"><span data-stu-id="f12af-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="f12af-122">Threading Probleme im Prozess internen Server</span><span class="sxs-lookup"><span data-stu-id="f12af-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="f12af-123">Prozesse, Threads und Apartments</span><span class="sxs-lookup"><span data-stu-id="f12af-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="f12af-124">Single Thread-und Multithread-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="f12af-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="f12af-125">Single Thread-Apartments</span><span class="sxs-lookup"><span data-stu-id="f12af-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




