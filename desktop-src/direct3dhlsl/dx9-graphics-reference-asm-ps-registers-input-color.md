---
title: Eingabefarbregister
description: Ein Pixel-Shader-Eingaberegister, das die Scheitelpunktfarbe enthält.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744630"
---
# <a name="input-color-register"></a>Eingabefarbregister

Ein Pixel-Shader-Eingaberegister, das die Scheitelpunktfarbe enthält.

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



Dabei gilt:

-   [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) ist eine Registerdeklarationsanweisung.
-   v ist ein Eingaberegister und \# die Registernummer. Die Zulässige Anzahl von Registern wird durch die Shaderversion bestimmt.
-   writeMask bestimmt, welche Komponenten (bis zu vier) geschrieben werden. Gültige Komponenten sind: (x,y,z,w) oder (r,g,b,a).

## <a name="remarks"></a>Hinweise

Farbregister sind schreibgeschützte Register. Jedes Register enthält RGBA-Werte mit vier Komponenten, die von Eingabevertices iteriert werden. Sie haben eine geringere Genauigkeit als die meisten Register, die garantiert 8 Bits nicht signierter Daten im Bereich (0, +1) haben. Sie können nicht mehr als einen in einer einzelnen Anweisung verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




