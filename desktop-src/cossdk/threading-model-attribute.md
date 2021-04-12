---
description: Com+ verwaltet Threads für Sie. Jede COM-Komponente verfügt über eine ThreadingModel-Eigenschaft, die Sie beim Entwickeln der Komponente angeben können. Diese Eigenschaft bestimmt, wie die Komponenten Objekte Threads zur Methoden Ausführung zugewiesen werden.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Threading Modell-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392998"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="b9e71-105">Threading Modell-Attribut</span><span class="sxs-lookup"><span data-stu-id="b9e71-105">Threading Model Attribute</span></span>

<span data-ttu-id="b9e71-106">Com+ verwaltet Threads für Sie.</span><span class="sxs-lookup"><span data-stu-id="b9e71-106">COM+ manages threads for you.</span></span> <span data-ttu-id="b9e71-107">Jede COM-Komponente verfügt über eine **ThreadingModel** -Eigenschaft, die Sie beim Entwickeln der Komponente angeben können.</span><span class="sxs-lookup"><span data-stu-id="b9e71-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="b9e71-108">Diese Eigenschaft bestimmt, wie die Objekte der Komponente Threads zur Methoden Ausführung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b9e71-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="b9e71-109">Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Threading-Model-Eigenschaft anzeigen, indem Sie mit der rechten Maustaste auf eine Komponente im Ordner **Komponenten** klicken, auf **Eigenschaften** klicken und dann **auf die Register** Karte Parallelität klicken. Unter dem **Threading Modell** sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="b9e71-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="b9e71-110">**Haupt Thread Apartment**</span><span class="sxs-lookup"><span data-stu-id="b9e71-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="b9e71-111">**Single Thread-Apartment**</span><span class="sxs-lookup"><span data-stu-id="b9e71-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="b9e71-112">**Kostenloses Thread Apartment**</span><span class="sxs-lookup"><span data-stu-id="b9e71-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="b9e71-113">**Neutrales Apartment**</span><span class="sxs-lookup"><span data-stu-id="b9e71-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="b9e71-114">**Beliebige Wohnungen**</span><span class="sxs-lookup"><span data-stu-id="b9e71-114">**Any Apartment**</span></span>

<span data-ttu-id="b9e71-115">Das bevorzugte Threading Modell für com+ ist das [neutrale Apartment](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="b9e71-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="b9e71-116">Wenn Sie jedoch kein Threading Modell für Ihre Komponente angeben, verwendet com+ das Haupt Thread-Apartment, das die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="b9e71-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="b9e71-117">Ausführlichere Informationen finden Sie unter [auswählen des Threading Modells](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="b9e71-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="b9e71-118">In der folgenden Tabelle wird das Programmiermodell für Apartments in com+ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9e71-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="b9e71-119">Modell</span><span class="sxs-lookup"><span data-stu-id="b9e71-119">Model</span></span>                     | <span data-ttu-id="b9e71-120">Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-120">Apartment</span></span>                                                 | <span data-ttu-id="b9e71-121">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="b9e71-121">Free</span></span>                               | <span data-ttu-id="b9e71-122">Both</span><span class="sxs-lookup"><span data-stu-id="b9e71-122">Both</span></span>                               | <span data-ttu-id="b9e71-123">Neutral</span><span class="sxs-lookup"><span data-stu-id="b9e71-123">Neutral</span></span>                      | <span data-ttu-id="b9e71-124">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="b9e71-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="b9e71-125">Single Thread, nicht Haupt</span><span class="sxs-lookup"><span data-stu-id="b9e71-125">Single-threaded, not main</span></span> | <span data-ttu-id="b9e71-126">In aktuellem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-126">Created in current apartment</span></span>                              | <span data-ttu-id="b9e71-127">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-128">In aktuellem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-128">Created in current apartment</span></span>       | <span data-ttu-id="b9e71-129">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-129">Created in neutral apartment</span></span> | <span data-ttu-id="b9e71-130">Erstellt in Haupt Thread-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="b9e71-131">Single Thread, Main</span><span class="sxs-lookup"><span data-stu-id="b9e71-131">Single-threaded, main</span></span>     | <span data-ttu-id="b9e71-132">In aktuellem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-132">Created in current apartment</span></span>                              | <span data-ttu-id="b9e71-133">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-134">In aktuellem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-134">Created in current apartment</span></span>       | <span data-ttu-id="b9e71-135">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-135">Created in neutral apartment</span></span> | <span data-ttu-id="b9e71-136">In aktuellem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-136">Created in current apartment</span></span>       |
| <span data-ttu-id="b9e71-137">Multithread</span><span class="sxs-lookup"><span data-stu-id="b9e71-137">Multithreaded</span></span>             | <span data-ttu-id="b9e71-138">Erstellt im Single Thread-Host-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="b9e71-139">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-140">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-141">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-141">Created in neutral apartment</span></span> | <span data-ttu-id="b9e71-142">Erstellt in Haupt Thread-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="b9e71-143">Neutral (auf STA-Thread)</span><span class="sxs-lookup"><span data-stu-id="b9e71-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="b9e71-144">Erstellt im Single Thread-Host für diesen Thread</span><span class="sxs-lookup"><span data-stu-id="b9e71-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="b9e71-145">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-146">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-146">Created in neutral apartment</span></span>       | <span data-ttu-id="b9e71-147">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-147">Created in neutral apartment</span></span> | <span data-ttu-id="b9e71-148">Erstellt in Haupt Thread-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="b9e71-149">Neutral (im MTA-Thread)</span><span class="sxs-lookup"><span data-stu-id="b9e71-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="b9e71-150">Erstellt im Single Thread-Host-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="b9e71-151">Im Multithread-Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="b9e71-152">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-152">Created in neutral apartment</span></span>       | <span data-ttu-id="b9e71-153">In neutralem Apartment erstellt</span><span class="sxs-lookup"><span data-stu-id="b9e71-153">Created in neutral apartment</span></span> | <span data-ttu-id="b9e71-154">Erstellt in Haupt Thread-Apartment</span><span class="sxs-lookup"><span data-stu-id="b9e71-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b9e71-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9e71-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9e71-156">**Threading Model**</span><span class="sxs-lookup"><span data-stu-id="b9e71-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
