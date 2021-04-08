---
title: Iadsextension-Schnittstelle
description: Dieses Thema enthält C++-Codebeispiele für die Verwendung der iadsextension-Schnittstelle.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- Iadsextension ADSI, using
- ADSI ADSI, Beispielcode C/C++, using iadsextension
- Erweiterungen ADSI, iadsextension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730225"
---
# <a name="iadsextension-interface"></a>Iadsextension-Schnittstelle

Die [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle wird wie folgt definiert:


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



Der Aggregator (ADSI) Ruft die [**iadsextension::**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Operation-Methode auf. Die Erweiterung sollte den *dwcode* -Parameter und jeden *VARDATA* -Parameter entsprechend der Dokumentation des Anbieters interpretieren.

Der Aggregator (ADSI) Ruft die [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -Methode auf. Sie wird aufgerufen, nachdem ADSI die Erweiterung für die Dienst Verteilung bestimmt hat. Die Erweiterung könnte die Typinformationen zum erhalten der DISPID, d. h. die Funktion " [**dispgetidsofnames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) ", verwenden.

ADSI ruft nach dem Aufrufen der [**privategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -Funktion normalerweise die [**privateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methode auf. Die Erweiterung sollte die tatsächlich implementierte Methode aufzurufen. Alternativ können von der Erweiterung Typinformationen verwendet und die Funktion " [**dispcall"**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) aufgerufen werden.

Alle Parameter haben dieselbe Bedeutung wie die Parameter in der Standardmethode [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

 

 