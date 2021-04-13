---
title: Beispiel für Computer Zertifikat
description: Beispiel für Computer Zertifikat
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Media-Format-SDK, Computer Zertifikate
- Windows Media-Format-SDK, Zertifikate
- Windows Media-Format-SDK, Beispielcode
- Windows Media-Format-SDK, Codebeispiele
- Digital Rights Management (DRM), Computer Zertifikate
- DRM (Digital Rights Management), Computer Zertifikate
- Digital Rights Management (DRM), Zertifikate
- DRM (Digital Rights Management), Zertifikate
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Erweiterte APIs für den DRM-Client, Computer Zertifikate
- Erweiterte Client-APIs, Computer Zertifikate
- Erweiterte APIs für den DRM-Client, Zertifikate
- Erweiterte Client-APIs, Zertifikate
- Erweiterte APIs für den DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- Erweiterte APIs für den DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
- Zertifikate, Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388622"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="fd6d7-124">Beispiel für Computer Zertifikat</span><span class="sxs-lookup"><span data-stu-id="fd6d7-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="fd6d7-125">Das folgende Beispiel zeigt, wie Sie die Computer Zertifikat Sammlung abrufen:</span><span class="sxs-lookup"><span data-stu-id="fd6d7-125">The following example shows how to retrieve the machine certificate collection:</span></span>


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fd6d7-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd6d7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd6d7-127">**DRM-Import Beispiele**</span><span class="sxs-lookup"><span data-stu-id="fd6d7-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




