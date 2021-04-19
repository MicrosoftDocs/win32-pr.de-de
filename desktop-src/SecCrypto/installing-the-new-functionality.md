---
description: Durch die Installation neuer Funktionen im Arbeitsspeicher kann die Leistung verbessert werden. Kryptoapi-Funktionen suchen den Arbeitsspeicher nach der Funktionalität, bevor Sie die Registrierung nach der dll durchsuchen. Die dll muss geladen werden, bevor die-Funktionalität installiert wird.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Installieren der neuen Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350106"
---
# <a name="installing-the-new-functionality"></a>Installieren der neuen Funktionalität

Durch die Installation neuer Funktionen im Arbeitsspeicher kann die Leistung verbessert werden. [*Kryptoapi*](../secgloss/c-gly.md) -Funktionen suchen den Arbeitsspeicher nach der Funktionalität, bevor Sie die Registrierung nach der dll durchsuchen. Die dll muss geladen werden, bevor die-Funktionalität installiert wird.

[**Cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installiert die Adresse der neuen Funktionalität. Er sollte in der **DllMain** -Funktion der dll platziert werden.

Wenn *HMODULE* an [**cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)übermittelt wird, wird die dll nach der Installation nicht entladen, bis die Crypt32.dll entladen wurde.

Im folgenden Beispiel wird die [**cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) -Funktion aufgerufen.


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



 

 
