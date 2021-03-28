---
title: Schleifen-vs
description: Schleife starten... ENDLOOP-Block.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993110"
---
# <a name="loop---vs"></a>Schleifen-vs

Schleife starten... [ENDLOOP](endloop---vs.md) -Block.

## <a name="syntax"></a>Syntax



| Schleife Al, i\# |
|--------------|



 

Hierbei gilt:

-   Al ist das [Schleifen Zähler Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) , das die aktuelle Schleifen Anzahl enthält.
-   Ich bin \# ein [konstantes ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md). Siehe Bemerkungen.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   Das [Schleifen Zähler Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) enthält die aktuelle Schleifen Anzahl und kann für die relative Adressierung in [Konstanten integerregister](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) oder [Ausgabe Registern](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) im Schleifen Block verwendet werden.
-   i \# . x gibt die Iterations Anzahl an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .
-   i \# . y gibt den Anfangswert des Register für das [Schleifen Leistungs Zähl Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. y nicht Inkrement oder Dekrement erhöht \# .
-   i \# . z gibt die Schritt-/Schritt-Größe an. Der zulässige Bereich ist \[ -128, 127 \] .
-   i \# . w wird nicht verwendet und muss auf 0 festgelegt werden.
-   Schleifen Blöcke können eingebettet werden. Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Beim Einfügen bezieht sich der Wert des [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) auf den unmittelbar einschließenden Schleifen Block.
-   Schleifen Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen. Es sind keine überspannen zulässig.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




