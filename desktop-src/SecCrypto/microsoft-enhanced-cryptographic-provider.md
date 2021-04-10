---
description: Der Microsoft Enhanced Cryptographic Provider unterstützt die gleichen Funktionen wie der Kryptografieanbieter von Microsoft, bietet jedoch eine höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Microsoft Enhanced Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cadaa0b6325dc7d855aa0b7eeb8d7ff5f114cfd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959000"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Microsoft Enhanced Cryptographic Provider

Der von Microsoft erweiterte Kryptografieanbieter, der als erweiterter Anbieter bezeichnet wird, unterstützt dieselben Funktionen wie der Microsoft-Basis-Kryptografieanbieter, der als Basis Anbieter bezeichnet wird. Der erweiterte Anbieter unterstützt eine stärkere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

Um die Abwärtskompatibilität mit früheren Anbieter Versionen aufrechtzuerhalten, behält der Anbieter Name, wie er in der Header Datei Wincrypt. h definiert ist, die Bezeichnung Version 1,0 bei. Die Version 2,0 dieses Anbieters wird jedoch zurzeit versendet. Um die Version des verwendeten Anbieters zu ermitteln, nennen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit dem *dwparam* -Argument, das auf die **PP- \_ Version** festgelegt ist. Die Version 2,0 wird verwendet, wenn "0x0200" zurückgegeben wird.

|                |                        |
|----------------|------------------------|
| Anbietertyp: | **Prov \_ RSA \_ Full**    |
| Anbieter Name: | **MS \_ Enhanced \_ Prov** |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basis Anbieter, dem starken Anbieter und dem erweiterten Anbieter hervorgehoben. Die angezeigten Schlüssellängen sind die Standardschlüssel Längen.



| Algorithmus                                                                                | Schlüssellänge des Basis Anbieters | Schlüssellänge des starken Anbieters | Erweiterte Anbieter Schlüssellänge                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| RSA-Algorithmus für die öffentliche Schlüssel Signatur                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den öffentlichen Schlüsselaustausch                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Block Verschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | 128 Bits-Salt-Länge kann festgelegt werden.<br/> |
| RC4-Stream-Verschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | 128 Bits-Salt-Länge kann festgelegt werden.<br/> |
| DES                                                                                      | 56 Bits                  | 56 Bits                    | 56 Bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2-Taste) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple des (3-Taste)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Der starke Anbieter und der erweiterte Anbieter sind mit dem Basis Anbieter abwärts kompatibel, mit der Ausnahme, dass die Anbieter nur RC2-oder RC4-Schlüssel mit der Standard [*Schlüssellänge*](../secgloss/k-gly.md)generieren können. Die Standardlänge für den Basis Anbieter beträgt 40 Bits. Die Standardlänge für den erweiterten Anbieter beträgt 128 Bits. Daher kann der erweiterte Anbieter keine Schlüssel mit Basis Anbieter kompatiblen Schlüssellängen erstellen. Allerdings kann der erweiterte Anbieter RC2-und RC4-Schlüssel mit bis zu 128 Bits importieren. Daher kann der erweiterte Anbieter 40-Bit-Schlüssel importieren und verwenden, die mit dem Basis Anbieter generiert wurden.

 

 
