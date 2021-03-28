---
title: Register-gs_5_0
description: Die folgenden Eingabe-und Ausgabe Register werden in der Geometry-Shader-Version 5 \_ 0 implementiert.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282b32dd1c8fcb327c273b0fbf3aa51bdb002c2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311047"
---
# <a name="registers---gs_5_0"></a>Register-GS \_ 5 \_ 0

Die folgenden Eingabe-und Ausgabe Register werden in der Geometry-Shader-Version 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                     | Anzahl              | R/W | Dimension         | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W | 4                 | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe (v- \[ Vertex- \] \[ Element \] )             | 32                 | R   | 4 (Comp) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe primitive-ID (vprim)                 | 1                  | R   | 1                 | Nein               | Keine     | Ja          |
| 32-Bit-Eingabe Instanz-ID (vinstanceid)            | 1                  | R   | 1                 | Nein               | Keine     | Ja          |
| -Element in einer Eingabe Ressource (t \# )                | 128                | R   | 1                 | Nein               | Keine     | Ja          |
| Sampler (e \# )                                     | 16                 | R   | 1                 | Nein               | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )          | 15                 | R   | 4                 | Ja (Inhalt)    | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] ) | 1                  | R   | 4                 | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                                               | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Ergebnis verwerfen, nützlich für OPS mit mehreren Ergebnissen) | –   | W   | –       | –              | –      | Nein           |
| 32-Bit-Ausgabe-Vertex-Daten Element (o \# )                     | 32    | W   | –       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




