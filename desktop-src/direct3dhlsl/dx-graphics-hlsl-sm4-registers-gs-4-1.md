---
title: Register – gs_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von den Geometry-Shaderversionen 4 \_ 0 und 4 1 implementiert \_ werden.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 262f86490e95684f0db8ce972f8fc93528cb33ed26b09989399c15ccab766205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119944"
---
# <a name="registers---gs_4_1"></a>Register – gs \_ 4 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von den Geometry-Shaderversionen 4 \_ 0 und 4 1 implementiert \_ werden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren                 | Name | Anzahl              | R/W | Dimension        | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096(r \# +x \# \[ n \] ) | R/W | 4                | Nein               | Keine     | Ja          |
| x \# \[ n\]                 |      | 4096(r \# +x \# \[ n \] ) | R/W | 4                | Ja              | Keine     | Ja          |
| v \# \[ \] \[ vertex-Element\] |      | 32                 | R   | 4(comp) \* 6(vert) | Ja              | Keine     | Ja          |
| vprim                    |      | 1                  | R   | 1                | Nein               | Keine     | Ja          |
| t\#                      |      | 128                | R   | 1                | Nein               | Keine     | Ja          |
| s\#                      |      | 16                 | R   | 1                | Nein               | Keine     | Ja          |
| \# \[ CB-Index\]            |      | 15                 | R   | 4                | Ja(Inhalt)    | Keine     | Ja          |
| icb \[ index\]             |      | 1                  | R   | 4                | Ja(Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registrieren | Name            | Anzahl | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Verwerfen des Ergebnisses  | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| O\#      | Ausgaberegister | 32    | W   | Nicht zutreffend       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




