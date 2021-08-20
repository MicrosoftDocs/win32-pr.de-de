---
description: Veranschaulicht, wie eine Zertifikatsperrliste abgerufen wird.
ms.assetid: b8fbffae-d968-453d-81f0-af9d60be5fa9
title: Abrufen einer Zertifikatsperrliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a301fd02b6a04c64a39471bdca03ff92f02d88f51f821af0c4b66a110300b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975061"
---
# <a name="retrieving-a-certificate-revocation-list"></a>Abrufen einer Zertifikatsperrliste

Eine [*Zertifizierungsstelle*](../secgloss/c-gly.md) ist für die Veröffentlichung ihrer [*Zertifikatsperrliste (Certificate Revocation List,*](../secgloss/c-gly.md) CRL) verantwortlich. Die aktuelle Zertifikatsperrliste kann mithilfe der [**ICertAdmin2::GetCRL-Methode**](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl) abgerufen werden. In Fällen, in denen das Zertifikat einer Zertifizierungsstelle erneuert wurde, müssen Sie möglicherweise CRLs für die vorherigen Zertifizierungsstellenzertifikate abrufen. Informationen zur Erneuerung von Zertifizierungsstellen finden Sie unter [Zertifizierungsstellenerneuerung.](certification-authority-renewal.md) Darüber hinaus kann eine Zertifizierungsstelle Delta-CRLs veröffentlichen. Um CRLs für erneuerte Zertifizierungsstellenzertifikate oder Delta-CRLs abzurufen, verwenden Sie entweder die Methoden [**ICertAdmin2::GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty) oder [**ICertRequest2::GetCAProperty.**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty)

Das folgende Beispiel zeigt das Abrufen der aktuellen CRL.


```C++
    ICertAdmin2 * pCertAdmin2 = NULL;  // pointer to interface object
    BSTR bstrCA = NULL;  // variable for computer\CAname
    BSTR bstrCRL = NULL;  // variable to contain the retrieved CRL
    HRESULT hr;

    // Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    // Create the CertAdmin object,
    // and get a pointer to its ICertAdmin interface.
    hr = CoCreateInstance( CLSID_CCertAdmin,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertAdmin2,
                           (void **)&pCertAdmin2;);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin2 [%x]\n", hr);
        goto error;
    }

    // Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (FAILED(hr))
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    // Retrieve the CRL.
    hr = pCertAdmin2->GetCRL( bstrCA, CR_OUT_BINARY, &bstrCRL );
    if (FAILED(hr))
    {
        printf("Failed GetCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("CRL retrieved successfully\n");
        // Use the CRL as needed...

    // Processing is finished.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCRL)
        SysFreeString(bstrCRL);

    // Clean up object resources.
    if (NULL != pCertAdmin2)
        pCertAdmin2->Release();

    // Free COM resources.
    CoUninitialize();
```



Das folgende Beispiel zeigt das Abrufen von Basis- und Delta-CRLs, einschließlich derjenigen für Zertifizierungsstellenzertifikate, die erneuert wurden. Im Beispiel wird [**ICertAdmin2::GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty)verwendet, obwohl [**ICertRequest2::GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) eine ähnliche Funktionalität bietet.


```C++
    LONG nCACertCount, nIndex, nCRLState;
    VARIANT    variant;

    VariantInit(&variant);
    // Determine the number of CA certificates.
    hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                CR_PROP_CASIGCERTCOUNT,
                                0,
                                PROPTYPE_LONG, 
                                CR_OUT_BINARY, 
                                &variant);
    if (FAILED(hr))
    {
        printf("Failed call to GetCAProperty - "
            "CR_PROP_CASIGCERTCOUNT\n");
        goto error;
    }
    nCACertCount = variant.lVal;

    for (nIndex = 0; nIndex < nCACertCount; nIndex++)
    {
           // Determine the CRL state for each certificate index.
           pCertAdmin2->GetCAProperty(bstrCA, 
                               CR_PROP_CRLSTATE, 
                               nIndex, 
                               PROPTYPE_LONG, 
                               CR_OUT_BINARY, 
                               &variant);
        if (FAILED(hr))
        {
            printf("Failed call to GetCAProperty - "
                "CR_PROP_CRLSTATE\n");
            goto error;
        }
        nCRLState = variant.lVal;

        // Process certificate indices only when 
        // the CRL state is valid.
        if (CA_DISP_VALID == nCRLState)
        {
           // Retrieve the base CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA,
                                   CR_PROP_BASECRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY,
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_BASECRL\n");
               goto error;
           }

           // Use the base CRL as needed (not shown).
           // ...

           // Retrieve the delta CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                   CR_PROP_DELTACRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY, 
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_DELTACRL\n");
               goto error;
           }

           // Use the delta CRL as needed (not shown).
           // ...

       }        
    }
    
    // Processing is finished.

error:

    // Clean up object resources.
    if ( NULL != pCertAdmin2 )
        pCertAdmin2->Release();

    // Free BSTR variables.
    if ( NULL != bstrCA )
        SysFreeString ( bstrCA );

    // Clear the variant.
    VariantClear(&variant);
```



 

 
