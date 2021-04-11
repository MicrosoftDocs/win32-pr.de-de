---
description: Sie können eine Komponente so konfigurieren, dass Sie nur dann in einem Pool zusammengefasst wird, wenn Sie ordnungsgemäß geschrieben wurde Ausführliche Informationen zu diesen Anforderungen finden Sie unter Anforderungen für in einem Pool Bare Objekte.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127564"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="6d182-104">Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll</span><span class="sxs-lookup"><span data-stu-id="6d182-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="6d182-105">Sie können eine Komponente so konfigurieren, dass Sie nur dann in einem Pool zusammengefasst wird, wenn Sie ordnungsgemäß geschrieben wurde</span><span class="sxs-lookup"><span data-stu-id="6d182-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="6d182-106">Ausführliche Informationen zu diesen Anforderungen finden Sie unter [Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6d182-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="6d182-107">Standardmäßig ist eine Komponente nicht für ein Pool konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6d182-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="6d182-108">Wenn Sie eine Komponente so konfigurieren, dass Sie in einem Pool zusammengefasst wird, können Sie die folgenden Eigenschaften angeben, um zu bestimmen, wie com+ den Pool verwaltet:</span><span class="sxs-lookup"><span data-stu-id="6d182-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="6d182-109">**Minimale Poolgröße.**</span><span class="sxs-lookup"><span data-stu-id="6d182-109">**Minimum pool size.**</span></span> <span data-ttu-id="6d182-110">Stellt die Anzahl der Objekte dar, die beim Start der Anwendung erstellt werden, und die Mindestanzahl von Objekten, die im Pool gewartet werden, während die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d182-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="6d182-111">Wenn die Anzahl der verfügbaren Objekte im Pool unter den angegebenen Minimalwert sinkt, werden neue Objekte erstellt, um ausstehende Objekt Anforderungen zu erfüllen und den Pool erneut auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="6d182-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="6d182-112">Wenn die Anzahl der verfügbaren Objekte im Pool größer ist als die Mindestanzahl, werden diese überzähligen Objekte während eines Bereinigungs Prozesses zerstört.</span><span class="sxs-lookup"><span data-stu-id="6d182-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="6d182-113">**Maximale Poolgröße.**</span><span class="sxs-lookup"><span data-stu-id="6d182-113">**Maximum pool size.**</span></span> <span data-ttu-id="6d182-114">Stellt die maximale Anzahl von in einem Pool zusammengefassten Objekten dar, die vom Pooling-Manager erstellt werden, der von den Clients aktiv verwendet und inaktiv im Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d182-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="6d182-115">Beim Erstellen von Objekten prüft der Pooling Manager, ob die maximale Poolgröße nicht erreicht wurde, und wenn dies nicht der Fall ist, erstellt der Pool-Manager eine neue Instanz des Objekts, das auf den Client verzichtet.</span><span class="sxs-lookup"><span data-stu-id="6d182-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="6d182-116">Wenn die maximale Poolgröße erreicht ist, werden Client Anforderungen in die Warteschlange eingereiht und empfangen das erste verfügbare Objekt aus dem Pool auf der Grundlage der ersten Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6d182-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="6d182-117">Bei Objekt Erstellungs Anforderungen wird nach einem bestimmten Zeitraum ein Timeout festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d182-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="6d182-118">**Erstellungs Timeout (MS).**</span><span class="sxs-lookup"><span data-stu-id="6d182-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="6d182-119">Gibt an, wie lange ein Client nach einem [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)-Aufrufvorgang (in Millisekunden) darauf wartet, dass ein Objekt aus dem Pool zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d182-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6d182-120">Wenn der Client-Rückruf nicht erfolgreich ist, wird der Fehler E \_ Timeout zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d182-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="6d182-121">**So legen Sie Pooling-bezogene Eigenschaften fest**</span><span class="sxs-lookup"><span data-stu-id="6d182-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="6d182-122">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="6d182-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="6d182-123">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="6d182-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="6d182-124">Aktivieren Sie das Kontrollkästchen **Objekt Pooling aktivieren** , um das Objekt Pooling für die Komponente zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d182-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="6d182-125">Geben Sie im Feld **minimale Poolgröße** die Mindestanzahl von Objekten dieses Typs in den Pool ein.</span><span class="sxs-lookup"><span data-stu-id="6d182-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="6d182-126">Der Pool wird so verwaltet, dass er mindestens über diese Anzahl von Objekten verfügt.</span><span class="sxs-lookup"><span data-stu-id="6d182-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="6d182-127">Geben Sie im Feld u die maximale Anzahl von Objekten dieses Typs in den Pool ein.</span><span class="sxs-lookup"><span data-stu-id="6d182-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="6d182-128">Die Anzahl der aktivierten und deaktivierten Objekte überschreitet diesen Wert nie.</span><span class="sxs-lookup"><span data-stu-id="6d182-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="6d182-129">Geben Sie im Feld **Erstellungs Timeout (MS)** die Zeitspanne in Millisekunden ein, die ein Client auf ein in einem Pool zusammen gefases Objekt wartet, wenn es nicht sofort verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6d182-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d182-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d182-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d182-131">Objekt Statistik überwachen</span><span class="sxs-lookup"><span data-stu-id="6d182-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
