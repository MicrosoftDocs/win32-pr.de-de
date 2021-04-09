---
description: Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit größerer Sicherheit als derzeit mit dem Kryptografieanbieter von Microsoft. Eine größere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Vergleich der Schlüssellänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869012"
---
# <a name="key-length-comparison"></a>Vergleich der Schlüssellänge

Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit größerer Sicherheit als derzeit mit dem Kryptografieanbieter von Microsoft. Eine größere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.

In der folgenden Tabelle werden die Standard [*Schlüssellängen*](../secgloss/k-gly.md) aufgelistet, die vom Basis Anbieter und dem erweiterten Anbieter für Standardalgorithmen unterstützt werden.



| Algorithmus                                                                                | Basis Anbieter | Starke und erweiterte Anbieter |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| RSA-Schlüsselaustausch                                                                         | 512-Bit       | 1.024-Bit                     |
| RSA-Signatur                                                                            | 512-Bit       | 1.024-Bit                     |
| RC2                                                                                      | 40-Bit        | 128 Bit                       |
| RC4                                                                                      | 40-Bit        | 128 Bit                       |
| DES                                                                                      | Nicht unterstützt | 56-Bit                        |
| [*Triple des*](../secgloss/t-gly.md) (2-Taste) | Nicht unterstützt | 112-Bit                       |
| Triple des (3-Taste)                                                                       | Nicht unterstützt | 168-Bit                       |



 

Der [*-und*](../secgloss/d-gly.md) der [*Triple des*](../secgloss/t-gly.md) -Algorithmen werden im erweiterten Anbieter unterstützt.

Der erweiterte Anbieter ist abwärts kompatibel mit dem Basis Anbieter, der mit früheren Versionen der CryptoAPI verteilt wurde, mit der folgenden Ausnahme. Sowohl der Basis Anbieter als auch der erweiterte Anbieter können nur Sitzungsschlüssel der Standard Schlüssellänge generieren. Die Standardlänge der Sitzungsschlüssel für den Basis Anbieter beträgt 40 Bits. Die Standardschlüssel Länge für den erweiterten Anbieter beträgt 128 Bits. Der erweiterte Anbieter kann keine Schlüssel mit Basis Anbieter kompatiblen Schlüssellängen erstellen. Der erweiterte Anbieter kann jedoch Schlüssellängen beliebiger Größe (bis zu 128 Bits) importieren.

 

 
