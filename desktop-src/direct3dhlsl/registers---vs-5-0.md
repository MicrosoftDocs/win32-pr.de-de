---
title: Register-vs_5_0
description: Die folgenden Eingabe-und Ausgabe Register sind in der Vertex-Shader-Version 5 \_ 0 implementiert.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976136"
---
# <a name="registers---vs_5_0"></a>Register-vs \_ 5 \_ 0

Die folgenden Eingabe-und Ausgabe Register sind in der Vertex-Shader-Version 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                      | Anzahl              | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe (v \# )                                 | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| -Element in einer Eingabe Ressource (t \# )                 | 128                | R   | 1         | Nein               | Keine     | Ja          |
| Sampler (e \# )                                      | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )           | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| iimmediate constantbuffer-Referenz (ICB- \[ Index \] ) | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                                                      | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Ergebnis verwerfen, nützlich für Vorgänge mit mehreren Ergebnissen) | –   | W   | –       | –              | –      | Nein           |
| 32-Bit-Ausgabe-Vertex-Daten Element (o \# )                            | 32    | W   | 4         | –              | –      | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




