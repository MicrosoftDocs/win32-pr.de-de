---
description: Der Basis Anbieter hat nur 40-Bit-symmetrische Schlüssel verwendet.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Neue Funktion für die Schlüssellänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217992"
---
# <a name="new-key-length-functionality"></a><span data-ttu-id="d4fc4-103">Neue Funktion für die Schlüssellänge</span><span class="sxs-lookup"><span data-stu-id="d4fc4-103">New Key-length Functionality</span></span>

<span data-ttu-id="d4fc4-104">Der Basis Anbieter hat nur 40-Bit- [*symmetrische Schlüssel*](../secgloss/s-gly.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-104">The Base Provider used only 40-bit [*symmetric keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d4fc4-105">Das Hinzufügen von längeren Schlüsseln im erweiterten Anbieter und die Tatsache, dass importierte Schlüssel eine beliebige Länge aufweisen können, erfordert eine Methode zum Abfragen der Länge für einen bestimmten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-105">The addition of longer keys in the Enhanced Provider, and the fact that imported keys can be of arbitrary length requires a method of querying the length for a specific key.</span></span> <span data-ttu-id="d4fc4-106">Um die tatsächliche Länge eines Schlüssels in Bits zu ermitteln, kann ein Benutzer [**cryptgetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) mit dem Wert des KP \_ keylen-Parameters aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-106">To find the actual length of a key in bits, a user can call [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) with the KP\_KEYLEN parameter value.</span></span> <span data-ttu-id="d4fc4-107">Die Länge des Schlüssels wird in dem **DWORD** zurückgegeben, auf das durch den *pbData* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-107">The length of the key is returned in the **DWORD** pointed to by the *pbData* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="d4fc4-108">Zum Schutz vor der durch Prüfung von [*Cryptanalysis*](../secgloss/c-gly.md) -Angriffen müssen Anwendungen auf unzureichende [*Schlüssellängen*](../secgloss/k-gly.md) prüfen und den Benutzer benachrichtigen, wenn ein solcher auftritt.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-108">To protect against stepping-down [*cryptanalysis*](../secgloss/c-gly.md) attacks, applications must check for insufficient [*key lengths*](../secgloss/k-gly.md) and notify the user when one is encountered.</span></span>

 

<span data-ttu-id="d4fc4-109">Im folgenden Beispiel wird gezeigt, wie die Länge eines Schlüssels abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="d4fc4-109">The following example shows how to query the length of a key.</span></span>


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



 

 
