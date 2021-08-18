---
title: Relative Adressierung (HLSL VS-Referenz)
description: Bei Vertex-Shadern kann die Syntax \\ nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 82fe97a6b78a2257208f3072d5932523d5cd04ba1d044b8a57fad5f3c212b94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744340"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Relative Adressierung (HLSL VS-Referenz)

Die \[ \] Syntax kann nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können. Die unterstützten Syntaxformen \[ \] sind wie folgt aufgeführt:

Hierbei gilt:

-   "R" gibt jeden Registertyp an, der relativ adressiert werden kann.
-   "A" gibt jedes Register an, das als Index verwendet werden kann, um relativ andere Register zu adressieren.
-   n0 - ni, m0 - mj und k sind ganze Zahlen >= 0.



| \[\]Syntax                              | Effektiver Index                       | Beispiele                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | Ein                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

Die Register sind in den folgenden Versionen verfügbar:



| Registertyp | Vertex-Shaderversionen |
|---------------|------------------------|
| a0            | Alle                    |
| Al            | Im Vergleich \_ zu \_ 2 0 und höher    |
| cn            | Im Vergleich zu \_ \_ 1 1 und höher    |
| on            | Vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




