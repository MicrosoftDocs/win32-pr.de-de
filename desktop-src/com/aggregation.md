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
# <a name="aggregation"></a>Aggregation

Aggregation ist der Mechanismus für die Wiederverwendung von Objekten, bei dem das äußere Objekt Schnittstellen vom inneren Objekt verfügbar macht, als wären Sie auf dem äußeren Objekt selbst implementiert. Dies ist hilfreich, wenn das äußere Objekt alle Aufrufe an eine der Schnittstellen an die gleiche Schnittstelle im inneren Objekt delegiert. Die Aggregation ist zur Vermeidung zusätzlicher Implementierungs Mehraufwand im äußeren Objekt in diesem Fall verfügbar. Die Aggregation ist tatsächlich ein spezieller Fall von Kapselung [/Delegierung](containment-delegation.md).

Die Aggregation ist fast so einfach wie die Kapselung, mit Ausnahme der drei [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Funktionen: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Der catch besteht aus der Sicht des Clients, dass sich jede **IUnknown** -Funktion für das äußere Objekt auf das äußere Objekt auswirken muss. Das heißt, dass sich **adressf** und **Release** auf das äußere Objekt auswirken und **QueryInterface** alle für das äußere Objekt verfügbaren Schnittstellen verfügbar macht. Wenn das äußere Objekt jedoch einfach die Schnittstelle eines inneren Objekts als eigen macht, Verhalten sich die **IUnknown** -Member, die über diese Schnittstelle aufgerufen wurden, anders als die **IUnknown** -Member in den Schnittstellen des äußeren Objekts, eine absolute Verletzung der Regeln und Eigenschaften, die **IUnknown** steuern.

Die Lösung besteht darin, dass für die Aggregation eine explizite Implementierung von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das innere Objekt und die Delegierung der **IUnknown** -Methoden einer beliebigen anderen Schnittstelle zu den **IUnknown** -Methoden des äußeren Objekts erforderlich ist.

## <a name="creating-aggregable-objects"></a>Erstellen von aggrebfähigen Objekten

Das Erstellen von Objekten, die aggregiert werden können, ist optional. Es ist jedoch einfach zu tun und bietet bedeutende Vorteile. Die folgenden Regeln gelten für das Erstellen eines aggretfähigen Objekts:

-   Die Implementierung von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle durch das aggregierte (oder innere) Objekt steuert den Verweis Zähler des inneren Objekts, und diese Implementierung darf nicht an das äußere Objekt (das steuernde **IUnknown**) delegiert werden.
-   Die Implementierung von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die anderen Schnittstellen des aggreofähigen (oder inneren) Objekts muss an das steuernde [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) delegiert werden und darf sich nicht direkt auf den Verweis Zähler des inneren Objekts auswirken.
-   Das innere [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) muss [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nur für das innere Objekt implementieren.
-   Beim Speichern eines Verweises auf den steuernden [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeiger darf das Aggregat Objekt keine [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Funktion abrufen.
-   Wenn das Objekt erstellt wird und eine andere Schnittstelle als [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) angefordert wird, muss die Erstellung mit E \_ nointerface fehlschlagen.

Das folgende Code Fragment veranschaulicht eine korrekte Implementierung eines aggreterfähigen Objekts, indem die Methode der Methode der Methode zum Implementieren von Schnittstellen verwendet wird:


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



## <a name="aggregating-objects"></a>Aggregations Objekte

Beim Entwickeln eines aggrebfähigen Objekts gelten die folgenden Regeln:

-   Beim Erstellen des inneren Objekts muss das äußere Objekt explizit nach [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)Fragen.
-   Das äußere Objekt muss seine Implementierung der [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) vor dem erneuten eintreten mit einem künstlichen Verweis Zähler um seinen Zerstörungs Code schützen.
-   Das äußere Objekt muss seine steuernde **IUnknown**- [**releasemethode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufruft, wenn es einen Zeiger auf eine der Schnittstellen des inneren Objekts abfragt. Um diesen Zeiger freizugeben, ruft das äußere Objekt seine kontrollierte **IUnknown**- [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode auf, gefolgt vom **Release** auf dem-Zeiger des inneren Objekts.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   Das äußere Objekt darf eine Abfrage für eine unbekannte Schnittstelle nicht blind an das innere Objekt delegieren, es sei denn, dieses Verhalten ist die Absicht des äußeren Objekts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschluss/Delegierung](containment-delegation.md)
</dt> </dl>

 

 