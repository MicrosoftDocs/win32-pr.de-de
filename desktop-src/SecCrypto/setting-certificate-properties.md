---
description: Verwenden Sie die ICertServerPolicy::SetCertificateProperty-Methode, um die Betreffeigenschaften eines Zertifikats fest zu legen.
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Festlegen von Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe131190b10b431427162e628004d8b21053a099015a68184196b7218967222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974568"
---
# <a name="setting-certificate-properties"></a>Festlegen von Zertifikateigenschaften

Verwenden Sie [**die ICertServerPolicy::SetCertificateProperty-Methode,**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) um die Betreffeigenschaften eines Zertifikats fest zu legen. Betreffeigenschaften sind Eigenschaften im Zusammenhang mit dem Besitzer des Zertifikats oder der Person, die das Zertifikat angefordert hat. Eine Liste der Betreffeigenschaften finden Sie unter [Namenseigenschaften.](name-properties.md)

Sie können auch die [**SetCertificateProperty-Methode**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) verwenden, um die Zertifikateigenschaften NotBefore und NotAfter festlegen. Eine Beschreibung der NotBefore- und NotAfter-Zertifikateigenschaften finden Sie unter [Zertifikateigenschaften](certificate-properties.md).

Verwenden Sie [**die ICertServerPolicy::SetCertificateExtension-Methode,**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) um dem Zertifikat eine beliebige Anzahl von Erweiterungen hinzuzufügen. Sie können Erweiterungen verwenden, um dem Zertifikat zusätzliche Betreff- oder Nutzungsinformationen hinzuzufügen. Weitere Informationen finden Sie unter [Erweiterungshandler.](extension-handlers.md)

Im folgenden Beispiel werden eine Zertifikateigenschaft und eine Erweiterung für ein Zertifikat definiert. Sie rufen die [**Methoden SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) und [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) in Ihrer [**ICertPolicy2::VerifyRequest-Implementierung**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) auf. Das Beispiel ist keine vollständige **VerifyRequest-Implementierung.** Im Beispiel wird die Überprüfungslogik nicht gezeigt.


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



 

 



