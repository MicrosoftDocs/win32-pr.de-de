---
description: Funktionsweise von IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funktionsweise von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123457"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="b6939-103">Funktionsweise von IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6939-103">How IUnknown Works</span></span>

<span data-ttu-id="b6939-104">Die Methoden in **IUnknown** ermöglichen einer Anwendung das Abfragen von Schnittstellen für die Komponente und das Verwalten des Verweis Zählers der Komponente.</span><span class="sxs-lookup"><span data-stu-id="b6939-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="b6939-105">**Verweisanzahl**</span><span class="sxs-lookup"><span data-stu-id="b6939-105">**Reference Count**</span></span>

<span data-ttu-id="b6939-106">Der Verweis Zähler ist eine interne Variable, die in der **adressf** -Methode inkrementiert und in der **releasemethode** dekrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b6939-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="b6939-107">Die Basisklassen verwalten den Verweis Zähler und synchronisieren den Zugriff auf den Verweis Zähler zwischen mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="b6939-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="b6939-108">**Schnittstellen Abfragen**</span><span class="sxs-lookup"><span data-stu-id="b6939-108">**Interface Queries**</span></span>

<span data-ttu-id="b6939-109">Das Abfragen für eine Schnittstelle ist ebenfalls unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="b6939-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="b6939-110">Der Aufrufer übergibt zwei Parameter: einen Schnittstellen Bezeichner (IID) und die Adresse eines Zeigers.</span><span class="sxs-lookup"><span data-stu-id="b6939-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="b6939-111">Wenn die Komponente die angeforderte Schnittstelle unterstützt, legt Sie den Zeiger auf die Schnittstelle fest, erhöht Ihren eigenen Verweis Zähler und gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b6939-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="b6939-112">Andernfalls wird der Zeiger auf **null** festgelegt und E \_ nointerface zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6939-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="b6939-113">Der folgende Pseudo Code zeigt die allgemeine Gliederung der **QueryInterface** -Methode.</span><span class="sxs-lookup"><span data-stu-id="b6939-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="b6939-114">Die Komponenten Aggregation, die im nächsten Abschnitt beschrieben wird, führt zu einer zusätzlichen Komplexität.</span><span class="sxs-lookup"><span data-stu-id="b6939-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



<span data-ttu-id="b6939-115">Der einzige Unterschied zwischen der **QueryInterface** -Methode einer Komponente und der **QueryInterface** -Methode eines anderen ist die Liste der IIDs, die von den einzelnen Komponenten getestet werden.</span><span class="sxs-lookup"><span data-stu-id="b6939-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="b6939-116">Für jede Schnittstelle, die von der Komponente unterstützt wird, muss die Komponente die IID der Schnittstelle testen.</span><span class="sxs-lookup"><span data-stu-id="b6939-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="b6939-117">**Aggregation und Delegierung**</span><span class="sxs-lookup"><span data-stu-id="b6939-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="b6939-118">Die Komponenten Aggregation muss für den Aufrufer transparent sein.</span><span class="sxs-lookup"><span data-stu-id="b6939-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="b6939-119">Daher muss das Aggregat eine einzelne **IUnknown** -Schnittstelle verfügbar machen, wobei die aggregierte Komponente auf die Implementierung der äußeren Komponente zurückschiebt.</span><span class="sxs-lookup"><span data-stu-id="b6939-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="b6939-120">Andernfalls würde der Aufrufer zwei verschiedene **IUnknown** -Schnittstellen im selben Aggregat sehen.</span><span class="sxs-lookup"><span data-stu-id="b6939-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="b6939-121">Wenn die Komponente nicht aggregiert wird, verwendet Sie eine eigene Implementierung.</span><span class="sxs-lookup"><span data-stu-id="b6939-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="b6939-122">Um dieses Verhalten zu unterstützen, muss die Komponente eine Dereferenzierungsebene hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b6939-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="b6939-123">Ein *delegier ender IUnknown* delegiert die Arbeit an die entsprechende Stelle: an die äußere Komponente, sofern vorhanden, oder an die interne Version der Komponente.</span><span class="sxs-lookup"><span data-stu-id="b6939-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="b6939-124">Ein nicht *delegier Endes IUnknown* führt die Arbeit aus, wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6939-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="b6939-125">Die delegier Ende Version ist öffentlich und behält den Namen " **IUnknown**" bei.</span><span class="sxs-lookup"><span data-stu-id="b6939-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="b6939-126">Die nicht delegier Ende Version wurde in [**inondelegatingunknown**](inondelegatingunknown.md)umbenannt.</span><span class="sxs-lookup"><span data-stu-id="b6939-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="b6939-127">Dieser Name ist nicht Teil der com-Spezifikation, da es sich nicht um eine öffentliche Schnittstelle handelt.</span><span class="sxs-lookup"><span data-stu-id="b6939-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="b6939-128">Wenn der Client eine Instanz der Komponente erstellt, wird die **IClassFactory::** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b6939-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="b6939-129">Ein Parameter ist ein Zeiger auf die **IUnknown** -Schnittstelle der aggregatkomponente oder **null** , wenn die neue Instanz nicht aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="b6939-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="b6939-130">Die Komponente speichert mithilfe dieses Parameters eine Member-Variable, die angibt, welche **IUnknown** -Schnittstelle verwendet werden soll, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b6939-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



<span data-ttu-id="b6939-131">Jede Methode in der delegierenden **IUnknown** -Methode ruft ihren nicht delegierenden Gegenstück auf, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b6939-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="b6939-132">Aufgrund der Art der Delegierung sehen die delegatenmethoden in jeder Komponente identisch aus.</span><span class="sxs-lookup"><span data-stu-id="b6939-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="b6939-133">Nur die nicht delegierenden Versionen werden geändert.</span><span class="sxs-lookup"><span data-stu-id="b6939-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6939-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6939-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6939-135">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6939-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



