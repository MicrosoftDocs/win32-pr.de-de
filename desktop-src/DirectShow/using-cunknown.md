---
description: DirectShow implementiert IUnknown in einer Basisklasse mit dem Namen cunknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Verwenden von cunknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348710"
---
# <a name="using-cunknown"></a><span data-ttu-id="d6cec-103">Verwenden von cunknown</span><span class="sxs-lookup"><span data-stu-id="d6cec-103">Using CUnknown</span></span>

<span data-ttu-id="d6cec-104">DirectShow implementiert [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in einer Basisklasse mit dem Namen [**cunknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d6cec-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="d6cec-105">Sie können mit **cunknown** andere Klassen ableiten und nur die Methoden überschreiben, die sich Komponenten übergreifend ändern.</span><span class="sxs-lookup"><span data-stu-id="d6cec-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="d6cec-106">Die meisten anderen Basisklassen in DirectShow werden von **cunknown** abgeleitet, sodass Ihre Komponente direkt von **cunknown** oder einer anderen Basisklasse erben kann.</span><span class="sxs-lookup"><span data-stu-id="d6cec-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="d6cec-107">Inondelegatingunknown</span><span class="sxs-lookup"><span data-stu-id="d6cec-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="d6cec-108">[**Cunknown**](cunknown.md) implementiert [**inondelegatingunknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d6cec-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="d6cec-109">Sie verwaltet Verweis Zähler intern, und in den meisten Fällen kann die abgeleitete Klasse die beiden Verweis Zählmethoden ohne Änderung erben.</span><span class="sxs-lookup"><span data-stu-id="d6cec-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="d6cec-110">Beachten Sie, dass **cunknown** sich selbst löscht, wenn der Verweis Zähler auf 0 (null) sinkt.</span><span class="sxs-lookup"><span data-stu-id="d6cec-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="d6cec-111">Andererseits müssen Sie [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md)überschreiben, da die-Methode in der Basisklasse E nointerface zurückgibt, \_ Wenn Sie eine andere IID als IID \_ IUnknown empfängt.</span><span class="sxs-lookup"><span data-stu-id="d6cec-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="d6cec-112">Testen Sie in der abgeleiteten Klasse die IIDs der Schnittstellen, die Sie unterstützen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d6cec-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="d6cec-113">Die Hilfsprogrammfunktion [**GetInterface**](getinterface.md) (siehe [**com**](com-helper-functions.md)-Hilfselemente) legt den-Zeiger fest, erhöht den Verweis Zähler auf Thread sichere Weise und gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d6cec-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="d6cec-114">Im Standardfall wird die Basisklassen Methode aufgerufen und das Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6cec-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="d6cec-115">Wenn Sie von einer anderen Basisklasse ableiten, müssen Sie stattdessen die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6cec-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="d6cec-116">Dadurch können Sie alle Schnittstellen unterstützen, die von der übergeordneten Klasse unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d6cec-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="d6cec-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6cec-117">IUnknown</span></span>

<span data-ttu-id="d6cec-118">Wie bereits erwähnt, ist die delegier Ende Version von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für jede Komponente identisch, da Sie nichts anderes bewirkt, als die richtige Instanz der nicht delegierenden Version aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6cec-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="d6cec-119">Aus Gründen der Bequemlichkeit enthält die Header Datei "ComBase. h" ein Makro, [**deklarieren Sie " \_ IUnknown**](declare-iunknown.md)", das die drei delegierenden Methoden als Inline Methoden deklariert.</span><span class="sxs-lookup"><span data-stu-id="d6cec-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="d6cec-120">Es wird auf den folgenden Code erweitert:</span><span class="sxs-lookup"><span data-stu-id="d6cec-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="d6cec-121">Die Utility-Funktion [**cunknown:: GetOwner**](cunknown-getowner.md) Ruft einen Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle der Komponente ab, die diese Komponente besitzt.</span><span class="sxs-lookup"><span data-stu-id="d6cec-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="d6cec-122">Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente.</span><span class="sxs-lookup"><span data-stu-id="d6cec-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="d6cec-123">Andernfalls ist die Komponente eigenständig.</span><span class="sxs-lookup"><span data-stu-id="d6cec-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="d6cec-124">Fügen Sie das \_ Makro DECLARE IUnknown in den Abschnitt Public der Klassendefinition ein.</span><span class="sxs-lookup"><span data-stu-id="d6cec-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="d6cec-125">Klassenkonstruktor</span><span class="sxs-lookup"><span data-stu-id="d6cec-125">Class Constructor</span></span>

<span data-ttu-id="d6cec-126">Der Klassenkonstruktor sollte zusätzlich zu allem, was für Ihre Klasse spezifisch ist, die Konstruktormethode für die übergeordnete Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d6cec-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="d6cec-127">Das folgende Beispiel ist eine typische Konstruktormethode:</span><span class="sxs-lookup"><span data-stu-id="d6cec-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="d6cec-128">Die-Methode übernimmt die folgenden Parameter, die Sie direkt an die [**cunknown**](cunknown.md) -Konstruktormethode übergibt.</span><span class="sxs-lookup"><span data-stu-id="d6cec-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="d6cec-129">*zzname* gibt einen Namen für die Komponente an.</span><span class="sxs-lookup"><span data-stu-id="d6cec-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="d6cec-130">der *Punk* ist ein Zeiger auf die Aggregations- [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d6cec-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="d6cec-131">*PHR* ist ein Zeiger auf einen HRESULT-Wert, der angibt, dass die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d6cec-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="d6cec-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d6cec-132">Summary</span></span>

<span data-ttu-id="d6cec-133">Das folgende Beispiel zeigt eine abgeleitete Klasse, die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und eine hypothetische Schnittstelle mit dem Namen "isominput Face" unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d6cec-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="d6cec-134">In diesem Beispiel werden die folgenden Punkte veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d6cec-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="d6cec-135">Die [**cunknown**](cunknown.md) -Klasse implementiert die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d6cec-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d6cec-136">Die neue Komponente erbt von **cunknown** und von allen Schnittstellen, die von der Komponente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d6cec-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="d6cec-137">Die Komponente kann stattdessen von einer anderen Basisklasse abgeleitet werden, die von **cunknown** erbt.</span><span class="sxs-lookup"><span data-stu-id="d6cec-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="d6cec-138">Das-Makro [**Declare \_ IUnknown**](declare-iunknown.md) deklariert die delegierenden [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methoden als Inline Methoden.</span><span class="sxs-lookup"><span data-stu-id="d6cec-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="d6cec-139">Die [**cunknown**](cunknown.md) -Klasse stellt die Implementierung für [**inondelegatingunknown**](inondelegatingunknown.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="d6cec-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="d6cec-140">Zur Unterstützung einer anderen Schnittstelle als [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)muss die abgeleitete Klasse die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode überschreiben und die IID der neuen Schnittstelle testen.</span><span class="sxs-lookup"><span data-stu-id="d6cec-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="d6cec-141">Der Klassenkonstruktor Ruft die Konstruktormethode für [**cunknown**](cunknown.md)auf.</span><span class="sxs-lookup"><span data-stu-id="d6cec-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="d6cec-142">Der nächste Schritt beim Schreiben eines Filters besteht darin, eine Anwendung zum Erstellen neuer Instanzen der Komponente zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6cec-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="d6cec-143">Dies erfordert ein Verständnis der DLLs und deren Beziehung zu Klassenfactorys und Klassenkonstruktormethoden.</span><span class="sxs-lookup"><span data-stu-id="d6cec-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="d6cec-144">Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d6cec-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6cec-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6cec-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6cec-146">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6cec-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
