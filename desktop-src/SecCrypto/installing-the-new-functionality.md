---
description: Die Installation neuer Funktionen im Arbeitsspeicher kann die Leistung verbessern. CryptoAPI-Funktionen durchsuchen den Arbeitsspeicher nach der Funktionalität, bevor sie die Registrierung nach der DLL durchsuchen. Die DLL muss vor der Installation der Funktionalität geladen werden.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Installieren der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c71167f8226ad78f449b3f529e2e22bdb060bc0c5d984671cf4c5a30cc6f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005298"
---
# <a name="installing-the-new-functionality"></a>Installieren der neuen Funktionalität

Die Installation neuer Funktionen im Arbeitsspeicher kann die Leistung verbessern. [*CryptoAPI-Funktionen*](../secgloss/c-gly.md) durchsuchen den Arbeitsspeicher nach der Funktionalität, bevor sie die Registrierung nach der DLL durchsuchen. Die DLL muss vor der Installation der Funktionalität geladen werden.

[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installiert die Adresse der neuen Funktionalität. Sie sollte in der **DllMain-Funktion** der DLL platziert werden.

Wenn *hModule* an [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)übergeben wird, wird die DLL nach der Installation erst entladen, wenn Crypt32.dll entladen wird.

Im folgenden Beispiel wird die [**CryptInstallOIDFunctionAddress-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) aufruft.


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
