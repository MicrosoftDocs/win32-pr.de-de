---
title: Schleife-PS
description: Startet eine Schleife... ENDLOOP-PS-Block.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038340"
---
# <a name="loop---ps"></a>Schleife-PS

Startet eine Schleife... [ENDLOOP-PS-](endloop---ps.md) Block.

## <a name="syntax"></a>Syntax



| Schleife Al, i\# |
|--------------|



 

Hierbei gilt:

-   Al ist das [Schleifen Zähler Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) , das die aktuelle Schleifen Anzahl enthält.
-   Ich bin \# ein [konstantes ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Siehe Bemerkungen.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   Das [Schleifen Zähler Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) enthält die aktuelle Schleifen Anzahl und kann für die relative Adressierung in ein [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) im Schleifen Block verwendet werden.
-   i \# . x gibt die Iterations Anzahl an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .
-   i \# . y gibt den Anfangswert des Register für das [Schleifen Leistungs Zähl Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. y nicht Inkrement oder Dekrement erhöht \# .
-   i \# . z gibt die Schritt-/Schritt-Größe an. Der zulässige Bereich ist \[ -128, 127 \] .
-   i \# . w wird nicht vom Schleifen Block verwendet und muss 0 sein.
-   Schleifen Blöcke können eingebettet werden. Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Beim Einfügen bezieht sich der Wert des [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) auf den unmittelbar einschließenden Schleifen Block.
-   Schleifen Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen. Es sind keine überspannen zulässig.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




