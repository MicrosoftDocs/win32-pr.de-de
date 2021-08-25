---
description: Unterstützte Protokolle und Verschlüsselungssammlungen können durch Aufrufe von CryptGetProvParam mit PP \_ ENUMALGS oder PP \_ ENUMALGS EX aufgelistet \_ werden.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Auflisten unterstützter Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d7236fe20901e9feb48e844deceea47e8f5936b9685580a653f1480b3b667c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874430"
---
# <a name="enumerating-supported-protocols"></a>Auflisten unterstützter Protokolle

Unterstützte Protokolle und Verschlüsselungssammlungen können durch Aufrufe von [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit PP \_ ENUMALGS oder PP \_ ENUMALGS EX aufgelistet \_ werden. Der PP \_ ENUMALGS \_ EX-Wert funktioniert wie PP \_ ENUMALGS, gibt jedoch eine [**PROV \_ ENUMALGS \_ EX-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) zurück, die umfangreichere Informationen zu den vom Anbieter unterstützten Algorithmen enthält.

Weitere Informationen zu definierten Protokollflags und ihren Werten finden Sie unter [Protokollflags.](protocol-flags.md)

Da das **hCryptProv-Element** das [*Handle*](../secgloss/h-gly.md) eines offenen kryptografischen [*Kontexts*](../secgloss/c-gly.md) ist, der mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) abgerufen wurde und dessen *dwProvType-Parameter* auf PROV RSA SCHANNEL festgelegt \_ \_ ist, werden im folgenden Beispiel die Namen aller im CSP verfügbaren Algorithmen aufgelistet.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



In der folgenden Tabelle sind einige Algorithmen aufgeführt, die von einem typischen nationalen PROV \_ RSA \_ SCHANNEL CSP zurückgegeben werden. Beachten Sie, dass weder SSL2-SHA-MACs noch SSL2-DES-Verschlüsselung vom CSP in diesem Beispiel unterstützt werden.



| Algorithmusbezeichner                                                                        | Minimale Schlüssellänge | Maximale Schlüssellänge | Protokolle | Algorithmusname |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | "MD5"          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | "SHA"          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | "RC4"          |
| CALG \_ DES                                                                                   | 56                 | 56                 | 0x0005    | "DES"          |



 

Um das Senden von ClientHello- oder [](../secgloss/s-gly.md) ServerHello-Nachrichten vorzubereiten, listet die Schannel-Protokoll-Engine die vom CSP unterstützten Algorithmen und Schlüsselgrößen auf und erstellt intern eine Liste der unterstützten Verschlüsselungssammlungen.

 

 
