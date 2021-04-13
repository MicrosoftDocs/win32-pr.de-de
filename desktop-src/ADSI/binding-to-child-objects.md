---
title: Binden an untergeordnete Objekte
description: In ADSI macht ein Container Objekt die IADsContainer-Schnittstelle verfügbar.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindung an untergeordnete Objekte
- Binden an untergeordnete Objekte
- Untergeordnete Objekte, binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474212"
---
# <a name="binding-to-child-objects"></a>Binden an untergeordnete Objekte

In ADSI macht ein Container Objekt die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle verfügbar. Die [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) -Methode wird verwendet, um eine direkte Bindung an ein untergeordnetes Objekt herzustellen. Das von **IADsContainer:: GetObject** zurückgegebene Objekt hat denselben Sicherheitskontext wie das Objekt, für das die Methode aufgerufen wurde. Dies bedeutet, dass, wenn alternative Anmelde Informationen verwendet werden, die alternativen Anmelde Informationen nicht erneut an die Bindungs Funktion oder-Methode weitergegeben werden müssen, um dieselben Anmelde Informationen zu erhalten.

Die [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) -Methode nimmt einen relativen Distinguished Name (RDN) auf, der relativ zum aktuellen Objekt ist. Diese Methode nimmt auch einen optionalen Klassennamen an und gibt einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger zurück, der das untergeordnete Objekt darstellt. Rufen Sie zum Abrufen der gewünschten ADSI-Schnittstelle, wie z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode dieses **IDispatch** -Schnittstellen Zeigers auf.

Im folgenden C++-Codebeispiel wird eine Funktion gezeigt, die ein angegebenes untergeordnetes Objekt abruft.


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 