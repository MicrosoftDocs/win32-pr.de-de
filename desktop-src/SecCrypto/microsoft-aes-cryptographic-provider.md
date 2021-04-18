---
description: Der Microsoft Enhanced RSA and AES Cryptographic Provider unterstützt dieselben Funktionen wie der Microsoft-Basis-Kryptografieanbieter, der als Basis Anbieter bezeichnet wird.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Kryptografieanbieter von Microsoft AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb4c774eb2cb9d01bcb3a12f5550537abe44b364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368110"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Kryptografieanbieter von Microsoft AES

Der Microsoft Enhanced RSA and AES Cryptographic Provider unterstützt dieselben Funktionen wie der Microsoft-Basis-Kryptografieanbieter, der als Basis Anbieter bezeichnet wird. Der AES-Anbieter unterstützt eine stärkere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

**Windows XP:** Der Kryptografieanbieter von Microsoft AES hat den Namen Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype).

Um die Abwärtskompatibilität mit früheren Anbieter Versionen aufrechtzuerhalten, behält der in der Header Datei Wincrypt. h definierte Anbieter Name die Bezeichnung der Version 1,0 bei, auch wenn neuere Versionen dieses Anbieters ausgeliefert wurden. Um die Version des verwendeten Anbieters zu ermitteln, nennen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit dem *dwparam* -Parameter, der auf die PP-Version festgelegt ist \_ . Die Version 2,0 wird verwendet, wenn "0x0200" zurückgegeben wird.

|                |                             |
|----------------|-----------------------------|
| Anbietertyp: | **Prov \_ RSA \_ AES**          |
| Anbieter Name: | **MS-Version \_ \_ RSA \_ AES \_ Prov** |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basis Anbieter, dem starken Anbieter und dem AES-Anbieter hervorgehoben. Die angezeigten [*Schlüssellängen*](../secgloss/k-gly.md) sind die Standardschlüssel Längen.



| Algorithmus                                                                                | Schlüssellänge des Basis Anbieters | Schlüssellänge des starken Anbieters | Schlüssellänge des AES-Anbieters                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| RSA-Algorithmus für die öffentliche Schlüssel Signatur                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den öffentlichen Schlüsselaustausch                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Block Verschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | 128 Bits-Salt-Länge kann festgelegt werden.<br/> |
| RC4-Stream-Verschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | 128 Bits-Salt-Länge kann festgelegt werden.<br/> |
| DES                                                                                      | 56 Bits                  | 56 Bits                    | 56 Bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2-Taste) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple des (3-Taste)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Eine umfassende Liste der unterstützten Algorithmen finden Sie unter [AES-Anbieter Algorithmen](aes-provider-algorithms.md).

Der starke Anbieter, der erweiterte Anbieter und der AES-Anbieter sind mit dem Basis Anbieter abwärts kompatibel, außer dass die Anbieter nur RC2-oder RC4-Schlüssel mit der Standard Schlüssellänge generieren können. Die Standardlänge für den Basis Anbieter beträgt 40 Bits. Die Standardlänge für den AES-Anbieter beträgt 128 Bits. Daher kann der AES-Anbieter keine Schlüssel mit Basis Anbieter kompatiblen Schlüssellängen erstellen. Der AES-Anbieter kann jedoch RC2-und RC4-Schlüssel mit bis zu 128 Bits importieren. Daher kann der AES-Anbieter 40-Bit-Schlüssel importieren und verwenden, die mithilfe des Basis Anbieters generiert wurden.

 

 
