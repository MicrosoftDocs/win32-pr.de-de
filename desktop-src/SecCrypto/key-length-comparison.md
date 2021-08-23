---
description: Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit einer größeren Sicherheit als derzeit mit dem Microsoft Base Cryptographic Provider verfügbar. Eine höhere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Schlüssellängenvergleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65615f6ffb9679b922600c4617e401067d565ac7dd62a258ae07a757d2cec7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622345"
---
# <a name="key-length-comparison"></a>Schlüssellängenvergleich

Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit einer größeren Sicherheit als derzeit mit dem Microsoft Base Cryptographic Provider verfügbar. Eine höhere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.

In der folgenden Tabelle sind die [*Standardschlüssellängen*](../secgloss/k-gly.md) aufgeführt, die vom Basisanbieter und vom erweiterten Anbieter für Standardalgorithmen unterstützt werden.



| Algorithmus                                                                                | Basisanbieter | Starke und erweiterte Anbieter |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| RSA-Exchange                                                                         | 512-Bit       | 1.024 Bit                     |
| RSA-Signatur                                                                            | 512-Bit       | 1.024 Bit                     |
| RC2                                                                                      | 40-Bit        | 128 Bit                       |
| RC4                                                                                      | 40-Bit        | 128 Bit                       |
| DES                                                                                      | Nicht unterstützt | 56-Bit                        |
| [*Triple DES*](../secgloss/t-gly.md) (2-Key) | Nicht unterstützt | 112-Bit                       |
| Triple DES (3-Key)                                                                       | Nicht unterstützt | 168-Bit                       |



 

[*DES-*](../secgloss/d-gly.md) [*und Triple DES-Algorithmen*](../secgloss/t-gly.md) werden im erweiterten Anbieter unterstützt.

Der erweiterte Anbieter ist abwärtskompatibel mit dem Basisanbieter, der mit früheren Versionen von CryptoAPI verteilt wurde, mit der folgenden Ausnahme. Sowohl der Basisanbieter als auch der erweiterte Anbieter können nur Sitzungsschlüssel der Standardschlüssellänge generieren. Die Standardlänge von Sitzungsschlüsseln für den Basisanbieter beträgt 40 Bits. Die Standardschlüssellänge für den erweiterten Anbieter beträgt 128 Bits. Der erweiterte Anbieter kann keine Schlüssel mit basisanbieterkompatiblen Schlüssellängen erstellen. Der erweiterte Anbieter kann jedoch Schlüssellängen beliebiger Größe (bis zu 128 Bits) importieren.

 

 
