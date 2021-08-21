---
title: setp_comp ps
description: Legen Sie das Prädikatregister fest. | setp_comp ps
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d278a6104a6c47d84623b185f78b921d61899f296eeaa557a6c6c6d5344097b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119487080"
---
# <a name="setp_comp---ps"></a>setp \_ comp - ps

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

    

     

-   dst ist das [Prädikatregister](dx9-graphics-reference-asm-ps-registers-predicate.md) p0.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| setp \_ comp            |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Speichern Sie für jeden Kanal, der gemäß der Zielschreibmaske geschrieben werden kann, das boolesche Ergebnis des Vergleichsvorgangs zwischen den entsprechenden Kanälen von src0 und src1 (nachdem die Swizzles des Quellmodifizierers aufgelöst wurden).

Quellregister ermöglichen das Angeben beliebiger Komponentenwischen.

Das Zielregister lässt beliebige Schreibmasken zu.

Das dst-Register muss das Prädikatregister sein.

## <a name="applying-the-predicate-register"></a>Anwenden des Prädikatregisters

Nachdem das Prädikatregister mit setp comp initialisiert \_ wurde, kann es verwendet werden, um eine Anweisung pro Komponente zu steuern. Dies ist die Syntax:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Hierbei gilt:

-   \[!\] ist ein optionaler boolescher NOT-Wert.
-   p0 ist das Prädikatregister.
-   \[.swizzle \] ist eine optionale Swizzle, die auf den Inhalt des Prädikatregisters angewendet werden soll, bevor sie zum Maskieren der Anweisung verwendet wird. Die verfügbaren Swizzles sind: .xyzw (Standard, wenn keiner angegeben ist) oder eine beliebige Replizieren-Swizzle: .x/.r, .y/.g, .z/.b oder .a/.w.
-   -Anweisung ist eine beliebige arithmetische Anweisung oder Texturanweisung. Dies kann keine statische oder dynamische Flusssteuerungsanweisung sein.
-   dest, src0, ... sind die register, die für die Anweisung erforderlich sind.

Wenn das Prädikatregister mit Komponentenwerten (true, true, false, false) eingerichtet wurde, kann es auf diese Anweisung angewendet werden:


```
(p0) add r1, r2, r3
```



, um eine 2-Komponenten-Add-Datei auszuführen.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Die Komponenten z und w von r1 werden nicht geschrieben, da das Prädikatregister in den Komponenten z und w false enthielt.

Durch Anwenden des Prädikatregisters auf eine arithmetische oder Texturanweisung wird die Anzahl der Anweisungsslots um 1 erhöht.

Das Prädikatregister kann auch auf angewendet [werden, wenn pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) und [breakp - ps](break-p---ps.md) instructions. Diese Anweisungen zur Flusssteuerung weisen bei Verwendung des Prädikatregisters keine Erhöhung der Anzahl der Anweisungsslots auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




