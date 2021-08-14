---
title: Beispielcode zum Festlegen und Entfernen von SACL- und DACL-Schutz
description: Dieses Thema enthält ein Codebeispiel zum Festlegen und Entfernen des SACL- und DACL-Schutzes.
ms.assetid: 1982ee9a-022a-4e5d-be9c-fab8894afa9e
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Festlegen und Entfernen des SACL-Schutzes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ed7c32ebdeb7408037e2e3fcff294f0750fb6a8dcd19837ee9154c65f0c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190152"
---
# <a name="example-code-for-setting-and-removing-sacl-and-dacl-protection"></a>Beispielcode zum Festlegen und Entfernen von SACL- und DACL-Schutz

Dieses Thema enthält ein Codebeispiel zum Festlegen und Entfernen des SACL- und DACL-Schutzes.

Im folgenden C- und C++-Codebeispiel werden die **SE \_ DACL \_ PROTECTED-** und **SE \_ SACL \_ PROTECTED-Elemente** in der [**IADsSecurityDescriptor.Control-Eigenschaft**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) eines Objektsicherheitsdeskriptors festgelegt und entfernt.


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



 

 