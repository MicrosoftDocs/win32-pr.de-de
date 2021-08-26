---
title: Unterstützen von Dual- oder Dispatch-Schnittstellen
description: Wie die Dispatchschnittstelle müssen alle dualen Schnittstellen von IDispatch erben, das alle seine IDispatch-Funktionen (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) zurück an das IDispatch des Aggregators (ADSI) delegiert.
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Unterstützung von Dual- oder Dispatch-Schnittstellen ADSI
- AdsI-, Dual- oder Dispatch-Erweiterungsschnittstellen
- ADSI ADSI , Beispielcode C/C++ , Delegieren von IDispatch-Methoden an den Aggregator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b783e9448926d6d29a27e5fb0db519175f82a9af1935e9f13655db743a946bcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930010"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Unterstützen von Dual- oder Dispatch-Schnittstellen

Wie die Dispatchschnittstelle müssen alle dualen Schnittstellen von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)erben, das alle seine **IDispatch-Funktionen** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) zurück an den **IDispatch** des Aggregators (ADSI) delegiert. Zum Delegieren sollte ein Erweiterungsobjekt den **IDispatch** des Aggregators abfragen, die entsprechende Aggregatormethode aufrufen und den Zeiger nach der Verwendung wieder frei geben.

Wenn die Erweiterung eine eigenständige Komponente sein kann, überprüfen Sie, ob sie aggregiert ist. Falls ja, werden die Dispatchfunktionen an [**das IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) des Aggregators umgeleitet. Andernfalls können Sie Ihre interne Implementierung von **IDispatch** aufrufen, oder Sie können Ihre Implementierung von [**IADsExtension aufrufen.**](/windows/desktop/api/Iads/nn-iads-iadsextension)

Das folgende Codebeispiel zeigt, wie sie den [**IDispatch-Aufruf**](/windows/win32/api/oaidl/nn-oaidl-idispatch) an **das IDispatch** des Aggregators umleiten. In diesem Codebeispiel wird davon ausgegangen, dass die **Membervariable m \_ pOuterUnknown** mit dem **IUnknown-Zeiger des Aggregators** initialisiert wurde.


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



Erweiterungsautoren wird dringend empfohlen, duale Schnittstellen anstelle von Dispatchschnittstellen in ihren Erweiterungsobjekten zu unterstützen. Eine duale Schnittstelle ermöglicht einem Client einen schnelleren Zugriff, solange der vtable-Zugriff im Client aktiviert ist. Weitere Informationen finden Sie unter [Späte Bindung im Vergleich zum Vtable-Zugriff im ADSI-Erweiterungsmodell.](late-binding-vs--vtable-access-in-the-adsi-extension-model.md) Basierend auf dem aktuellen Modell sollte die Implementierung von dualen Schnittstellen nicht schwieriger als die Implementierung von Dispatchschnittstellen sein.

 

 