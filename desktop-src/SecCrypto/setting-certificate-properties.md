---
description: 'Verwenden Sie die icertserverpolicy:: setcertificateproperty-Methode, um die betreffeigenschaften eines Zertifikats festzulegen.'
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Festlegen von Zertifikat Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344240"
---
# <a name="setting-certificate-properties"></a>Festlegen von Zertifikat Eigenschaften

Verwenden Sie die [**icertserverpolicy:: setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) -Methode, um die betreffeigenschaften eines Zertifikats festzulegen. Betreffeigenschaften sind Eigenschaften, die mit dem Besitzer des Zertifikats oder der Person verknüpft sind, die das Zertifikat angefordert hat. Eine Liste der betreffeigenschaften finden Sie unter [Name Properties](name-properties.md).

Sie können auch die [**setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) -Methode verwenden, um die Eigenschaften "NotBefore" und "NotAfter Certificate" festzulegen. Eine Beschreibung der Eigenschaften "NotBefore" und "NotAfter Certificate" finden Sie unter [Zertifikat Eigenschaften](certificate-properties.md).

Verwenden Sie die [**icertserverpolicy:: setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) -Methode, um dem Zertifikat eine beliebige Anzahl von Erweiterungen hinzuzufügen. Sie können Erweiterungen verwenden, um zusätzliche Betreff-oder Nutzungsinformationen zum Zertifikat hinzuzufügen. Weitere Informationen finden Sie unter [Erweiterungs Handler](extension-handlers.md).

Im folgenden Beispiel werden eine Zertifikat Eigenschaft und eine Erweiterung für ein Zertifikat festgelegt. Sie aufrufen die Methoden [**setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) und [**setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) in Ihrer [**ICertPolicy2:: verifyrequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) -Implementierung. Bei dem Beispiel handelt es sich nicht um eine komplette **verifyrequest** -Implementierung. Das Beispiel zeigt keine Überprüfungs Logik an.


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



