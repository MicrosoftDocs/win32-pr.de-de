---
title: Register – vs_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Vertex-Shader Version 4 \_ 1 implementiert werden.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119924"
---
# <a name="registers---vs_4_1"></a>Register im Vergleich zu \_ 4 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Vertex-Shader Version 4 \_ 1 implementiert werden.

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



| Registrieren | Name            | Anzahl | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Verwerfen des Ergebnisses  | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| O\#      | Ausgaberegister | 32    | W   | Nicht zutreffend       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




