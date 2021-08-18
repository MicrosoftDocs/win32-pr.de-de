---
title: Beispiel zum Erhalten eines Computerzertifikats
description: Beispiel zum Erhalten eines Computerzertifikats
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Medienformat-SDK, Computerzertifikate
- Windows Medienformat-SDK, Zertifikate
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, Codebeispiele
- Digital Rights Management (DRM), Computerzertifikate
- DRM (Digital Rights Management), Computerzertifikate
- Digital Rights Management (DRM), Zertifikate
- DRM (Digital Rights Management), Zertifikate
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- ERWEITERTE APIs für DEN DRM-Client, Computerzertifikate
- Erweiterte Client-APIs, Computerzertifikate
- Erweiterte DRM-Client-APIs, Zertifikate
- Erweiterte Client-APIs, Zertifikate
- ERWEITERTE APIs für DEN DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- ERWEITERTE APIs für DEN DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
- Zertifikate,Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964009"
---
# <a name="get-machine-certificate-example"></a>Beispiel zum Erhalten eines Computerzertifikats

Das folgende Beispiel zeigt, wie die Computerzertifikatsammlung abgerufen wird:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BEISPIELE FÜR DRM-Importe**](drm-import-examples.md)
</dt> </dl>

 

 




