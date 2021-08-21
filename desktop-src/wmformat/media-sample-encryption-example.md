---
title: Beispiel für die Medienverschlüsselung
description: Beispiel für die Medienverschlüsselung
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Medienformat-SDK, Medienbeispielverschlüsselung
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, Codebeispiele
- Digital Rights Management (DRM), Medienbeispielverschlüsselung
- DRM (Digital Rights Management), Medienbeispielverschlüsselung
- Digital Rights Management (DRM),Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Erweiterte DRM-Client-APIs, Medienbeispielverschlüsselung
- Erweiterte Client-APIs, Medienbeispielverschlüsselung
- Erweiterte DRM-Client-APIs, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- Erweiterte DRM-Client-APIs, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccab97c5a27518d1a31c8c5cdcdbe0defe897bd2bdd47fee1c709a9192262bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846567"
---
# <a name="media-sample-encryption-example"></a>Beispiel für die Medienverschlüsselung

Im folgenden unvollständigen Beispiel wird veranschaulicht, wie ein Medienbeispiel mit drm-Verschlüsselung verschlüsselt wird. Der RC4-Verschlüsselungsalgorithmus wurde aufgrund von Speicherplatzeinschränkungen aus dem Beispiel weggelassen.


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

[**DRM-Importbeispiele**](drm-import-examples.md)
</dt> </dl>

 

 




