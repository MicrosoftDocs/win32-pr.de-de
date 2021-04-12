---
description: Der Dispenser-Manager stellt Ressourcen Pooling für die Ressourcen Spender bereit und stellt sicher, dass eine von einem Ressourcen Verteiler bereitgestellte Ressource ordnungsgemäß in der Anwendungs Objekt Transaktion eingetragen ist.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Com+-Dispenser-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523579"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="dabce-103">Com+-Dispenser-Manager</span><span class="sxs-lookup"><span data-stu-id="dabce-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="dabce-104">Der Dispenser-Manager bietet Ressourcen Pooling für die Ressourcen Spender und stellt sicher, dass eine von einem Ressourcen Verteiler bereitgestellte Ressource ordnungsgemäß in der Transaktion des Anwendungs Objekts eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="dabce-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="dabce-105">Der Dispenser-Manager gibt automatisch Ressourcen frei, die noch am Ende der Lebensdauer eines Objekts reserviert sind, wodurch die Wahrscheinlichkeit von Ressourcenverlusten entfällt.</span><span class="sxs-lookup"><span data-stu-id="dabce-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="dabce-106">Der Dispenser Manager kann einen Ressourcen Verteiler bitten, eine neue Ressource zu erstellen oder im Leerlauf befindliche Ressourcen zu zerstören, wenn dies erforderlich ist, um Inventur Ebenen anzupassen, anstatt statische Einstellungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dabce-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="dabce-107">Da Ressourcen Verteiler Schnittstellen, die für die Anwendung verfügbar gemacht werden, keine COM-Schnittstellen sein müssen, kann der Dispenser-Manager in einem Prozess verwendet werden, ohne com zu initialisieren, z. b. zur Unterstützung des ODBC-Ressourcen Verteilers.</span><span class="sxs-lookup"><span data-stu-id="dabce-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="dabce-108">Bei der Erstellung von Ressourcen kann der Ressourcen Verteiler angeben, wie lange eine Leerlauf Ressource im Pool verbleiben darf, bevor Sie zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="dabce-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="dabce-109">Ein Thread, der im Dispenser-Manager ausgeführt wird, sucht immer nach diesen im Leerlauf befindlichen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="dabce-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="dabce-110">Der Inventur Statistik-Manager</span><span class="sxs-lookup"><span data-stu-id="dabce-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="dabce-111">Der Dispenser-Manager verwendet den *Inventur Statistik-Manager* zum Verwalten der Ressourcen Inventur Ebenen des Pools.</span><span class="sxs-lookup"><span data-stu-id="dabce-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="dabce-112">Der Inventur Statistik-Manager verwaltet einen Datensatz darüber, wann die einzelnen Ressourcen verwendet wurden, und entfernt Ressourcen aus dem Inventar, wenn Sie nicht für *x* Sekunden verwendet wurden, wobei der Wert von *x* für jede Ressource festgelegt wird, wenn die Ressource erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dabce-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="dabce-113">Die Inhaber Komponente</span><span class="sxs-lookup"><span data-stu-id="dabce-113">The Holder Component</span></span>

<span data-ttu-id="dabce-114">Der Dispenser-Manager fragt jeden einzelnen *Inhaber* ab, eine Komponente, die vom Dispenser Manager erstellt wird und die den Ressourcen bestand für jeden Ressourcen Verteiler alle 10 Sekunden auflistet, damit er die Ressourcen Inventur nur noch lesen kann.</span><span class="sxs-lookup"><span data-stu-id="dabce-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="dabce-115">Jeder Inhaber Ruft den Inventur Statistik-Manager auf, um Inventur Ebenen für jeden Ressourcentyp vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="dabce-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="dabce-116">Demzufolge kann der Inhaber den Ressourcen Verteiler auffordern, eine Inventur zu erstellen oder zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="dabce-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="dabce-117">Der Inhaber und der Ressourcen Spender kommunizieren mit den Anforderungs Ressourcen eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="dabce-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="dabce-118">Zwischen dem Inhaber und dem Ressourcen Verteiler bestehen folgende Beziehungen:</span><span class="sxs-lookup"><span data-stu-id="dabce-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="dabce-119">Der Inhaber kann eine Ressource vom Ressourcen Verteiler anfordern.</span><span class="sxs-lookup"><span data-stu-id="dabce-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="dabce-120">Der Ressourcen Spender gibt entweder eine verfügbare Ressource zurück oder erstellt eine neue Ressource.</span><span class="sxs-lookup"><span data-stu-id="dabce-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="dabce-121">Der Inhaber kann den Ressourcen Verteiler Benachrichtigen, dass eine Anwendung keine Ressource mehr benötigt, und Sie dann an den Ressourcenpool zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dabce-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="dabce-122">Der Inhaber und der Ressourcen Verteiler arbeiten zusammen, um die Größe des Ressourcenpools beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="dabce-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dabce-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dabce-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dabce-124">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="dabce-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



