---
title: Register-ps_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 4 1 implementierten Eingabe-und Ausgabe Registern \_ .
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947714"
---
# <a name="registers---ps_4_1"></a>Register-PS \_ 4 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 4 1 implementierten Eingabe-und Ausgabe Registern \_ .

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



| Register | Name             | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ergebnis verwerfen   | –   | W   | –       | –              | –      | Nein           |
| o\#      | Ausgabe Register  | 8     | W   | –       | N/V              | 4        | Nein           |
| otiefe   | Ausgabe Tiefe     | 1     | W   | –       | –              | 1        | Nicht zutreffend          |
| omask    | Ausgabe-MSAA-Maske | 1     | W   | –       | –              | 1        | Nicht zutreffend          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




