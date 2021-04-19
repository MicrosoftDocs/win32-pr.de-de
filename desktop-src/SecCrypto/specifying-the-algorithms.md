---
description: Nachdem ein Hauptschlüssel erstellt oder importiert wurde, informieren sowohl RSA/SChannel als auch Diffie-Hellman/SChannel den CSP über den Typ der Massen Verschlüsselungsschlüssel und Mac-Schlüssel, die vom Hauptschlüssel abgeleitet werden.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Angeben der Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360065"
---
# <a name="specifying-the-algorithms"></a><span data-ttu-id="326c4-103">Angeben der Algorithmen</span><span class="sxs-lookup"><span data-stu-id="326c4-103">Specifying the Algorithms</span></span>

<span data-ttu-id="326c4-104">Nachdem ein [*Hauptschlüssel*](../secgloss/m-gly.md) erstellt oder importiert wurde, informieren sowohl [*RSA*](../secgloss/r-gly.md)/SChannel als auch [*Diffie-Hellman*](../secgloss/d-gly.md)/SChannel den [*CSP*](../secgloss/c-gly.md) über den Typ der [*Massen Verschlüsselungsschlüssel*](../secgloss/b-gly.md) und [*Mac-Schlüssel*](../secgloss/m-gly.md) , die vom Hauptschlüssel abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="326c4-104">After a [*master key*](../secgloss/m-gly.md) is created or imported, both [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel inform the [*CSP*](../secgloss/c-gly.md) of the type of [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) that will be derived from the master key.</span></span> <span data-ttu-id="326c4-105">Im folgenden Beispiel werden diese Algorithmen angegeben.</span><span class="sxs-lookup"><span data-stu-id="326c4-105">The following example specifies these algorithms.</span></span> <span data-ttu-id="326c4-106">Der gleiche Code wird sowohl für Client als auch für Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="326c4-106">The same code is used for both client and server.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> <span data-ttu-id="326c4-107">Eine [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine darf keine Algorithmen und Schlüsselgrößen angeben, die vom CSP nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="326c4-107">An [*Schannel*](../secgloss/s-gly.md) protocol engine must not specify algorithms and key sizes not supported by the CSP.</span></span> <span data-ttu-id="326c4-108">Weitere Informationen finden Sie [unter Auflisten unterstützter Protokolle](enumerating-supported-protocols.md).</span><span class="sxs-lookup"><span data-stu-id="326c4-108">For more information, see [Enumerating Supported Protocols](enumerating-supported-protocols.md).</span></span> <span data-ttu-id="326c4-109">Wenn nicht unterstützte Algorithmen oder Schlüsselgrößen angegeben werden, muss bei der CSP-Funktion ein Fehler auftreten und der Fehlercode für die erbende \_ Fehlermeldung zurückgegeben werden \_</span><span class="sxs-lookup"><span data-stu-id="326c4-109">If unsupported algorithms or key sizes are specified, the CSP function must fail and return the NTE\_BAD\_DATA error code.</span></span>

 

 

 
