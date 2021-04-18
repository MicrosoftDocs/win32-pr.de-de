---
title: Regeln für die Implementierung von QueryInterface
description: Regeln für die Implementierung von QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337875"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="f3882-103">Regeln für die Implementierung von QueryInterface</span><span class="sxs-lookup"><span data-stu-id="f3882-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="f3882-104">Es gibt drei Hauptregeln, die die Implementierung der [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für ein COM-Objekt Steuern:</span><span class="sxs-lookup"><span data-stu-id="f3882-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="f3882-105">Objekte müssen über eine Identität verfügen.</span><span class="sxs-lookup"><span data-stu-id="f3882-105">Objects must have identity.</span></span>
-   <span data-ttu-id="f3882-106">Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3882-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="f3882-107">Es muss möglich sein, für jede beliebige Schnittstelle eines Objekts von einer beliebigen anderen Schnittstelle aus erfolgreich eine Abfrage durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f3882-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="f3882-108">Objekte müssen über eine Identität verfügen.</span><span class="sxs-lookup"><span data-stu-id="f3882-108">Objects Must Have Identity</span></span>

<span data-ttu-id="f3882-109">Für eine beliebige Objektinstanz muss ein [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufrufe mit IID \_ IUnknown immer denselben physischen Zeiger Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f3882-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="f3882-110">Dies ermöglicht es Ihnen, **QueryInterface** für zwei beliebige Schnittstellen aufzurufen und die Ergebnisse zu vergleichen, um zu bestimmen, ob Sie auf dieselbe Instanz eines Objekts zeigen.</span><span class="sxs-lookup"><span data-stu-id="f3882-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="f3882-111">Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3882-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="f3882-112">Der Satz von Schnittstellen, der über [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Objekt zugänglich ist, muss statisch und nicht dynamisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3882-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="f3882-113">Wenn **QueryInterface** \_ z. b. für eine bestimmte IID einmal OK zurückgibt, darf es niemals E \_ nointerface für nachfolgende Aufrufe desselben Objekts zurückgeben. Wenn **QueryInterface** \_ für eine bestimmte IID e nointerface zurückgibt, dürfen nachfolgende Aufrufe für dieselbe IID für das gleiche Objekt niemals S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="f3882-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="f3882-114">Es muss möglich sein, für jede Schnittstelle eines Objekts von einer beliebigen anderen Schnittstelle aus erfolgreich eine Abfrage durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f3882-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="f3882-115">Das heißt, wenn der folgende Code angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="f3882-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="f3882-116">die folgenden Regeln gelten:</span><span class="sxs-lookup"><span data-stu-id="f3882-116">the following rules apply:</span></span>

-   <span data-ttu-id="f3882-117">Wenn Sie über einen Zeiger auf eine Schnittstelle für ein Objekt verfügen, muss ein-Befehl wie der folgende für [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für die gleiche Schnittstelle erfolgreich ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="f3882-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="f3882-118">Wenn ein Abruf von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für einen zweiten Schnittstellen Zeiger erfolgreich ist, muss auch der **QueryInterface** -Rückruf von diesem Zeiger für die erste Schnittstelle erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f3882-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="f3882-119">Wenn PB erfolgreich abgerufen wurde, muss Folgendes ebenfalls erfolgreich sein:</span><span class="sxs-lookup"><span data-stu-id="f3882-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="f3882-120">Jede Schnittstelle muss in der Lage sein, beliebige andere Schnittstellen in einem Objekt abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f3882-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="f3882-121">Wenn PB erfolgreich abgerufen wurde und Sie erfolgreich eine dritte Schnittstelle (IC) mithilfe dieses Zeigers abgefragt haben, müssen Sie auch in der Lage sein, mithilfe des ersten Zeigers (PA) erfolgreich eine Abfrage für den IC durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f3882-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="f3882-122">In diesem Fall muss die folgende Sequenz erfolgreich ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="f3882-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="f3882-123">Schnittstellen Implementierungen müssen einen Gegenstand von ausstehenden Zeiger verweisen auf alle Schnittstellen eines bestimmten Objekts beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f3882-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="f3882-124">Sie sollten eine **Ganzzahl ohne** Vorzeichen für den-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3882-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="f3882-125">Wenn ein Client wissen muss, dass Ressourcen freigegeben wurden, muss er eine Methode in einer Schnittstelle für das Objekt mit einer Semantik auf höherer Ebene verwenden, bevor [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f3882-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3882-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3882-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3882-127">Verwenden und Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3882-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 