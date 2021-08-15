---
title: Beispiel zum Erstellen eines Sitzungsschlüssels
description: Beispiel zum Erstellen eines Sitzungsschlüssels
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Medienformat-SDK, Sitzungsschlüssel
- Windows Medienformat-SDK, Inhaltsschlüssel
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, Codebeispiele
- Digital Rights Management (DRM), Sitzungsschlüssel
- DRM (Digital Rights Management), Sitzungsschlüssel
- Digital Rights Management (DRM), Inhaltsschlüssel
- DRM (Digital Rights Management), Inhaltsschlüssel
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- ERWEITERTE APIs des DRM-Clients, Sitzungsschlüssel
- Erweiterte Client-APIs, Sitzungsschlüssel
- ERWEITERTE APIs für DEN DRM-Client, Inhaltsschlüssel
- Erweiterte Client-APIs, Inhaltsschlüssel
- ERWEITERTE APIs für DEN DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- ERWEITERTE APIs für DEN DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
- Sitzungsschlüssel
- Inhaltsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef4a9c673b0aef24e010bff0f9a84beaf6321a81fe4ac8a8a9935c126983eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964139"
---
# <a name="create-session-key-example"></a>Beispiel zum Erstellen eines Sitzungsschlüssels

Der Sitzungsschlüssel wird verwendet, um den Inhaltsschlüssel zu schützen. Der folgende Code veranschaulicht das Erstellen eines Sitzungsschlüssels, lässt aber die Details der Zufälligschlüsselgenerierung aus.


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BEISPIELE FÜR DRM-Importe**](drm-import-examples.md)
</dt> </dl>

 

 




