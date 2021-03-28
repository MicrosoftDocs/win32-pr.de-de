---
title: Relative Adressierung (HLSL vs-Referenz)
description: Die Syntax \ \ kann nur in Registrierungs Typen verwendet werden, die in bestimmten shadermodellen relativ adressiert werden können.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313787"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Relative Adressierung (HLSL vs-Referenz)

Die \[ \] Syntax kann nur in Registrierungs Typen verwendet werden, die in bestimmten shadermodellen relativ adressiert werden können. Die unterstützten \[ \] Syntax Formen werden wie folgt aufgelistet:

Hierbei gilt:

-   "R" bezeichnet jeden registriungstyp, der relativ adressiert werden kann.
-   "A" bezeichnet jedes Register, das als Index verwendet werden kann, um andere Register relativ zu adressieren.
-   N0-NI, M0-MJ und k sind ganze Zahlen >= 0.



| \[\]Syntax                              | Effektiver Index                       | Beispiele                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + M0 +... + MJ \]                  | A + M0 +... + MJ                     | c \[ a0. x + 3 + 7 \]              |
| R \[ k \] (= RK)                         | k                                     | c \[ 10 \] (= C10)              |
| R \[ A \]                                  | Ein                                     | c \[ a0. y \]                      |
| RK \[ N0 +... + NI + A + M0 +... + MJ \] | A + k + N0 +... + NI + M0 +... + MJ | C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ N0 +... + NI + A + M0 +... + MJ \]  | A + N0 +... + NI + M0 +... + MJ     | c \[ 2 + 1 + Al + 3 + 4 + 5 \]    |
| RK \[ A \]                                 | A + k                                 | C12 \[ Al \] , C0 \[ a0. z \]        |
| RK \[ A + M0 +... + MJ \]                 | A + k + M0 +... + MJ                 | v1 \[ Al + 4 + 8 \]               |
| R \[ N0 +... + NI + A \]                  | A + N0 +... + NI                     | o \[ 3 + 1 + Al \]                |
| RK \[ N0 +... + NI + A \]                 | A + k + N0 +... + NI                 | o1 \[ 2 + 1 + 3 + Al \]           |



 

Die Register sind in den folgenden Versionen verfügbar:



| Registriungstyp | Vertex-Shader-Versionen |
|---------------|------------------------|
| a0            | All                    |
| irdische            | vs \_ 2 \_ 0 und höher    |
| cn            | vs \_ 1 \_ 1 und höher    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




