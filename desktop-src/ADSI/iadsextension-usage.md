---
title: Iadsextension-Verwendung
description: Dieses Thema enthält C++-Codebeispiele für die Verwendung der iadsextension-Schnittstelle.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, iadsextension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206242"
---
# <a name="iadsextension-usage"></a><span data-ttu-id="f0882-104">Iadsextension-Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0882-104">IADsExtension Usage</span></span>

<span data-ttu-id="f0882-105">[**Iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ist eine optionale Schnittstelle, die vom erweiterungswriter implementiert wird, wenn mindestens eine der folgenden Bedingungen erfüllt ist:</span><span class="sxs-lookup"><span data-stu-id="f0882-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) is an optional interface implemented by the extension writer when at least one of the following conditions are met:</span></span>

-   <span data-ttu-id="f0882-106">Die Erweiterungs Komponente erfordert eine Initialisierungs Benachrichtigung, wie von **ADSI \_ Ext \_ \* dwcode**\* in der Operation [**-Methode definiert**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="f0882-106">The extension component requires an initialization notification as defined by **ADSI\_EXT\_\*dwCode**\* in the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span>
-   <span data-ttu-id="f0882-107">Die Erweiterung unterstützt eine Dual-oder Dispatch-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f0882-107">The extension supports a dual or dispatch interface.</span></span>

<span data-ttu-id="f0882-108">Wenn eine Erweiterungs Komponente die [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle aus dem ersten Grund unterstützt, können die [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -Methode und die [**iadsextension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methode **E \_ notimpl** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f0882-108">If an extension component supports the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for the first reason, the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**IADsExtension::PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods can return **E\_NOTIMPL**.</span></span> <span data-ttu-id="f0882-109">Wenn eine Erweiterungs Komponente eine Dual-oder Dispatch-Schnittstelle unterstützt, kann die Operation [**-Methode die**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Daten ignorieren und ein **HRESULT** von **E \_ notimpl** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f0882-109">Alternatively, if an extension component supports a dual or dispatch interface , the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method can ignore the data and return an **HRESULT** of **E\_NOTIMPL**.</span></span>

<span data-ttu-id="f0882-110">Der folgende Code zeigt eine Erweiterung, die [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)implementiert.</span><span class="sxs-lookup"><span data-stu-id="f0882-110">The following code shows an extension implementing [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




