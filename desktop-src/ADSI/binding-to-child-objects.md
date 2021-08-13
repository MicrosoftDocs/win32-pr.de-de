---
title: Binden an untergeordnete Objekte
description: In ADSI macht ein Containerobjekt die IADsContainer-Schnittstelle verfügbar.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , using, Bindung an untergeordnete Objekte
- Binden an untergeordnete Objekte
- Untergeordnete Objekte, Binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e454da1aaea93acc404e92da4b9c45ac8d67b4c3cee8a4fe9a04027c7533b39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429037"
---
# <a name="binding-to-child-objects"></a>Binden an untergeordnete Objekte

In ADSI macht ein Containerobjekt die [**IADsContainer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verfügbar. Die [**IADsContainer::GetObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) wird verwendet, um direkt an ein untergeordnetes Objekt zu binden. Das von **IADsContainer::GetObject** zurückgegebene Objekt hat den gleichen Sicherheitskontext wie das Objekt, für das die Methode aufgerufen wurde. Dies bedeutet, dass bei Verwendung alternativer Anmeldeinformationen die alternativen Anmeldeinformationen nicht erneut an die Bindungsfunktion oder -methode übergeben werden müssen, um die gleichen Anmeldeinformationen beizubehalten.

Die [**IADsContainer::GetObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) verwendet einen relativen Distinguished Name (RDN), der relativ zum aktuellen Objekt ist. Diese Methode verwendet auch einen optionalen Klassennamen und gibt einen [**IDispatch-Schnittstellenzeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück, der das untergeordnete Objekt darstellt. Um die gewünschte ADSI-Schnittstelle wie [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)abzurufen, rufen Sie die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) dieses **IDispatch-Schnittstellenzeigers** auf.

Das folgende C++-Codebeispiel zeigt eine Funktion, die ein angegebenes untergeordnetes Objekt abruft.


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



 

 