---
description: Der Microsoft Enhanced Cryptographic Provider unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, unterstützt jedoch höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Microsoft Enhanced Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60dbe254f9f22623a61de51b044b58df3a52f19f8a0b4f283caba3f59db7974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425510"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Microsoft Enhanced Cryptographic Provider

Der Microsoft Enhanced Cryptographic Provider, der als erweiterter Anbieter bezeichnet wird, unterstützt die gleichen Funktionen wie der Microsoft Base Cryptographic Provider, der als Basisanbieter bezeichnet wird. Der erweiterte Anbieter unterstützt höhere Sicherheit durch längere Schlüssel und zusätzliche Algorithmen. Sie kann mit allen Versionen von CryptoAPI verwendet werden.

Zur Aufrechterhaltung der Abwärtskompatibilität mit früheren Anbieterversionen behält der Anbietername, wie in der Wincrypt.h-Headerdatei definiert, die Bezeichnung Version 1.0 bei. Version 2.0 dieses Anbieters wird derzeit jedoch im Versand verfügbar sein. Um die Version des zu verwendenden Anbieters zu bestimmen, rufen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, und legen Sie dabei das *argument dwParam* auf **PP VERSION \_ fest.** Version 2.0 wird verwendet, wenn 0x0200 zurückgegeben wird.

|                   | Wert               |
|-------------------|---------------------|
| **Anbietertyp** | PROV \_ RSA \_ FULL     |
| **Anbietername** | MS \_ ENHANCED \_ PROV  |



 

In der folgenden Tabelle werden die Unterschiede zwischen dem Basisanbieter, dem starken Anbieter und dem erweiterten Anbieter aufgeführt. Die angezeigten Schlüssellängen sind die Standardschlüssellängen.



| Algorithmus                                                                                | Schlüssellänge des Basisanbieters | Schlüssellänge des starken Anbieters | Erweiterte Schlüssellänge des Anbieters                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Signaturalgorithmus für den öffentlichen RSA-Schlüssel                                                       | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RSA-Algorithmus für den Austausch öffentlicher Schlüssel                                                        | 512 Bits                 | 1.024 Bits                 | 1.024 Bits                                  |
| RC2-Blockverschlüsselungsalgorithmus                                                           | 40 Bits                  | 128 Bits                   | Eine Salt-Länge von 128 Bits kann festgelegt werden.<br/> |
| RC4-Streamverschlüsselungsalgorithmus                                                          | 40 Bits                  | 128 Bits                   | Eine Salt-Länge von 128 Bits kann festgelegt werden.<br/> |
| DES                                                                                      | 56 Bit                  | 56 Bit                    | 56 Bit                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 Key) | Nicht unterstützt            | 112 Bits                   | 112 Bits                                    |
| Triple DES (3 Schlüssel)                                                                       | Nicht unterstützt            | 168 Bits                   | 168 Bits                                    |



 

Der starke Anbieter und der erweiterte Anbieter sind abwärtskompatibel mit dem Basisanbieter, mit der Ausnahme, dass die Anbieter nur RC2- oder RC4-Schlüssel der [*Standardschlüssellänge generieren können.*](../secgloss/k-gly.md) Die Standardlänge für den Basisanbieter beträgt 40 Bits. Die Standardlänge für den erweiterten Anbieter beträgt 128 Bits. Daher kann der erweiterte Anbieter keine Schlüssel mit basisanbieterkompatiblen Schlüssellängen erstellen. Der erweiterte Anbieter kann jedoch RC2- und RC4-Schlüssel mit bis zu 128 Bits importieren. Daher kann der erweiterte Anbieter 40-Bit-Schlüssel importieren und verwenden, die mit dem Basisanbieter generiert wurden.

 

 
