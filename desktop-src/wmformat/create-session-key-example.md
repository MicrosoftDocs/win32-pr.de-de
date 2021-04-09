---
title: Beispiel für das Erstellen eines Sitzungsschlüssels
description: Beispiel für das Erstellen eines Sitzungsschlüssels
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Media-Format-SDK, Sitzungsschlüssel
- Windows Media-Format-SDK, Inhalts Schlüssel
- Windows Media-Format-SDK, Beispielcode
- Windows Media-Format-SDK, Codebeispiele
- Digital Rights Management (DRM), Sitzungsschlüssel
- DRM (Digital Rights Management), Sitzungsschlüssel
- Digital Rights Management (DRM), Inhalts Schlüssel
- DRM (Digital Rights Management), Inhalts Schlüssel
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Erweiterte APIs für den DRM-Client, Sitzungsschlüssel
- Erweiterte Client-APIs, Sitzungsschlüssel
- Erweiterte APIs für den DRM-Client, Inhalts Schlüssel
- Erweiterte Client-APIs, Inhalts Schlüssel
- Erweiterte APIs für den DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- Erweiterte APIs für den DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
- Sitzungsschlüssel
- Inhalts Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037583"
---
# <a name="create-session-key-example"></a><span data-ttu-id="d24d9-125">Beispiel für das Erstellen eines Sitzungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="d24d9-125">Create Session Key Example</span></span>

<span data-ttu-id="d24d9-126">Der Sitzungsschlüssel wird verwendet, um den Inhalts Schlüssel zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d24d9-126">The session key is used to protect the content key.</span></span> <span data-ttu-id="d24d9-127">Der folgende Code veranschaulicht, wie ein Sitzungsschlüssel erstellt wird, aber die Details der Zufallsschlüssel Generierung weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="d24d9-127">The following code demonstrates how to create a session key, but leaves out the details of random key generation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d24d9-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d24d9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24d9-129">**DRM-Import Beispiele**</span><span class="sxs-lookup"><span data-stu-id="d24d9-129">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




