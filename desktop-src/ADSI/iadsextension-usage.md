---
title: IADsExtension Usage
description: Dieses Thema enthält C++-Codebeispiele für die Verwendung der IADsExtension-Schnittstelle.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- extensions ADSI , IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab6813a87701fe2d7e130a03540476412c9e13b9d5d3ca96bdd0e63b2dad54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023488"
---
# <a name="iadsextension-usage"></a>IADsExtension Usage

[**IADsExtension ist**](/windows/desktop/api/Iads/nn-iads-iadsextension) eine optionale Schnittstelle, die vom Erweiterungswriter implementiert wird, wenn mindestens eine der folgenden Bedingungen erfüllt ist:

-   Die Erweiterungskomponente erfordert eine Initialisierungsbenachrichtigung, wie durch **ADSI \_ EXT \_ *dwCode*** in der [**Operate-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) definiert.
-   Die Erweiterung unterstützt eine Dual- oder Dispatch-Schnittstelle.

Wenn eine Erweiterungskomponente die [**IADsExtension-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsextension) aus dem ersten Grund unterstützt, können die [**Methoden IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) und [**IADsExtension::P rivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) **E \_ NOTIMPL zurückgeben.** Wenn eine Erweiterungskomponente eine Dual- oder Dispatch-Schnittstelle unterstützt, kann die [**Operate-Methode**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) alternativ die Daten ignorieren und ein **HRESULT** von **E \_ NOTIMPL zurückgeben.**

Der folgende Code zeigt eine Erweiterung, die [**IADsExtension implementieren.**](/windows/desktop/api/Iads/nn-iads-iadsextension)


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



 

 




