---
description: Transaktionale Komponenten, die in einem Pool zusammengefasst werden sollen, müssen besondere Anforderungen erfüllen.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling von transaktionalen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345445"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="845a9-103">Pooling von transaktionalen Objekten</span><span class="sxs-lookup"><span data-stu-id="845a9-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="845a9-104">Transaktionale Komponenten, die in einem Pool zusammengefasst werden sollen, müssen besondere Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="845a9-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="845a9-105">Manuelles eintragen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="845a9-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="845a9-106">In Poolable-Objekten, die an Transaktionen teilnehmen, müssen verwaltete Ressourcen manuell eingetragen werden.</span><span class="sxs-lookup"><span data-stu-id="845a9-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="845a9-107">Wenn ein Objekt verwaltete Ressourcen zwischen Clients enthält, gibt es keine Möglichkeit für den Ressourcen-Manager, sich automatisch in eine Transaktion einzutragen, wenn das Objekt in einem bestimmten Kontext aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="845a9-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="845a9-108">Das Objekt selbst muss die Logik zum Erkennen der Transaktion, zum Ausschalten der automatischen Eintragung des Ressourcen-Managers und zum manuellen eintragen der darin befindlichen Ressourcen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="845a9-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="845a9-109">Die erforderlichen Schritte sind spezifisch für den Ressourcen-Manager, den Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="845a9-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="845a9-110">Wenn Sie eine manuelle Eintragung ausführen müssen, lesen Sie die Dokumentation für Ihren Ressourcen-Manager.</span><span class="sxs-lookup"><span data-stu-id="845a9-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="845a9-111">Wie unten beschrieben, können Objekte mit Transaktions Affinität in einem Pool zusammengefasst werden, während eine Transaktion aktiv ist und mit Transaktions Affinität aktiviert werden kann, wenn Sie von einem Client aufgerufen wird, der dieser Transaktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="845a9-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="845a9-112">Vor der Eintragung von Ressourcen sollten Sie zunächst die Transaktions Affinität überprüfen.</span><span class="sxs-lookup"><span data-stu-id="845a9-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="845a9-113">Wenn das Objekt aus dem für diese Transaktion spezifischen Pool entnommen wurde, hat es bereits in dieser Transaktion gearbeitet und seine Ressourcen eingetragen.</span><span class="sxs-lookup"><span data-stu-id="845a9-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="845a9-114">Deaktivieren der automatischen Eintragung</span><span class="sxs-lookup"><span data-stu-id="845a9-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="845a9-115">Die automatische Eintragung muss ausgeschaltet werden, nachdem die Ressource abgerufen wurde, normalerweise im Konstruktor des Objekts.</span><span class="sxs-lookup"><span data-stu-id="845a9-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="845a9-116">Das heißt, Sie deaktivieren die automatische Eintragung und stellen dann eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="845a9-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="845a9-117">Das Deaktivieren der automatischen Eintragung kann manchmal ein sehr feines Verfahren sein, insbesondere im Fall von mehrstufigen Datenzugriffs Anbietern.</span><span class="sxs-lookup"><span data-stu-id="845a9-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="845a9-118">Die automatische Eintragung ist manchmal mit dem Verbindungspooling gekoppelt, wie z.b. mit ODBC, und manchmal nicht, wie bei OLE DB.</span><span class="sxs-lookup"><span data-stu-id="845a9-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="845a9-119">Möglicherweise müssen Sie sicherstellen, dass die automatische Eintragung auf mehreren Ebenen von Anbietern deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="845a9-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="845a9-120">Implementieren von IObjectControl</span><span class="sxs-lookup"><span data-stu-id="845a9-120">Implementing IObjectControl</span></span>

<span data-ttu-id="845a9-121">In einem Pool enthaltene Objekte, die an Transaktionen teilnehmen, müssen den aktuellen Status der Ressourcen überwachen, die Sie halten.</span><span class="sxs-lookup"><span data-stu-id="845a9-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="845a9-122">Wenn das Objekt erkennt, dass es sich in einem nicht wiederverwendbaren Zustand befindet – z. b. Wenn eine Verbindung fehlerfrei ist – sollte für [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)der Wert false zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="845a9-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="845a9-123">Dies hat den Effekt, dass die Objektinstanz verworfen und die aktuelle Transaktion angedockt wird.</span><span class="sxs-lookup"><span data-stu-id="845a9-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="845a9-124">Transaction-Specific Pools</span><span class="sxs-lookup"><span data-stu-id="845a9-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="845a9-125">Ein Pool von Objekten ist im allgemeinen homogen, und jedes in einem Pool enthaltene Objekt, das zurzeit nicht verwendet wird, kann zu einem beliebigen Client zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="845a9-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="845a9-126">Die einzige Ausnahme von dieser Regel sind Transaktions Objekte, bei denen das Objekt Pooling optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="845a9-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="845a9-127">Wenn der Client, der ein Objekt anfordert, über eine zugeordnete Transaktion verfügt, scannt com+ den Pool nach einem verfügbaren Objekt, das bereits der Transaktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="845a9-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="845a9-128">Wenn ein Objekt mit Transaktions Affinität gefunden wird, wird es an den Client zurückgegeben. Andernfalls wird ein Objekt aus dem allgemeinen Pool zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="845a9-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="845a9-129">Auf diese Weise werden spezielle unter Pools verwaltet, die Objekte mit Affinität für eine bestimmte Transaktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="845a9-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="845a9-130">Wenn die Transaktion ausgeführt wird oder abgebrochen wird, werden diese Objekte ohne Transaktions Affinität an den allgemeinen Pool zurückgegeben und können von jedem beliebigen Client verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="845a9-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="845a9-131">Wenn Ihre verwalteten Ressourcen von der Komponente manuell in eine Transaktion eingetragen werden, sollten Sie daher zunächst überprüfen, ob Sie bereits eingetragen wurden.</span><span class="sxs-lookup"><span data-stu-id="845a9-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="845a9-132">Wenn dies der Fall ist, müssen Sie sich nicht eintragen.</span><span class="sxs-lookup"><span data-stu-id="845a9-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="845a9-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="845a9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="845a9-134">Com+-objektkonstruktorzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="845a9-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="845a9-135">Steuern der Objekt Lebensdauer und des Zustands</span><span class="sxs-lookup"><span data-stu-id="845a9-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="845a9-136">Funktionsweise des Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="845a9-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="845a9-137">Verbessern der Leistung durch Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="845a9-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="845a9-138">Anforderungen für in einem Pool Bare Objekte</span><span class="sxs-lookup"><span data-stu-id="845a9-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



