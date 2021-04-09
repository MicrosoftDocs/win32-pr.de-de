---
description: Im Allgemeinen ist die Synchronisierung nicht erforderlich, wenn Sie über ein Single Thread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Com+-Synchronisierungs Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748880"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="739b7-103">Com+-Synchronisierungs Konzepte</span><span class="sxs-lookup"><span data-stu-id="739b7-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="739b7-104">Im Allgemeinen ist die Synchronisierung nicht erforderlich, wenn Sie über ein Single Thread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="739b7-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="739b7-105">Die Synchronisierung wird wichtig, wenn Sie über ein Multithread-Apartment (MTA) und ein Freethread-Objekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="739b7-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="739b7-106">In der Vergangenheit mussten frei Thread Objekte Sperren behandeln.</span><span class="sxs-lookup"><span data-stu-id="739b7-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="739b7-107">Sie können die Verwendung von Sperren ausschließen, indem Sie das Synchronisierungs Attribut für eine Komponente festlegen.</span><span class="sxs-lookup"><span data-stu-id="739b7-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="739b7-108">Die Synchronisierung verfügt über die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="739b7-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="739b7-109">Ermöglicht einem Aufrufer, die Komponente gleichzeitig einzugeben.</span><span class="sxs-lookup"><span data-stu-id="739b7-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="739b7-110">Verhindert, dass der Flow Prozess übergreifend oder Computer übergreifend ist.</span><span class="sxs-lookup"><span data-stu-id="739b7-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="739b7-111">Fließt von Komponente zu Komponente innerhalb eines Prozesses.</span><span class="sxs-lookup"><span data-stu-id="739b7-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="739b7-112">Ermöglicht den erneuten eintreten desselben Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="739b7-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="739b7-113">Im Gegensatz zu-Apartments umfassen Aktivitäten Kontexte zwischen mehreren Prozessen und Hosts.</span><span class="sxs-lookup"><span data-stu-id="739b7-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="739b7-114">Durch die Synchronisierung wird bestimmt, welche Aktivität ein Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="739b7-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="739b7-115">-Objekte können sich in einer der folgenden Aktivitäten befinden:</span><span class="sxs-lookup"><span data-stu-id="739b7-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="739b7-116">Aktivität des Erstellers</span><span class="sxs-lookup"><span data-stu-id="739b7-116">Creator's activity</span></span>
-   <span data-ttu-id="739b7-117">Neue Aktivität</span><span class="sxs-lookup"><span data-stu-id="739b7-117">New activity</span></span>
-   <span data-ttu-id="739b7-118">Keine Aktivität</span><span class="sxs-lookup"><span data-stu-id="739b7-118">No activity</span></span>

<span data-ttu-id="739b7-119">Com+ stellt Parallelität durch eine Reihe von Sperren für jede Aktivität sicher.</span><span class="sxs-lookup"><span data-stu-id="739b7-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="739b7-120">Wenn ein Aufrufer versucht, eine synchronisierte COM+-Komponente einzugeben, die bereits von einem anderen Aufrufer verwendet wird, wird der Aufruf blockiert, bis die Sperre aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="739b7-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="739b7-121">Bei diesem blockierenden Verhalten tritt kein Timeout auf, und es kann nicht konfiguriert werden, dass ein Timeout auftritt. Wenn die Sperre nicht verwendet wird, wird die Sperre abgerufen, und der-Befehl wird verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="739b7-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="739b7-122">Nach Abschluss der Ausführung wird die Sperre für den nächsten Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="739b7-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="739b7-123">Um Deadlocks zu verhindern, verwaltet com+ den Zugriff auf alle Objekte über Aktivitäten hinweg durch eine Reihe von im Netzwerk verketteten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="739b7-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="739b7-124">Com+ bietet die folgenden Synchronisierungs Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="739b7-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="739b7-125">Disabled</span><span class="sxs-lookup"><span data-stu-id="739b7-125">Disabled</span></span>
-   <span data-ttu-id="739b7-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="739b7-126">Not Supported</span></span>
-   <span data-ttu-id="739b7-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="739b7-127">Supported</span></span>
-   <span data-ttu-id="739b7-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="739b7-128">Required</span></span>
-   <span data-ttu-id="739b7-129">Requires New</span><span class="sxs-lookup"><span data-stu-id="739b7-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="739b7-130">Einige Synchronisierungs Einstellungen funktionieren in Verbindung mit anderen COM+-Komponenten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="739b7-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="739b7-131">Beispielsweise ist eine Synchronisierung erforderlich, wenn der [com+-Just-in-time (JIT)-Aktivierungs](com--just-in-time-activation.md) Dienst aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="739b7-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="739b7-132">JIT ist erforderlich, wenn Sie Transaktionen aktivieren. Daher muss die com+- [Transaktionsverarbeitung](com--transactions.md) ebenfalls synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="739b7-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="739b7-133">Daher müssen Klassen mit der Einstellung "JIT = true" auch die Einstellung "Synchronisierung = erforderlich" oder "Synchronisierung = Requirements SNEW" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="739b7-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="739b7-134">Anweisungen zum Festlegen von Synchronisierungs Optionen mithilfe des Verwaltungs Programms Komponenten Dienste finden Sie unter [Festlegen des Synchronisierungs Attributs](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="739b7-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="739b7-135">Weitere Informationen zum Festlegen von Synchronisierungs Optionen mithilfe der com+-Verwaltungs Bibliothek finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="739b7-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="739b7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="739b7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="739b7-137">Com+-Synchronisierungs Tasks</span><span class="sxs-lookup"><span data-stu-id="739b7-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



