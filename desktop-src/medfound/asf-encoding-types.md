---
description: ASF-Codierungs Typen
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: ASF-Codierungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128008"
---
# <a name="asf-encoding-types"></a>ASF-Codierungs Typen

Die Codierungs Methoden konzentrieren sich alle auf den Puffer, der vom Encoder zum Verwalten nicht komprimierter Eingabedaten verwendet wird. Dieser Puffer wird durch die Bitrate des Streams in Bits pro Sekunde und das Puffer Fenster in Millisekunden definiert. Beim Codieren in ASF-Dateien halten die Windows Media Encoder die Einschränkungen des Puffers an. Weitere Informationen zum Puffer Fenster finden Sie unter unkomplizierter [Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md). Wenn Sie wissen, wie und wann die einzelnen Methoden verwendet werden sollen, können Sie hochwertige komprimierte Inhalte erstellen. Die folgende Tabelle enthält Links zu Themen zu den einzelnen verfügbaren Codierungs Methoden, die eine Anwendung verwenden kann, um Mediendaten in ASF zu codieren.



| Codiermethode                                                                                      | BESCHREIBUNG                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)                                         | Der Encoder komprimiert Daten auf eine angegebene Bitrate.                                                                                                                                                     |
| [Qualitäts basierte Variable Bitrate Codierung](quality-based-variable-bit-rate--vbr--encoding.md)       | Der Encoder komprimiert Daten auf einen bestimmten Qualitäts Wert, sodass die Qualität der codierten Medien während der gesamten Dauer konsistent ist, unabhängig von den Puffer Anforderungen des resultierenden Streams. |
| [Unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)       | Der Encoder komprimiert Daten auf die höchste mögliche Qualität, während eine angegebene Bitrate beibehalten wird. Dieser Modus wird auch als 2-Pass-VBR-Codierung (Variable Bitrate) bezeichnet.                                    |
| [Mit Spitzenwerten beschränkte Variable Bitrate-Codierung](peak-constrained-variable-bit-rate--vbr--encoding.md) | Der Encoder komprimiert Daten auf eine angegebene Bitrate und behält dabei die Puffer Werte unter dem angegebenen maximalen Puffer Fenster und der angegebenen Bitrate bei. Dieser Modus wird auch als 2-Durchlauf-Spitzenwert für VBR bezeichnet.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



