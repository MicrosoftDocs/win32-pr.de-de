---
title: Register-cs_5_0
description: Die folgenden Eingabe-und Ausgabe Register werden in der COMPUTE-Shader-Version 5 \_ 0 implementiert.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9a1164a1b3b4d623ced8453bbee50f561d4666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388671"
---
# <a name="registers---cs_5_0"></a>Register-CS \_ 5 \_ 0

Die folgenden Eingabe-und Ausgabe Register werden in der COMPUTE-Shader-Version 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                        | Anzahl                                                  | R/W | Dimension                        | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                    | 4096 (r \# + x \# \[ n \] )                                     | R/W | 4                                | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )               | 4096 (r \# + x \# \[ n \] )                                     | R/W | 4                                | Ja              | Keine     | Ja          |
| 32-Bit-Thread Gruppe Shared Memory (g \# \[ n \] )         | 8192 (Summe aller freigegebenen Speicher-decls für die Thread Gruppe) | R/W | 1 (kann auf verschiedene Weise deklariert werden) | Ja              | Keine     | Ja          |
| -Element in einer Eingabe Ressource (t \# )                   | 128                                                    | R   | 1                                | Nein               | Keine     | Ja          |
| Sampler (e \# )                                        | 16                                                     | R   | 1                                | Nein               | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )             | 15                                                     | R   | 4                                | Ja (Inhalt)   | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] )    | 1                                                      | R   | 4                                | Ja (Inhalt)    | Keine     | Ja          |
| ThreadID (vThreadID.XYZ)                             | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| Threadgroupid (vThreadGroupID.XYZ)                   | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| Threadidingroup (vThreadIDInGroup.XYZ)               | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| Threadidingroupflatchten (vthreadidingroupflatchten) | 1                                                      | R   | 1                                | Nein               | –      | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                                               | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Ergebnis verwerfen, nützlich für OPS mit mehreren Ergebnissen) | –   | W   | –       | –              | –      | Nein           |
| Unsorderte Zugriffs Ansicht (u \# )                                 | 8     | R/W | 1         | Nein               | Nein       | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




