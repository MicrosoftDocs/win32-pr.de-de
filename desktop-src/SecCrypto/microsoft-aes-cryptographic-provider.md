---
description: Der Microsoft Enhanced RSA- und AES-Kryptografieanbieter unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Microsoft AES-Kryptografieanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581868"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Microsoft AES-Kryptografieanbieter

Der Microsoft Enhanced RSA- und AES-Kryptografieanbieter unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird. Der AES-Anbieter unterstützt höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

**Windows XP:** Der Microsoft AES-Kryptografieanbieter wurde als Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) bezeichnet.

Zur Aufrechterhaltung der Abwärtskompatibilität mit früheren Anbieterversionen behält der Anbietername, wie in der Wincrypt.h-Headerdatei definiert, die Bezeichnung Version 1.0 bei, obwohl neuere Versionen dieses Anbieters ausgeliefert wurden. Um die Version des zu verwendenden Anbieters zu bestimmen, rufen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, und legen Sie dabei den *parameter dwParam* auf PP \_ VERSION fest. Version 2.0 wird verwendet, wenn 0x0200 zurückgegeben wird.

|                   | Wert                    |
|-------------------|--------------------------|
| **Anbietertyp** | PROV \_ RSA \_ AES           |
| **Anbietername** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basisanbieter, dem starken Anbieter und dem AES-Anbieter aufgeführt. Die [*angezeigten Schlüssellängen*](../secgloss/k-gly.md) sind die Standardschlüssellängen.



| Algorithmus                                                                                | Schlüssellänge des Basisanbieters | Schlüssellänge des starken Anbieters | Schlüssellänge des AES-Anbieters                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Signaturalgorithmus für den öffentlichen RSA-Schlüssel                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den Austausch öffentlicher Schlüssel                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Blockverschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | Eine Salt-Länge von 128 Bits kann festgelegt werden.<br/> |
| RC4-Streamverschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | Eine Salt-Länge von 128 Bits kann festgelegt werden.<br/> |
| DES                                                                                      | 56 Bit                  | 56 Bit                    | 56 Bit                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 Key) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple DES (3 Key)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Eine vollständige Liste der unterstützten Algorithmen finden Sie unter [AES-Anbieteralgorithmen](aes-provider-algorithms.md).

Der starke Anbieter, der erweiterte Anbieter und der AES-Anbieter sind abwärtskompatibel mit dem Basisanbieter, mit der Ausnahme, dass die Anbieter nur RC2- oder RC4-Schlüssel der Standardschlüssellänge generieren können. Die Standardlänge für den Basisanbieter beträgt 40 Bits. Die Standardlänge für den AES-Anbieter beträgt 128 Bits. Daher kann der AES-Anbieter keine Schlüssel mit basisanbieterkompatiblen Schlüssellängen erstellen. Der AES-Anbieter kann jedoch RC2- und RC4-Schlüssel mit bis zu 128 Bits importieren. Daher kann der AES-Anbieter 40-Bit-Schlüssel importieren und verwenden, die mit dem Basisanbieter generiert wurden.

 

 
