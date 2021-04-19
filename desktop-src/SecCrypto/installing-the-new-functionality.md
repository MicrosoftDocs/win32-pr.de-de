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
# <a name="installing-the-new-functionality"></a><span data-ttu-id="0bc77-105">Installieren der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="0bc77-105">Installing the New Functionality</span></span>

<span data-ttu-id="0bc77-106">Durch die Installation neuer Funktionen im Arbeitsspeicher kann die Leistung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="0bc77-106">Installing new functionality into memory can improve performance.</span></span> <span data-ttu-id="0bc77-107">[*Kryptoapi*](../secgloss/c-gly.md) -Funktionen suchen den Arbeitsspeicher nach der Funktionalität, bevor Sie die Registrierung nach der dll durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="0bc77-107">[*CryptoAPI*](../secgloss/c-gly.md) functions search memory for the functionality before searching the registry for the DLL.</span></span> <span data-ttu-id="0bc77-108">Die dll muss geladen werden, bevor die-Funktionalität installiert wird.</span><span class="sxs-lookup"><span data-stu-id="0bc77-108">The DLL must be loaded before installing the functionality.</span></span>

<span data-ttu-id="0bc77-109">[**Cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installiert die Adresse der neuen Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="0bc77-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installs the address of the new functionality.</span></span> <span data-ttu-id="0bc77-110">Er sollte in der **DllMain** -Funktion der dll platziert werden.</span><span class="sxs-lookup"><span data-stu-id="0bc77-110">It should be placed in the **DllMain** function of the DLL.</span></span>

<span data-ttu-id="0bc77-111">Wenn *HMODULE* an [**cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)übermittelt wird, wird die dll nach der Installation nicht entladen, bis die Crypt32.dll entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="0bc77-111">If *hModule* is passed to [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), once installed, the DLL is not unloaded until the Crypt32.dll is unloaded.</span></span>

<span data-ttu-id="0bc77-112">Im folgenden Beispiel wird die [**cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bc77-112">The following example calls the [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) function.</span></span>


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



 

 
