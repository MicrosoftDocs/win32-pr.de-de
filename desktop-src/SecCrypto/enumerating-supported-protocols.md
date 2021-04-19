---
description: Unterstützte Protokolle und Verschlüsselungs Sammlungen können mithilfe von Aufrufen von CryptGetProvParam mit PP \_ enumalgs oder PP \_ enumalgs Ex aufgelistet werden \_ .
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Auflisten unterstützter Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372989"
---
# <a name="enumerating-supported-protocols"></a>Auflisten unterstützter Protokolle

Unterstützte Protokolle und Verschlüsselungs Sammlungen können mithilfe von Aufrufen von [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit PP \_ enumalgs oder PP \_ enumalgs Ex aufgelistet werden \_ . Der Wert "PP \_ enumalgs \_ Ex" funktioniert wie PP- \_ enumalgs, gibt jedoch eine [**Prov \_ enumalgs \_ Ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) -Struktur zurück, die ausführlichere Informationen zu den vom Anbieter unterstützten Algorithmen enthält.

Weitere Informationen zu definierten protokollflags und deren Werten finden Sie unter [protokollflags](protocol-flags.md).

Da das **hcryptprov** -Element das [*handle*](../secgloss/h-gly.md) eines offenen Kryptografiekontexts ist, der mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) abgerufen wurde, dessen *dwprovtype* -Parameter auf Prov RSA SChannel festgelegt ist [](../secgloss/c-gly.md) \_ \_ , werden im folgenden Beispiel die Namen aller im CSP verfügbaren Algorithmen aufgelistet.


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



In der folgenden Tabelle werden einige Algorithmen aufgelistet, die von einem typischen in der Standard- \_ RSA \_ SChannel-CSP zurückgegebenen Algorithmus Beachten Sie, dass in diesem Beispiel weder SSL2 verwendet SHA Macs noch SSL2 verwendet der-Verschlüsselung vom CSP unterstützt wird.



| Algorithmusbezeichner                                                                        | Minimale Schlüssellänge | Maximale Schlüssellänge | Protokolle | Algorithmusname |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*calg \_ RSA \_ Keyx*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ Keyx"    |
| [*Calg \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | Benutzen          |
| [*calg \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | SHA          |
| [*Calg \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| " \_ calg"                                                                                   | 56                 | 56                 | 0x0005    | DES          |



 

Um das Senden von ClientHello-oder serverhello-Nachrichten vorzubereiten, listet die [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine die vom CSP unterstützten Algorithmen und Schlüsselgrößen auf und erstellt intern eine Liste der unterstützten Verschlüsselungs Sammlungen.

 

 
