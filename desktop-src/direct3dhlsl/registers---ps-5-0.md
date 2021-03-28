---
title: Register-ps_5_0
description: Die folgenden Eingabe-und Ausgabe Register werden in der Pixelshader-Version 5 \_ 0 implementiert.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d945e06ed3ae1847e15a32da973709b8ceb241ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948022"
---
# <a name="registers---ps_5_0"></a>Register-PS \_ 5 \_ 0

Die folgenden Eingabe-und Ausgabe Register werden in der Pixelshader-Version 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                     | Anzahl              | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Attribut (v \# )                      | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| -Element in einer Eingabe Ressource (t \# )                | 128                | R   | 1         | Nein               | Keine     | Ja          |
| Sampler (e \# )                                     | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )          | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] ) | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                                                      | Anzahl                   | R/W | Dimension                                | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (Ergebnis verwerfen, nützlich für Vorgänge mit mehreren Ergebnissen) | –                     | W   | –                                      | –              | –      | Nein           |
| 32-Bit-Ausgabe Element (o \# )                                        | 8                       | W   | 4                                        | –              | –      | Nein           |
| Unsorderte Zugriffs Ansicht (u \# )                                        | 8- \# of-Rendertargets | R/W | D3D11 \_ PS \_ CS- \_ UAV- \_ Register \_ Komponenten | Nein               | Nein       | Ja          |
| 32-Bit \[ 0,0 f.. 1.0 f \] float-Ausgabe Tiefe (otiefe)                  | 1                       | W   | 1                                        | Nicht zutreffend              | –      | Ja          |
| 32-Bit uint Output Sample Mask (omask)                             | 1                       | W   | 1                                        | Nicht zutreffend              | –      | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




