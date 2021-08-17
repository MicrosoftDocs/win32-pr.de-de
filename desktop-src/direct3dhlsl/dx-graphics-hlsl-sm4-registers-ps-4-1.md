---
title: Register – ps_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Der Pixel-Shader Version 4 \_ 1 implementiert wurden.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff602f2f14292407b81dca9e19048e88db645a1b3514b4b279282436046e11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276540"
---
# <a name="registers---ps_4_1"></a>Register – ps \_ 4 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Der Pixel-Shader Version 4 \_ 1 implementiert wurden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren      | Name | Anzahl              | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| V\#           |      | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| t\#           |      | 128                | R   | 1         | Nein               | Keine     | Ja          |
| s\#           |      | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| cb \# \[ index\] |      | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| \[icb-Index\]  |      | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registrieren | Name             | Anzahl | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Verwerfen des Ergebnisses   | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| O\#      | Ausgaberegister  | 8     | W   | Nicht zutreffend       | N/V              | 4        | Nein           |
| oDepth   | Ausgabetiefe     | 1     | W   | Nicht zutreffend       | Nicht zutreffend              | 1        | Nicht zutreffend          |
| oMask    | Ausgabe der MSAA-Maske | 1     | W   | Nicht zutreffend       | Nicht zutreffend              | 1        | Nicht zutreffend          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




