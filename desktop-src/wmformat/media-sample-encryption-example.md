---
title: Beispiel für eine Beispiel Verschlüsselung für Medien
description: Beispiel für eine Beispiel Verschlüsselung für Medien
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Media-Format-SDK, Medien Beispiel Verschlüsselung
- Windows Media-Format-SDK, Beispielcode
- Windows Media-Format-SDK, Codebeispiele
- Digital Rights Management (DRM), Medien Beispiel Verschlüsselung
- DRM (Digital Rights Management), Medien Beispiel Verschlüsselung
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Erweiterte APIs für den DRM-Client, Medien Beispiel Verschlüsselung
- Erweiterte Client-APIs, Medien Beispiel Verschlüsselung
- Erweiterte APIs für den DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- Erweiterte APIs für den DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037558"
---
# <a name="media-sample-encryption-example"></a>Beispiel für eine Beispiel Verschlüsselung für Medien

Im folgenden unvollständigen Beispiel wird veranschaulicht, wie ein Medien Beispiel mithilfe der DRM-Verschlüsselung verschlüsselt wird. Der RC4-Verschlüsselungsalgorithmus wurde aufgrund von Speicherplatz Beschränkungen aus dem Beispiel ausgelassen.


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import Beispiele**](drm-import-examples.md)
</dt> </dl>

 

 




