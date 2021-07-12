---
description: Der Microsoft Enhanced Cryptographic Provider unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, aber mehr Sicherheit durch längere Schlüssel und zusätzliche Algorithmen.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Microsoft Enhanced Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf3b3b421e3151811da033e7536f334e3883487
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581828"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Microsoft Enhanced Cryptographic Provider

Der Microsoft Enhanced Cryptographic Provider, der als erweiterter Anbieter bezeichnet wird, unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird. Der erweiterte Anbieter unterstützt eine höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

Um die Abwärtskompatibilität mit früheren Anbieterversionen zu gewährleisten, behält der Anbietername, wie in der Headerdatei Wincrypt.h definiert, die Bezeichnung Version 1.0 bei. Version 2.0 dieses Anbieters wird derzeit jedoch ausgeliefert. Um die Version des verwendeten Anbieters zu bestimmen, rufen [**Sie CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, wobei das *dwParam-Argument* auf **PP \_ VERSION** festgelegt ist. Version 2.0 wird verwendet, wenn 0x0200 zurückgegeben wird.

|                   | Wert               |
|-------------------|---------------------|
| **Anbietertyp** | PROV \_ RSA \_ FULL     |
| **Anbietername** | MS \_ ENHANCED \_ PROV  |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basisanbieter, dem starken Anbieter und dem erweiterten Anbieter hervorgehoben. Die angezeigten Schlüssellängen sind die Standardschlüssellängen.



| Algorithmus                                                                                | Schlüssellänge des Basisanbieters | Schlüssellänge des starken Anbieters | Erweiterte Schlüssellänge des Anbieters                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| RSA-Algorithmus für die Signatur mit öffentlichem Schlüssel                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den Austausch öffentlicher Schlüssel                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Blockverschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | Die Salt-Länge kann auf 128 Bit festgelegt werden.<br/> |
| RC4-Datenstromverschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | Die Salt-Länge kann auf 128 Bit festgelegt werden.<br/> |
| DES                                                                                      | 56 Bits                  | 56 Bits                    | 56 Bits                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 Schlüssel) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple DES (3 Schlüssel)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Der starke Anbieter und der erweiterte Anbieter sind abwärtskompatibel mit dem Basisanbieter, außer dass die Anbieter nur RC2- oder RC4-Schlüssel der [*Standardschlüssellänge*](../secgloss/k-gly.md)generieren können. Die Standardlänge für den Basisanbieter beträgt 40 Bits. Die Standardlänge für den erweiterten Anbieter beträgt 128 Bits. Daher kann der erweiterte Anbieter keine Schlüssel mit basisanbieterkompatiblen Schlüssellängen erstellen. Der erweiterte Anbieter kann jedoch RC2- und RC4-Schlüssel mit bis zu 128 Bit importieren. Daher kann der erweiterte Anbieter 40-Bit-Schlüssel importieren und verwenden, die mit dem Basisanbieter generiert wurden.

 

 
