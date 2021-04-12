---
title: Aggregation
description: Aggregation ist der Mechanismus für die Wiederverwendung von Objekten, bei dem das äußere Objekt Schnittstellen vom inneren Objekt verfügbar macht, als wären Sie auf dem äußeren Objekt selbst implementiert.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316533"
---
# <a name="aggregation"></a><span data-ttu-id="72646-103">Aggregation</span><span class="sxs-lookup"><span data-stu-id="72646-103">Aggregation</span></span>

<span data-ttu-id="72646-104">Aggregation ist der Mechanismus für die Wiederverwendung von Objekten, bei dem das äußere Objekt Schnittstellen vom inneren Objekt verfügbar macht, als wären Sie auf dem äußeren Objekt selbst implementiert.</span><span class="sxs-lookup"><span data-stu-id="72646-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="72646-105">Dies ist hilfreich, wenn das äußere Objekt alle Aufrufe an eine der Schnittstellen an die gleiche Schnittstelle im inneren Objekt delegiert.</span><span class="sxs-lookup"><span data-stu-id="72646-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="72646-106">Die Aggregation ist zur Vermeidung zusätzlicher Implementierungs Mehraufwand im äußeren Objekt in diesem Fall verfügbar.</span><span class="sxs-lookup"><span data-stu-id="72646-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="72646-107">Die Aggregation ist tatsächlich ein spezieller Fall von Kapselung [/Delegierung](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="72646-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="72646-108">Die Aggregation ist fast so einfach wie die Kapselung, mit Ausnahme der drei [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Funktionen: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="72646-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="72646-109">Der catch besteht aus der Sicht des Clients, dass sich jede **IUnknown** -Funktion für das äußere Objekt auf das äußere Objekt auswirken muss.</span><span class="sxs-lookup"><span data-stu-id="72646-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="72646-110">Das heißt, dass sich **adressf** und **Release** auf das äußere Objekt auswirken und **QueryInterface** alle für das äußere Objekt verfügbaren Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="72646-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="72646-111">Wenn das äußere Objekt jedoch einfach die Schnittstelle eines inneren Objekts als eigen macht, Verhalten sich die **IUnknown** -Member, die über diese Schnittstelle aufgerufen wurden, anders als die **IUnknown** -Member in den Schnittstellen des äußeren Objekts, eine absolute Verletzung der Regeln und Eigenschaften, die **IUnknown** steuern.</span><span class="sxs-lookup"><span data-stu-id="72646-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="72646-112">Die Lösung besteht darin, dass für die Aggregation eine explizite Implementierung von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das innere Objekt und die Delegierung der **IUnknown** -Methoden einer beliebigen anderen Schnittstelle zu den **IUnknown** -Methoden des äußeren Objekts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="72646-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="72646-113">Erstellen von aggrebfähigen Objekten</span><span class="sxs-lookup"><span data-stu-id="72646-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="72646-114">Das Erstellen von Objekten, die aggregiert werden können, ist optional. Es ist jedoch einfach zu tun und bietet bedeutende Vorteile.</span><span class="sxs-lookup"><span data-stu-id="72646-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="72646-115">Die folgenden Regeln gelten für das Erstellen eines aggretfähigen Objekts:</span><span class="sxs-lookup"><span data-stu-id="72646-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="72646-116">Die Implementierung von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle durch das aggregierte (oder innere) Objekt steuert den Verweis Zähler des inneren Objekts, und diese Implementierung darf nicht an das äußere Objekt (das steuernde **IUnknown**) delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="72646-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="72646-117">Die Implementierung von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die anderen Schnittstellen des aggreofähigen (oder inneren) Objekts muss an das steuernde [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) delegiert werden und darf sich nicht direkt auf den Verweis Zähler des inneren Objekts auswirken.</span><span class="sxs-lookup"><span data-stu-id="72646-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="72646-118">Das innere [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) muss [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nur für das innere Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="72646-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="72646-119">Beim Speichern eines Verweises auf den steuernden [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeiger darf das Aggregat Objekt keine [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="72646-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="72646-120">Wenn das Objekt erstellt wird und eine andere Schnittstelle als [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) angefordert wird, muss die Erstellung mit E \_ nointerface fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="72646-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="72646-121">Das folgende Code Fragment veranschaulicht eine korrekte Implementierung eines aggreterfähigen Objekts, indem die Methode der Methode der Methode zum Implementieren von Schnittstellen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="72646-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a><span data-ttu-id="72646-122">Aggregations Objekte</span><span class="sxs-lookup"><span data-stu-id="72646-122">Aggregating Objects</span></span>

<span data-ttu-id="72646-123">Beim Entwickeln eines aggrebfähigen Objekts gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="72646-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="72646-124">Beim Erstellen des inneren Objekts muss das äußere Objekt explizit nach [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)Fragen.</span><span class="sxs-lookup"><span data-stu-id="72646-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="72646-125">Das äußere Objekt muss seine Implementierung der [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) vor dem erneuten eintreten mit einem künstlichen Verweis Zähler um seinen Zerstörungs Code schützen.</span><span class="sxs-lookup"><span data-stu-id="72646-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="72646-126">Das äußere Objekt muss seine steuernde **IUnknown**- [**releasemethode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufruft, wenn es einen Zeiger auf eine der Schnittstellen des inneren Objekts abfragt.</span><span class="sxs-lookup"><span data-stu-id="72646-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="72646-127">Um diesen Zeiger freizugeben, ruft das äußere Objekt seine kontrollierte **IUnknown**- [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode auf, gefolgt vom **Release** auf dem-Zeiger des inneren Objekts.</span><span class="sxs-lookup"><span data-stu-id="72646-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="72646-128">Das äußere Objekt darf eine Abfrage für eine unbekannte Schnittstelle nicht blind an das innere Objekt delegieren, es sei denn, dieses Verhalten ist die Absicht des äußeren Objekts.</span><span class="sxs-lookup"><span data-stu-id="72646-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72646-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72646-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72646-130">Einschluss/Delegierung</span><span class="sxs-lookup"><span data-stu-id="72646-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 