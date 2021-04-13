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
# <a name="binding-to-child-objects"></a><span data-ttu-id="f0e3e-106">Binden an untergeordnete Objekte</span><span class="sxs-lookup"><span data-stu-id="f0e3e-106">Binding to Child Objects</span></span>

<span data-ttu-id="f0e3e-107">In ADSI macht ein Container Objekt die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-107">In ADSI, a container object exposes the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span> <span data-ttu-id="f0e3e-108">Die [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) -Methode wird verwendet, um eine direkte Bindung an ein untergeordnetes Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-108">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind directly to a child object.</span></span> <span data-ttu-id="f0e3e-109">Das von **IADsContainer:: GetObject** zurückgegebene Objekt hat denselben Sicherheitskontext wie das Objekt, für das die Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-109">The object returned by **IADsContainer::GetObject** has the same security context as the object on which the method was called.</span></span> <span data-ttu-id="f0e3e-110">Dies bedeutet, dass, wenn alternative Anmelde Informationen verwendet werden, die alternativen Anmelde Informationen nicht erneut an die Bindungs Funktion oder-Methode weitergegeben werden müssen, um dieselben Anmelde Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-110">This means that if alternate credentials are used, the alternate credentials do not have to be passed to the binding function or method again to maintain the same credentials.</span></span>

<span data-ttu-id="f0e3e-111">Die [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) -Methode nimmt einen relativen Distinguished Name (RDN) auf, der relativ zum aktuellen Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-111">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method takes a relative distinguished name (RDN) that is relative to the current object.</span></span> <span data-ttu-id="f0e3e-112">Diese Methode nimmt auch einen optionalen Klassennamen an und gibt einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger zurück, der das untergeordnete Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-112">This method also takes an optional class name and returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface pointer that represents the child object.</span></span> <span data-ttu-id="f0e3e-113">Rufen Sie zum Abrufen der gewünschten ADSI-Schnittstelle, wie z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode dieses **IDispatch** -Schnittstellen Zeigers auf.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-113">To obtain the desired ADSI interface, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of this **IDispatch** interface pointer.</span></span>

<span data-ttu-id="f0e3e-114">Im folgenden C++-Codebeispiel wird eine Funktion gezeigt, die ein angegebenes untergeordnetes Objekt abruft.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-114">The following C++ code example shows a function that retrieves a specified child object.</span></span>


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



 

 