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
# <a name="supporting-dual-or-dispatch-interfaces"></a>Unterstützung für duale Schnittstellen

Wie die Dispatch-Schnittstelle müssen alle Dual Schnittstellen von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)erben, die alle **IDispatch** -Funktionen ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Aufruf**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) zurück an die **IDispatch** des Aggregators (ADSI) delegiert. Zum Delegieren sollte ein Erweiterungs Objekt die **IDispatch** des Aggregators Abfragen, die entsprechende Aggregator-Methode aufzurufen und den Zeiger nach der Verwendung freigeben.

Wenn die Erweiterung eine eigenständige Komponente sein kann, überprüfen Sie, ob Sie aggregiert ist. Wenn dies der Fall ist, leiten Sie die Dispatch-Funktionen an die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) des Aggregators um. andernfalls können Sie die interne Implementierung von **IDispatch** aufzurufen, oder Sie können Ihre Implementierung von [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)aufzurufen.

Im folgenden Codebeispiel wird gezeigt, wie der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Befehl an die **IDispatch** des Aggregators umgeleitet wird. In diesem Codebeispiel wird davon ausgegangen, dass die Member-Variable **m \_ pouterunknown** mit dem **IUnknown** -Zeiger des Aggregators initialisiert wurde.


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



Erweiterungs Schreiber wird dringend empfohlen, duale Schnittstellen anstelle von Dispatchschnittstellen in ihren Erweiterungs Objekten zu unterstützen. Eine duale Schnittstelle ermöglicht einem Client einen schnelleren Zugriff, solange der vtable-Zugriff im Client aktiviert ist. Weitere Informationen finden Sie unter [späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). Basierend auf dem aktuellen Modell sollte das Implementieren von Dual-Schnittstellen nicht schwieriger sein als das Implementieren von Dispatch-Schnittstellen.

 

 