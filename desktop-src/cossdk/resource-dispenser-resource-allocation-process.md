---
description: Ressourcen Zuordnungs Prozess Ressourcen Verteiler
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Ressourcen Zuordnungs Prozess Ressourcen Verteiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214140"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="3e097-103">Ressourcen Zuordnungs Prozess Ressourcen Verteiler</span><span class="sxs-lookup"><span data-stu-id="3e097-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="3e097-104">Jedes Mal, wenn ein Ressourcen Verteiler eine Ressource von seinem Inhaber zugeordnet hat, geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3e097-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="3e097-105">Der Ressourcen Verteiler deklariert einen Ressourcentyp Bezeichner (**restypid**), der den Typ der erforderlichen Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3e097-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="3e097-106">Der Ressourcen Verteiler ruft die [**ihälter:: Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) -Methode des Inhabers auf und übergibt diese **restypid**.</span><span class="sxs-lookup"><span data-stu-id="3e097-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="3e097-107">Der Inhaber generiert eine Kandidatenliste aus den verfügbaren Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3e097-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="3e097-108">Kandidaten sind Ressourcen, die entweder nicht in einer Transaktion eingetragen sind oder bereits in der Transaktion des aufrufenden Objekts eingetragen wurden.</span><span class="sxs-lookup"><span data-stu-id="3e097-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="3e097-109">Diese Kandidaten werden einzeln an die [**idispenser Server Driver:: rateresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) -Methode übergeben, wo Sie (auf einer Skala von 0 bis 100) bewertet werden, um wie gut die Candidate-Ressource mit der gewünschten **restypid** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3e097-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="3e097-110">Der Inhaber wählt die Ressource aus, die der Ressourcen Spender als höchsten Wert bewertet.</span><span class="sxs-lookup"><span data-stu-id="3e097-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="3e097-111">Der Ressourcen Verteiler kann die Bewertungs Schleife frühzeitig beenden, indem er den Kandidaten eine Ressourcenbewertung von 100 (eine perfekte Anpassung) zuweist.</span><span class="sxs-lookup"><span data-stu-id="3e097-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="3e097-112">Die Bewertung 100 ist normalerweise für Kandidaten Ressourcen reserviert, die bereits ordnungsgemäß eingetragen sind, es sei denn, der Ressourcen Verteiler schließt aus, dass die Eintragung ein kostengünstiger Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="3e097-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="3e097-113">Wenn alle möglichen Ressourcen (sofern vorhanden) als 0 (unbrauchbar) eingestuft werden, wird eine neue Ressource durch Aufrufen von [**idispenser Server:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource)erstellt.</span><span class="sxs-lookup"><span data-stu-id="3e097-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="3e097-114">Wenn die zuvor ausgewählte Ressource noch nicht in der Transaktion des aufrufenden Objekts eingetragen ist, wird die [**idispenser Server Driver:: enlistresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) -Methode des Ressourcen Verteilers aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e097-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="3e097-115">Der Methoden Aufrufder [**Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) wird an den Ressourcen Verteiler mit der eingetragenen Ressource zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e097-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e097-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e097-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e097-117">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="3e097-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="3e097-118">Eintragen einer Ressource in eine Transaktion</span><span class="sxs-lookup"><span data-stu-id="3e097-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="3e097-119">Nachverfolgen nicht zugewiesener Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3e097-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



