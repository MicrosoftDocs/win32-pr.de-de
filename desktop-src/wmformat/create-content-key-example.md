---
title: Beispiel zum Erstellen eines Inhaltsschlüssels
description: Beispiel zum Erstellen eines Inhaltsschlüssels
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- Windows Medienformat-SDK, Inhaltsschlüssel
- Windows Medienformat-SDK, Beispielcode
- Windows Medienformat-SDK, Codebeispiele
- Digital Rights Management (DRM), Inhaltsschlüssel
- DRM (Digital Rights Management), Inhaltsschlüssel
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- ERWEITERTE APIs für DEN DRM-Client, Inhaltsschlüssel
- Erweiterte Client-APIs, Inhaltsschlüssel
- ERWEITERTE APIs für DEN DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- ERWEITERTE APIs für DEN DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
- Inhaltsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c63f55cd825de197ea7e13d9215971e1d3153aabb23ee41924a65f91849c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931480"
---
# <a name="create-content-key-example"></a>Beispiel zum Erstellen eines Inhaltsschlüssels

Der Inhaltsschlüssel wird zum Verschlüsseln von Medienbeispielen für Windows Media DRM Import verwendet. Im folgenden Codebeispiel wird veranschaulicht, wie eine Inhaltsschlüsselstruktur erstellt und initialisiert wird.


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BEISPIELE FÜR DRM-Importe**](drm-import-examples.md)
</dt> </dl>

 

 




