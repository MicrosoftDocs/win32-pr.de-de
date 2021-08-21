---
description: Microsoft Enhanced RSA und AES Cryptographic Provider unterstützen die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Microsoft AES Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead697543c9846bbc47b61bd26d721811569b2bcea6584b75fad031d9451195
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683170"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Microsoft AES Cryptographic Provider

Microsoft Enhanced RSA und AES Cryptographic Provider unterstützen die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird. Der AES-Anbieter unterstützt eine höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

**Windows XP:** Der Microsoft AES-Kryptografieanbieter heißt Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype).

Um die Abwärtskompatibilität mit früheren Anbieterversionen zu gewährleisten, behält der Anbietername, wie in der Headerdatei Wincrypt.h definiert, die Bezeichnung Version 1.0 bei, obwohl neuere Versionen dieses Anbieters ausgeliefert wurden. Um die Version des verwendeten Anbieters zu bestimmen, rufen [**Sie CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, wobei der *dwParam-Parameter* auf PP VERSION festgelegt \_ ist. Version 2.0 wird verwendet, wenn 0x0200 zurückgegeben wird.

|                   | Wert                    |
|-------------------|--------------------------|
| **Anbietertyp** | PROV \_ RSA \_ AES           |
| **Anbietername** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basisanbieter, dem starken Anbieter und dem AES-Anbieter hervorgehoben. Die [*angezeigten Schlüssellängen*](../secgloss/k-gly.md) sind die Standardschlüssellängen.



| Algorithmus                                                                                | Schlüssellänge des Basisanbieters | Schlüssellänge des starken Anbieters | Schlüssellänge des AES-Anbieters                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| RSA-Algorithmus für die Signatur mit öffentlichem Schlüssel                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den Austausch öffentlicher Schlüssel                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Blockverschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | Die Salt-Länge kann auf 128 Bit festgelegt werden.<br/> |
| RC4-Datenstromverschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | Die Salt-Länge kann auf 128 Bit festgelegt werden.<br/> |
| DES                                                                                      | 56 Bits                  | 56 Bits                    | 56 Bits                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 Schlüssel) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple DES (3 Schlüssel)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Eine vollständige Liste der unterstützten Algorithmen finden Sie unter [AES-Anbieteralgorithmen.](aes-provider-algorithms.md)

Der starke Anbieter, der erweiterte Anbieter und der AES-Anbieter sind abwärtskompatibel mit dem Basisanbieter, mit der Ausnahme, dass die Anbieter nur RC2- oder RC4-Schlüssel der Standardschlüssellänge generieren können. Die Standardlänge für den Basisanbieter beträgt 40 Bits. Die Standardlänge für den AES-Anbieter beträgt 128 Bits. Daher kann der AES-Anbieter keine Schlüssel mit basisanbieterkompatiblen Schlüssellängen erstellen. Der AES-Anbieter kann jedoch RC2- und RC4-Schlüssel mit bis zu 128 Bits importieren. Daher kann der AES-Anbieter 40-Bit-Schlüssel importieren und verwenden, die mit dem Basisanbieter generiert wurden.

 

 
