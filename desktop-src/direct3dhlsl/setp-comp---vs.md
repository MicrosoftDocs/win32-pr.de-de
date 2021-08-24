---
title: setp_comp – vs
description: Legen Sie das Prädikatregister fest. | setp_comp – vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 892acf44000e178e7ed6774a3841760db32e3ced4d8348a7f9e9c22969bf9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671770"
---
# <a name="setp_comp---vs"></a>setp \_ comp – vs

Legen Sie das Prädikatregister fest.

## <a name="syntax"></a>Syntax



| setp \_ comp dst, src0, src1 |
|----------------------------|



 

Hierbei gilt:

-   \_comp ist ein Kanalvergleich zwischen den beiden Quellregistern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_Gt   | Größer als          |
    | \_Lt   | Kleiner als             |
    | \_Ge   | Größer als oder gleich |
    | \_Le   | Kleiner oder gleich    |
    | \_Eq   | Gleich              |
    | \_Ne   | Ungleich          |

    

     

-   dst ist das [Prädikatregister,](dx9-graphics-reference-asm-vs-registers-predicate.md) p0.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| setp \_ comp             |      |      | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Speichern Sie für jeden Kanal, der gemäß der Ziel-Schreibmaske geschrieben werden kann, das boolesche Ergebnis des Vergleichsvorgang zwischen den entsprechenden Kanälen von src0 und src1 (nachdem die Quellmodifizierer swizzles aufgelöst wurden).

Quellregister ermöglichen die Angabe beliebiger Komponenten swizzles.

Das Zielregister lässt beliebige Schreibmasken zu.

Das dest-Register muss das Prädikatregister sein.

## <a name="applying-the-predicate-register"></a>Anwenden des Prädikatregisters

Sobald das Prädikatregister mit setp initialisiert wurde, kann es verwendet werden, um eine Anweisung pro Komponente zu steuern. Dies ist die Syntax:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Hierbei gilt:

-   \[!\] ist ein optionaler boolescher NOT-Wert.
-   p0 ist das Prädikatregister.
-   \[.swizzle ist ein optionaler Swizzle, der auf den Inhalt des Prädikatregisters angewendet werden kann, bevor er zum \] Maskieren der Anweisung verwendet wird. Die verfügbaren Swizzles sind: .xyzw (Standard, wenn kein Wert angegeben ist) oder ein beliebiges Replizieren von Swizzle: .x/.r, .y/.g, .z/.b oder .a/.w.
-   -Anweisung ist eine beliebige aritmetic- oder texture-Anweisung. Dies darf keine statische oder dynamische Flusssteuerungsanweisung sein.
-   dest, srcReg, ... sind die registers, die für die Anweisung erforderlich sind.

Wenn das Prädikatregister mit Komponentenwerten (true, true, false, false) eingerichtet wurde, kann es auf diese Anweisung angewendet werden:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



, um ein 2-Komponenten-Add-Element durchzuführen.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



Die x- und y-Komponenten von r2 werden nicht geschrieben, da das Prädikatregister false in den Komponenten z und w enthielt.

Durch anwenden des Prädikatregisters auf eine arithmetische oder Texturanweisung erhöht sich die Anzahl der Anweisungsslots um 1.

Das Prädikatregister kann auch auf angewendet werden, wenn [pred – vs](if-pred---vs.md), [callnz pred – vs](callnz-pred---vs.md) und [breakp – vs](breakp---vs.md) instructions. Bei Verwendung des Prädikatregisters haben diese Anweisungsanweisungen für die Flusssteuerung keine Erhöhung der Anzahl von Anweisungsslots.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




