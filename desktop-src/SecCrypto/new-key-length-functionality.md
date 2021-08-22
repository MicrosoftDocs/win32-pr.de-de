---
description: Der Basisanbieter hat nur symmetrische 40-Bit-Schlüssel verwendet.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Neue Schlüssellängenfunktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1da54be20e2b7e238cc99e787a2871bea54b40b0c46e214b7280482dcd8232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407010"
---
# <a name="new-key-length-functionality"></a>Neue Schlüssellängenfunktionalität

Der Basisanbieter hat nur [*symmetrische*](../secgloss/s-gly.md)40-Bit-Schlüssel verwendet. Das Hinzufügen längerer Schlüssel im erweiterten Anbieter und die Tatsache, dass importierte Schlüssel eine beliebige Länge haben können, erfordern eine Methode zum Abfragen der Länge für einen bestimmten Schlüssel. Um die tatsächliche Länge eines Schlüssels in Bits zu ermitteln, kann ein Benutzer [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) mit dem KP \_ KEYLEN-Parameterwert aufrufen. Die Länge des Schlüssels wird in dem **DWORD zurückgegeben,** auf das der *pbData-Parameter* zeigt.

> [!Note]  
> Zum Schutz vor schrittweisen [*Cryptanalysis-Angriffen*](../secgloss/c-gly.md) müssen Anwendungen überprüfen, ob die [*Schlüssellänge*](../secgloss/k-gly.md) nicht ausreicht, und den Benutzer benachrichtigen, wenn eine gefunden wird.

 

Das folgende Beispiel zeigt, wie die Länge eines Schlüssels abgefragt wird.


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
