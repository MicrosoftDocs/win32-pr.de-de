---
description: Steuern der Objekt Lebensdauer und des Zustands
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Steuern der Objekt Lebensdauer und des Zustands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343607"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="75b15-103">Steuern der Objekt Lebensdauer und des Zustands</span><span class="sxs-lookup"><span data-stu-id="75b15-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="75b15-104">Ein in einem Pool zusammengefasste Objekt kann daran teilnehmen, wie com+ seine Aktivität im Pool durch Implementieren von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)verwaltet.</span><span class="sxs-lookup"><span data-stu-id="75b15-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="75b15-105">Wenn ein in einem Pool zusammengestelltes Objekt erstellt wird, wird es in ein größeres Objekt aggregiert, das das Objekt verwaltet, indem die folgenden Methoden für **IObjectControl** an den regulären Punkten im Lebenszyklus des Objekts aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="75b15-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="75b15-106">[**Aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)– wird aufgerufen, wenn das Objekt an einen Client zurückgegeben wird, das in einem bestimmten Kontext aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="75b15-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="75b15-107">[**Deaktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)– wird aufgerufen, wenn ein Objekt vom Client freigegeben wird, oder im Fall eines JIT-aktivierten Objekts, wenn es deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="75b15-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="75b15-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)– wird aufgerufen, wenn ein Objekt an den allgemeinen Pool zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="75b15-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="75b15-109">Die Implementierung von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) ist optional, mit Ausnahme von transaktionalen Objekten, die immer [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) implementieren sollten, um den Status der Ressourcen zu überwachen, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="75b15-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="75b15-110">In den meisten Fällen empfiehlt es sich jedoch, **IObjectControl** zu implementieren, da es eine effiziente Möglichkeit bietet, das Verhalten eines in einem Pool zusammen gepoolten Objekts zu verwalten, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75b15-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="75b15-111">Ausführen Context-Specific Initialisierung</span><span class="sxs-lookup"><span data-stu-id="75b15-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="75b15-112">Mithilfe von " [**aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)" können Sie das Objekt im Kontext initialisieren, in dem es für einen bestimmten Client aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="75b15-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="75b15-113">Um z. b. zu ermitteln, ob das Objekt Transaktions Affinität aufweist (seine Ressourcen sind möglicherweise bereits eingetragen), erhalten Sie möglicherweise die Transaktions-ID, die dem Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75b15-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="75b15-114">In der Regel verwenden Sie " [**aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)", um eine Initialisierung durchzuführen, die für alle Methoden konsistent ist, die vom-Objekt verfügbar gemacht werden, und behandelt diese als kontextspezifischen Teil des-Konstruktors des Objekts.</span><span class="sxs-lookup"><span data-stu-id="75b15-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="75b15-115">Bereinigen eines beliebigen Client Zustands</span><span class="sxs-lookup"><span data-stu-id="75b15-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="75b15-116">Mithilfe von " [**Deaktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)" können Sie jeden Client spezifischen Zustand entfernen, der möglicherweise vorhanden ist, damit das Objekt in einem vollständig generischen Zustand an den Pool zurückkehrt und dann von jedem Client verwendet werden kann, ohne die Sicherheit oder Isolation zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="75b15-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="75b15-117">Steuern der Wiederverwendung des Objekts</span><span class="sxs-lookup"><span data-stu-id="75b15-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="75b15-118">Mithilfe von [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)können Sie den internen Zustand Ihres Objekts überwachen und melden, ob er für seine Wiederverwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="75b15-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="75b15-119">Wenn " **CanBePooled** " den Wert "true" zurückgibt und der Pool "Maximum" nicht erreicht wurde, wird das Objekt wieder im allgemeinen Pool abgelegt.</span><span class="sxs-lookup"><span data-stu-id="75b15-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="75b15-120">Wenn **CanBePooled** false zurückgibt, wird das-Objekt verworfen.</span><span class="sxs-lookup"><span data-stu-id="75b15-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="75b15-121">Im Fall von transaktionalen Komponenten wird die aktuelle Transaktion durch Zurückgeben von "false" unterbunden.</span><span class="sxs-lookup"><span data-stu-id="75b15-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="75b15-122">In der Regel behalten Sie einen globalen Datenmember für das Objekt bei, und wenn Sie eine Verbindung mit einem ungültigen Zustand erkennen oder eine Ressource in einem fehlerhaften Zustand haben, legen Sie diese so fest, dass Sie die aktuelle Situation widerspiegelt, und geben Sie Sie über " [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)" zurück.</span><span class="sxs-lookup"><span data-stu-id="75b15-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="75b15-123">Wenn ein Objekt keine [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)implementiert, werden die Instanzen weiterhin wieder verwendet, bis die maximale Pool Ebene erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="75b15-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b15-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75b15-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b15-125">Com+-objektkonstruktorzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="75b15-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="75b15-126">Funktionsweise des Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="75b15-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="75b15-127">Verbessern der Leistung durch Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="75b15-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="75b15-128">Pooling von transaktionalen Objekten</span><span class="sxs-lookup"><span data-stu-id="75b15-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="75b15-129">Anforderungen für in einem Pool Bare Objekte</span><span class="sxs-lookup"><span data-stu-id="75b15-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



