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
# <a name="iadsextension-interface"></a><span data-ttu-id="d98b4-106">IADsExtension-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d98b4-106">IADsExtension Interface</span></span>

<span data-ttu-id="d98b4-107">Die [**IADsExtension-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsextension) ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="d98b4-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


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



<span data-ttu-id="d98b4-108">Der Aggregator (ADSI) ruft die [**IADsExtension::Operate-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) auf.</span><span class="sxs-lookup"><span data-stu-id="d98b4-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="d98b4-109">Die Erweiterung sollte den *dwCode-Parameter* und jeden *varData-Parameter* gemäß der Dokumentation des Anbieters interpretieren.</span><span class="sxs-lookup"><span data-stu-id="d98b4-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="d98b4-110">Der Aggregator (ADSI) ruft die [**IADsExtension::P rivateGetIDsOfNames-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) auf.</span><span class="sxs-lookup"><span data-stu-id="d98b4-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="d98b4-111">Sie wird aufgerufen, nachdem ADSI die Erweiterung zum Service der Dispatch bestimmt hat.</span><span class="sxs-lookup"><span data-stu-id="d98b4-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="d98b4-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span><span class="sxs-lookup"><span data-stu-id="d98b4-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="d98b4-113">ADSI ruft normalerweise die [**PrivateInvoke-Methode auf,**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) nachdem die [**PrivateGetIDsOfNames-Funktion aufruft.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="d98b4-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="d98b4-114">Die Erweiterung sollte die tatsächliche Methode aufrufen, die sie implementiert.</span><span class="sxs-lookup"><span data-stu-id="d98b4-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="d98b4-115">Alternativ kann die Erweiterung Typinformationen verwenden und die [**DispInvoke-Funktion**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d98b4-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="d98b4-116">Alle Parameter haben die gleiche Bedeutung wie die Parameter in der [**IDispatch::Invoke-Standardmethode.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)</span><span class="sxs-lookup"><span data-stu-id="d98b4-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 