---
title: Eingabe Farb Register
description: Ein Pixel-Shader-Eingabe Register, das Vertexfarbe enthält.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388793"
---
# <a name="input-color-register"></a>Eingabe Farb Register

Ein Pixel-Shader-Eingabe Register, das Vertexfarbe enthält.

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



Dabei gilt:

-   [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) ist eine Register Deklarations Anweisung.
-   v ist ein Eingabe Register und \# ist die Registernummer. Die Anzahl der zulässigen Register wird durch die Shader-Version bestimmt.
-   der Schreibzugriff bestimmt, welche Komponenten (bis zu vier) geschrieben wurden. Gültige Komponenten sind: (x, y, z, w) oder (r, g, b, a).

## <a name="remarks"></a>Bemerkungen

Farbregister sind schreibgeschützte Register. Jedes Register enthält aus Eingabe Scheitel Punkten durch Iterierte RGBA-Werte mit vier Komponenten. Sie haben niedrigere Genauigkeit als die meisten Register, und es sind garantiert 8 Bits unsignierter Daten im Bereich (0, + 1) vorhanden. Sie können nicht mehr als eine Anweisung in einer einzigen Anweisung verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[PS \_ 2 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[PS \_ 2 \_ x-Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[PS \_ 3 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




