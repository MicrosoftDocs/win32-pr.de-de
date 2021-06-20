---
title: IADsExtension-Schnittstelle
description: Dieser Artikel enthält die C++-Codedefinition der IADsExtension-Schnittstelle und eine Beschreibung ihrer Methoden.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI , using
- ADSI ADSI , Beispielcode C/C++ , mit IADsExtension
- Extensions ADSI , IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d59048d29620cdc2d3703b9ba26a852441a47
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405943"
---
# <a name="iadsextension-interface"></a>IADsExtension-Schnittstelle

Die [**IADsExtension-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsextension) ist wie folgt definiert:


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



Der Aggregator (ADSI) ruft die [**IADsExtension::Operate-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) auf. Die Erweiterung sollte den *dwCode-Parameter* und jeden *varData-Parameter* gemäß der Dokumentation des Anbieters interpretieren.

Der Aggregator (ADSI) ruft die [**IADsExtension::P rivateGetIDsOfNames-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) auf. Sie wird aufgerufen, nachdem ADSI die Erweiterung zum Service der Dispatch bestimmt hat. The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.

ADSI ruft normalerweise die [**PrivateInvoke-Methode auf,**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) nachdem die [**PrivateGetIDsOfNames-Funktion aufruft.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) Die Erweiterung sollte die tatsächliche Methode aufrufen, die sie implementiert. Alternativ kann die Erweiterung Typinformationen verwenden und die [**DispInvoke-Funktion**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) aufrufen.

Alle Parameter haben die gleiche Bedeutung wie die Parameter in der [**IDispatch::Invoke-Standardmethode.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)

 

 