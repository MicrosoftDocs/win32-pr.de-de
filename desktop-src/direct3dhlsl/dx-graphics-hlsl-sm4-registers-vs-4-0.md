---
title: Register – vs_4_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 4 0 des Vertex-Shaders implementiert \_ werden.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfe21574bdcf6fd0c4063e59117012f1b0ef2a0ba3e2cac50ac78b28ba9d644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090687"
---
# <a name="registers---vs_4_0"></a>Register – vergleicht \_ 4 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 4 0 des Vertex-Shaders implementiert \_ werden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren      | Name | Anzahl              | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| V\#           |      | 16                 | R   | 4         | Ja              | Keine     | Ja          |
| T\#           |      | 128                | R   | 1         | Nein               | Keine     | Ja          |
| s\#           |      | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| \# \[ CB-Index\] |      | 15                 | R   | 4         | Ja(Inhalt)    | Keine     | Ja          |
| icb \[ index\]  |      | 1                  | R   | 4         | Ja(Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registrieren | Name            | Anzahl | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Verwerfen des Ergebnisses  | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| O\#      | Ausgaberegister | 16    | W   | Nicht zutreffend       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




