---
title: Beispiel zum Initialisieren des DRM-Imports
description: Beispiel zum Initialisieren des DRM-Imports
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Media Format SDK,import
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, Codebeispiele
- Digital Rights Management (DRM), Importieren
- DRM (Digital Rights Management), Import
- Digital Rights Management (DRM), Initialisieren des Imports
- DRM (Digital Rights Management), Initialisieren des Imports
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- ERWEITERTE APIs des DRM-Clients, Initialisieren des Imports
- Erweiterte Client-APIs, Initialisieren des Imports
- ERWEITERTE APIs des DRM-Clients,Import
- Erweiterte Client-APIs,Import
- ERWEITERTE APIs für DEN DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- ERWEITERTE APIs für DEN DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e91d0aac6e9d54dac4cd52de7d84140a9e6af580084bd22ccc0af7283900d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702121"
---
# <a name="initialize-drm-import-example"></a>Beispiel zum Initialisieren des DRM-Imports

Im folgenden Codebeispiel wird veranschaulicht, wie ein DRM Writer-Objekt für DRM Import initialisiert wird:


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel zum Erstellen eines Inhaltsschlüssels**](create-content-key-example.md)
</dt> <dt>

[**Beispiel zum Erstellen eines Sitzungsschlüssels**](create-session-key-example.md)
</dt> <dt>

[**BEISPIELE FÜR DRM-Importe**](drm-import-examples.md)
</dt> </dl>

 

 




