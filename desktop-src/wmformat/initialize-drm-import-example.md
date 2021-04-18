---
title: Initialisieren des DRM-Import Beispiels
description: Initialisieren des DRM-Import Beispiels
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Beispielcode
- Windows Media-Format-SDK, Codebeispiele
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Initialisieren des Imports
- DRM (Digital Rights Management), Initialisieren des Imports
- Digital Rights Management (DRM), Beispielcode
- DRM (Digital Rights Management), Beispielcode
- Digital Rights Management (DRM), Codebeispiele
- DRM (Digital Rights Management), Codebeispiele
- Erweiterte APIs für den DRM-Client, Initialisieren des Imports
- Erweiterte Client-APIs, Initialisieren des Imports
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Beispielcode
- Erweiterte Client-APIs, Beispielcode
- Erweiterte APIs für den DRM-Client, Codebeispiele
- Erweiterte Client-APIs, Codebeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207303"
---
# <a name="initialize-drm-import-example"></a><span data-ttu-id="09507-123">Initialisieren des DRM-Import Beispiels</span><span class="sxs-lookup"><span data-stu-id="09507-123">Initialize DRM Import Example</span></span>

<span data-ttu-id="09507-124">Im folgenden Codebeispiel wird veranschaulicht, wie ein DRM-Writer-Objekt für den DRM-Import initialisiert wird:</span><span class="sxs-lookup"><span data-stu-id="09507-124">The following code example illustrates how to initialize a DRM writer object for DRM Import:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="09507-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09507-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09507-126">**Beispiel für das Erstellen eines Inhalts Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="09507-126">**Create Content Key Example**</span></span>](create-content-key-example.md)
</dt> <dt>

[<span data-ttu-id="09507-127">**Beispiel für das Erstellen eines Sitzungsschlüssels**</span><span class="sxs-lookup"><span data-stu-id="09507-127">**Create Session Key Example**</span></span>](create-session-key-example.md)
</dt> <dt>

[<span data-ttu-id="09507-128">**DRM-Import Beispiele**</span><span class="sxs-lookup"><span data-stu-id="09507-128">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




