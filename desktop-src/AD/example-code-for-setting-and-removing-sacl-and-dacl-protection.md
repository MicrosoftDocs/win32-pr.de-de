---
title: Beispiel Code für das Festlegen und Entfernen von SACL-und DACL-Schutz
description: Dieses Thema enthält ein Codebeispiel, das zum Festlegen und Entfernen von SACL-und DACL-Schutz verwendet wird.
ms.assetid: 1982ee9a-022a-4e5d-be9c-fab8894afa9e
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, festlegen und Entfernen von SACL-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c77cb1da29aa650fe4559c3da27c6a00f59e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106340896"
---
# <a name="example-code-for-setting-and-removing-sacl-and-dacl-protection"></a><span data-ttu-id="38a66-104">Beispiel Code für das Festlegen und Entfernen von SACL-und DACL-Schutz</span><span class="sxs-lookup"><span data-stu-id="38a66-104">Example Code for Setting and Removing SACL and DACL Protection</span></span>

<span data-ttu-id="38a66-105">Dieses Thema enthält ein Codebeispiel, das zum Festlegen und Entfernen von SACL-und DACL-Schutz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38a66-105">This topic includes a code example used to set and remove SACL and DACL protection.</span></span>

<span data-ttu-id="38a66-106">Im folgenden C-und C++-Codebeispiel werden die von " **SE \_ DACL \_ Protected** " und " **SE \_ SACL" \_ geschützten** Elemente in der [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Eigenschaft einer Objekt Sicherheits Beschreibung festgelegt und entfernt.</span><span class="sxs-lookup"><span data-stu-id="38a66-106">The following C and C++ code example sets and removes the **SE\_DACL\_PROTECTED** and **SE\_SACL\_PROTECTED** elements in the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property of an object security descriptor.</span></span>


```C++
/***************************************************************************

    SetSDInheritProtect()

    This function sets and removes the SE_DACL_PROTECTED and 
    SE_SACL_PROTECTED elements in the Control property. Valid values for 
    lControl are:
        0 - Remove both SE_DACL_PROTECTED and SE_SACL_PROTECTED if they are 
        set.

        SE_DACL_PROTECTED - Add SE_DACL_PROTECTED and remove SE_SACL_PROTECTED.

        SE_SACL_PROTECTED - Add SE_SACL_PROTECTED and remove SE_DACL_PROTECTED.

    Be aware that SE_DACL_PRESENT must be present to set SE_DACL_PROTECTED 
    and SE_SACL_PRESENT must be present to set SE_SACL_PROTECTED.
 
***************************************************************************/

HRESULT SetSDInheritProtect(IADs *pObject, long lControl)
{
    if(!pObject)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    CComVariant svar;
    long lSetControl;
    long lOriginalControl;

    // Get the nTSecurityDescriptor
    CComBSTR sbstrAttribute = "nTSecurityDescriptor";
    hr = pObject->Get(sbstrAttribute, &svar);
    if(FAILED(hr))
    {
        return hr;
    }
    
    /*
    The type should be VT_DISPATCH which is an IDispatch pointer to the security 
    descriptor object.
    */
    if(svar.vt != VT_DISPATCH)
    {
        return E_FAIL;
    }

    /*
    Get the IDispatch pointer from VARIANT structure and call the QueryInterface method for 
    the IADsSecurityDescriptor pointer.
    */
    CComPtr<IADsSecurityDescriptor> spSD;
    hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (void**)&spSD);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the Control property.
    hr = spSD->get_Control(&lSetControl);
    if(FAILED(hr))
    {
        return hr;
    }

    // Save the original value to see if the value changes.
    lOriginalControl = lSetControl;

    if(lControl & SE_DACL_PROTECTED)
    {
        lSetControl |= SE_DACL_PROTECTED;
        lSetControl &= !SE_SACL_PROTECTED;
    }
    else if(lControl & SE_SACL_PROTECTED)
    {
        lSetControl |= SE_SACL_PROTECTED;
        lSetControl &= !SE_DACL_PROTECTED;
    }
    else
    {
        lSetControl &= !SE_DACL_PROTECTED;
        lSetControl &= !SE_SACL_PROTECTED;
    }

    /*
    If there was change to the Control property, write it to the Security 
    Descriptor, write the SD to object, and then call SetInfo to write the 
    object to the directory.
    */
    if(lOriginalControl != lSetControl)
    {
        hr = spSD->put_Control(lSetControl);
        if(SUCCEEDED(hr))
        {
            hr = pObject->Put(sbstrAttribute, svar);
            if(SUCCEEDED(hr))
            {
                hr = pObject->SetInfo();
            }
        }
    }

    return hr;
}
```



 

 