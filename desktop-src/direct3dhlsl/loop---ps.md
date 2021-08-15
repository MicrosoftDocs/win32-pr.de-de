---
title: loop – ps
description: 'Startet eine Schleife... endloop : ps-Block.'
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510983"
---
# <a name="loop---ps"></a>loop – ps

Startet eine Schleife... [endloop : ps-Block.](endloop---ps.md)

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Hierbei gilt:

-   aL ist das [Schleifenzählerregister mit](dx9-graphics-reference-asm-ps-registers-loop-counter.md) der aktuellen Schleifenanzahl.
-   i \# ist ein Constant Integer [Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Siehe Bemerkungen.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   Das [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) enthält die aktuelle Schleifenanzahl und kann für die relative Adressierung im [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (v) innerhalb des Schleifenblocks verwendet \# werden.
-   i \# .x gibt die Iterationsanzahl an. Der rechtliche Bereich \[ beträgt 0, 255 \] . Beachten Sie, dass der Wert von i.x durch diese Anweisung nicht erhöht oder \# dekrementiert wird.
-   i \# .y gibt den Anfangswert des AL-Registers [(Loop Counter Register)](dx9-graphics-reference-asm-ps-registers-loop-counter.md) an. Der rechtliche Bereich \[ beträgt 0, 255 \] . Beachten Sie, dass der Wert von i.y durch diese Anweisung nicht erhöht \# oder dekrementiert wird.
-   i \# .z gibt die Schritt-/Schrittgröße an. Der rechtliche Bereich ist \[ -128, 127 \] .
-   i \# .w wird vom Schleifenblock nicht verwendet und muss 0 sein.
-   Schleifenblöcke können geschachtelt sein. Weitere Informationen [finden Flow Einschränkungen des Steuerelements](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Bei der Verschachtelung bezieht sich der Wert des [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) auf den unmittelbaren umschließenden Schleifenblock.
-   Schleifenblöcke dürfen sich entweder vollständig innerhalb eines \* if-Blocks oder vollständig um ihn herum befinden. Es ist kein Umschnallen zulässig.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




