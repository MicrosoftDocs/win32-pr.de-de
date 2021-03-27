---
title: Register-vs_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 1 implementiert werden \_ .
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206944"
---
# <a name="registers---vs_4_1"></a>Register-vs \_ 4 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 1 implementiert werden \_ .

## <a name="input-registers"></a>Eingabe Register



| Register      | Name | Anzahl              | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| Ramelow\#           |      | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| t\#           |      | 128                | R   | 1         | Nein               | Keine     | Ja          |
| s\#           |      | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| CB- \# \[ Index\] |      | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| ICB- \[ Index\]  |      | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgabe Register



| Register | Name            | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ergebnis verwerfen  | –   | W   | –       | –              | –      | Nein           |
| o\#      | Ausgabe Register | 32    | W   | –       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




