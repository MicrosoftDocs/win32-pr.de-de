---
title: Unterstützung für duale Schnittstellen
description: Wie die Dispatch-Schnittstelle müssen alle Dual Schnittstellen von IDispatch erben, die alle IDispatch-Funktionen (GetIDsOfNames, Aufruf, GetTypeInfo, GetTypeInfoCount) zurück an die IDispatch des Aggregators (ADSI) delegiert.
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Unterstützen von Dual-oder Dispatch-Schnittstellen ADSI
- Erweiterungen ADSI, Dual oder Dispatch Interfaces
- ADSI ADSI, Beispielcode C/C++, Delegierung von IDispatch-Methoden an den Aggregator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338492"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="25df4-106">Unterstützung für duale Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="25df4-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="25df4-107">Wie die Dispatch-Schnittstelle müssen alle Dual Schnittstellen von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)erben, die alle **IDispatch** -Funktionen ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Aufruf**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) zurück an die **IDispatch** des Aggregators (ADSI) delegiert.</span><span class="sxs-lookup"><span data-stu-id="25df4-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="25df4-108">Zum Delegieren sollte ein Erweiterungs Objekt die **IDispatch** des Aggregators Abfragen, die entsprechende Aggregator-Methode aufzurufen und den Zeiger nach der Verwendung freigeben.</span><span class="sxs-lookup"><span data-stu-id="25df4-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="25df4-109">Wenn die Erweiterung eine eigenständige Komponente sein kann, überprüfen Sie, ob Sie aggregiert ist.</span><span class="sxs-lookup"><span data-stu-id="25df4-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="25df4-110">Wenn dies der Fall ist, leiten Sie die Dispatch-Funktionen an die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) des Aggregators um. andernfalls können Sie die interne Implementierung von **IDispatch** aufzurufen, oder Sie können Ihre Implementierung von [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="25df4-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="25df4-111">Im folgenden Codebeispiel wird gezeigt, wie der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Befehl an die **IDispatch** des Aggregators umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="25df4-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="25df4-112">In diesem Codebeispiel wird davon ausgegangen, dass die Member-Variable **m \_ pouterunknown** mit dem **IUnknown** -Zeiger des Aggregators initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="25df4-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



<span data-ttu-id="25df4-113">Erweiterungs Schreiber wird dringend empfohlen, duale Schnittstellen anstelle von Dispatchschnittstellen in ihren Erweiterungs Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="25df4-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="25df4-114">Eine duale Schnittstelle ermöglicht einem Client einen schnelleren Zugriff, solange der vtable-Zugriff im Client aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="25df4-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="25df4-115">Weitere Informationen finden Sie unter [späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="25df4-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="25df4-116">Basierend auf dem aktuellen Modell sollte das Implementieren von Dual-Schnittstellen nicht schwieriger sein als das Implementieren von Dispatch-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="25df4-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 