---
title: Aggregation
description: Aggregation ist der Mechanismus zur Objektwiederverwendung, bei dem das äußere Objekt Schnittstellen aus dem inneren Objekt verfügbar macht, als wären sie für das äußere Objekt selbst implementiert.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4855b1fa3a614d190b8f192aeee2e7cf3d3d53bbdce589a1363e0398f70430c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731720"
---
# <a name="aggregation"></a>Aggregation

Aggregation ist der Mechanismus zur Objektwiederverwendung, bei dem das äußere Objekt Schnittstellen aus dem inneren Objekt verfügbar macht, als wären sie für das äußere Objekt selbst implementiert. Dies ist nützlich, wenn das äußere Objekt jeden Aufruf einer seiner Schnittstellen an dieselbe Schnittstelle im inneren Objekt delegiert. Aggregation ist zur Vereinfachung verfügbar, um in diesem Fall zusätzlichen Implementierungsaufwand im äußeren Objekt zu vermeiden. Aggregation ist eigentlich ein spezieller Fall von [Einschluss/Delegierung.](containment-delegation.md)

Die Aggregation ist fast so einfach zu implementieren wie die Einschlussfunktion, mit Ausnahme der drei [**IUnknown-Funktionen:**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Der Catch ist, dass sich aus Sicht des Clients jede **IUnknown-Funktion** für das äußere Objekt auf das äußere Objekt auswirken muss. Das heißt, **AddRef** und **Release** wirken sich auf das äußere Objekt aus, und **QueryInterface** macht alle Schnittstellen verfügbar, die für das äußere Objekt verfügbar sind. Wenn das äußere Objekt jedoch einfach die Schnittstelle eines inneren Objekts als eigene verfügbar macht, verhalten sich die **IUnknown-Member** dieses inneren Objekts, die über diese Schnittstelle aufgerufen werden, anders als die **IUnknown-Member** in den Schnittstellen des äußeren Objekts. Dies ist ein absoluter Verstoß gegen die Regeln und Eigenschaften, die **IUnknown** steuern.

Die Lösung besteht darin, dass die Aggregation eine explizite Implementierung von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das innere Objekt und die Delegierung der **IUnknown-Methoden** einer beliebigen anderen Schnittstelle an die **IUnknown-Methoden** des äußeren Objekts erfordert.

## <a name="creating-aggregable-objects"></a>Erstellen von Aggregable-Objekten

Das Erstellen von Objekten, die aggregiert werden können, ist optional. dies ist jedoch einfach und bietet erhebliche Vorteile. Die folgenden Regeln gelten für das Erstellen eines aggregable-Objekts:

-   Die Implementierung von [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) des Aggregable-Objekts steuert den Verweiszähler des inneren Objekts, und diese Implementierung darf nicht an das unbekannte (das steuernde **IUnknown)** des äußeren Objekts delegiert werden.
-   Die Implementierung von [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) des aggregable -Objekts (oder inneren Objekts) für seine anderen Schnittstellen muss an die steuernde [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) delegiert werden und darf sich nicht direkt auf den Verweiszähler des inneren Objekts auswirken.
-   Der innere [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) muss [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nur für das innere Objekt implementieren.
-   Das aggregable-Objekt darf [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) nicht aufrufen, wenn ein Verweis auf den steuernden [**IUnknown-Zeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) gehalten wird.
-   Wenn beim Erstellen des Objekts eine andere Schnittstelle als [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) angefordert wird, muss die Erstellung mit E \_ NOINTERFACE fehlschlagen.

Das folgende Codefragment veranschaulicht eine korrekte Implementierung eines aggregable-Objekts mithilfe der geschachtelten Klassenmethode zum Implementieren von Schnittstellen:


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



## <a name="aggregating-objects"></a>Aggregieren von Objekten

Beim Entwickeln eines aggregable-Objekts gelten die folgenden Regeln:

-   Beim Erstellen des inneren Objekts muss das äußere Objekt explizit nach seinem [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)-Objekt fragen.
-   Das äußere Objekt muss seine Implementierung von [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) vor Erneutinvarianz mit einem künstlichen Verweiszähler um seinen Zerstörungscode schützen.
-   Das äußere Objekt muss seine steuernde **IUnknown** [**Release-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen, wenn es einen Zeiger auf eine der Schnittstellen des inneren Objekts abfragt. Um diesen Zeiger freizugeben, ruft das äußere Objekt seine steuernde **IUnknown** [**AddRef-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) auf, gefolgt von **Release** für den Zeiger des inneren Objekts.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   Das äußere Objekt darf eine Abfrage für nicht erkannte Schnittstellen nicht blind an das innere Objekt delegieren, es sei denn, dieses Verhalten ist speziell die Absicht des äußeren Objekts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschluss/Delegierung](containment-delegation.md)
</dt> </dl>

 

 