---
title: Register-gs_4_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Geometry-Shader Version 4 0 implementiert werden \_ .
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515812"
---
# <a name="registers---gs_4_0"></a>Register-GS \_ 4 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Geometry-Shader Version 4 0 implementiert werden \_ .

## <a name="input-registers"></a>Eingabe Register



| Register                 | Name | Anzahl              | R/W | Dimension        | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| r\#                      |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4                | Nein               | Keine     | Ja          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4                | Ja              | Keine     | Ja          |
| v- \# \[ Vertex- \] \[ Element\] |      | 32                 | R   | 4 (Comp) \* 6 (Vert) | Ja              | Keine     | Ja          |
| vprim                    |      | 1                  | R   | 1                | Nein               | Keine     | Ja          |
| t\#                      |      | 128                | R   | 1                | Nein               | Keine     | Ja          |
| s\#                      |      | 16                 | R   | 1                | Nein               | Keine     | Ja          |
| CB- \# \[ Index\]            |      | 15                 | R   | 4                | Ja (Inhalt)    | Keine     | Ja          |
| ICB- \[ Index\]             |      | 1                  | R   | 4                | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Register | Name            | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ergebnis verwerfen  | –   | W   | –       | –              | –      | Nein           |
| o\#      | Ausgabe Register | 32    | W   | –       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




