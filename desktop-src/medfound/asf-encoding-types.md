---
description: ASF-Codierungstypen
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: ASF-Codierungstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83e1b9f39118cea5e7c5610b9480ea3d615a002d7f889933e3f3e7d62f0b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035578"
---
# <a name="asf-encoding-types"></a>ASF-Codierungstypen

Die Codierungsmethoden konzentrieren sich alle auf den Puffer, der vom Encoder zum Verwalten nicht komprimierter Eingabedaten verwendet wird. Dieser Puffer wird durch die Bitrate des Streams in Bits pro Sekunde und das Pufferfenster in Millisekunden definiert. Bei der Codierung in ASF-Dateien halten sich Windows Media Encoder an die Einschränkungen des Puffers. Weitere Informationen zum Pufferfenster finden Sie unter [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md). Wenn Sie wissen, wie und wann die einzelnen Methoden verwendet werden, können Sie hochwertige komprimierte Inhalte erstellen. Die folgende Tabelle enthält Links zu Themen zu den einzelnen verfügbaren Codierungsmethoden, die eine Anwendung zum Codieren von Mediendaten in ASF verwenden kann.



| Codiermethode                                                                                      | Beschreibung                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codierung der konstanten Bitrate](constant-bit-rate-encoding.md)                                         | Der Encoder komprimiert Daten auf eine angegebene Bitrate.                                                                                                                                                     |
| [Qualitätsbasierte Codierung mit variabler Bitrate](quality-based-variable-bit-rate--vbr--encoding.md)       | Der Encoder komprimiert Daten auf einen bestimmten Qualitätswert, sodass die Qualität der codierten Medien während der gesamten Dauer konsistent ist, unabhängig von den Pufferanforderungen des resultierenden Streams. |
| [Codierung der unkonstraineden Variablenbitrate](unconstrained-variable-bit-rate--vbr--encoding.md)       | Der Encoder komprimiert Daten in der höchstmöglichen Qualität, während eine angegebene Bitrate beibehalten wird. Dieser Modus wird auch als 2-Pass-VBR-Codierung (Variable Bit Rate) bezeichnet.                                    |
| [Codierung der variablen Bitrate mit eingeschränkter Spitzenrate](peak-constrained-variable-bit-rate--vbr--encoding.md) | Der Encoder komprimiert Daten auf eine angegebene Bitrate, während die Pufferwerte unter dem angegebenen maximalen Pufferfenster und der angegebenen Bitrate bleiben. Dieser Modus wird auch als 2-Pass-Spitzen-VBR bezeichnet.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



