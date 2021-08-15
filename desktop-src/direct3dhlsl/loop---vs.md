---
title: loop – im Vergleich zu
description: Starten einer Schleife... endloop-Block.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a211014137f35c39a6b89cd16f0e27687b4daafd89841f752312f459531cab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986440"
---
# <a name="loop---vs"></a>loop – im Vergleich zu

Starten einer Schleife... [endloop-Block.](endloop---vs.md)

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Hierbei gilt:

-   aL ist das [Schleifenzählerregister](dx9-graphics-reference-asm-vs-registers-loop-counter.md) mit der aktuellen Schleifenanzahl.
-   i \# ist ein Constant Integer [Register.](dx9-graphics-reference-asm-vs-registers-constant-integer.md) Siehe Bemerkungen.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   Das [Schleifenzählerregister](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Loop Counter Register, aL) enthält die aktuelle Schleifenanzahl und kann für die relative Adressierung in [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c) oder Output \# Registers (o ) innerhalb des [Schleifenblocks](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) verwendet \# werden.
-   i \# .x gibt die Iterationsanzahl an. Der rechtliche Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i .x nicht erhöht oder dekrementiert. \#
-   i \# .y gibt den Anfangswert des [AL-Registers (Loop Counter Register)](dx9-graphics-reference-asm-vs-registers-loop-counter.md) an. Der rechtliche Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i .y nicht erhöht oder dekrementiert. \#
-   i \# .z gibt die Schritt-/Schrittgröße an. Der rechtliche Bereich ist \[ -128, 127 \] .
-   i \# .w wird nicht verwendet und muss auf 0 festgelegt werden.
-   Schleifenblöcke können geschachtelt sein. Weitere Informationen finden Sie [unter Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Wenn geschachtelt, bezieht sich der Wert des [Schleifenzählerregisters](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Loop Counter Register, aL) auf den unmittelbar einschließenden Schleifenblock.
-   Schleifenblöcke dürfen sich entweder vollständig in einem \* if-Block befinden oder vollständig umschließen. Es ist kein Umschließen zulässig.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




