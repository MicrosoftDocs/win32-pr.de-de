---
title: setp_comp-PS
description: Legen Sie das Prädikat Register fest. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219322"
---
# <a name="setp_comp---ps"></a>SETP \_ -Comp-PS

Legen Sie das Prädikat Register fest.

## <a name="syntax"></a>Syntax



| SETP \_ Comp DST, src0, Quelle1 |
|----------------------------|



 

Hierbei gilt:

-   \_comp ist ein pro-Kanal-Vergleich zwischen den beiden Quell Registern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_siegt   | Größer als          |
    | \_General   | Kleiner als             |
    | \_Färbung   | Größer als oder gleich |
    | \_Kirchturm   | Kleiner als oder gleich    |
    | \_stecken   | Gleich              |
    | \_NES   | Ungleich          |

    

     

-   DST ist das [Registrierungs](dx9-graphics-reference-asm-ps-registers-predicate.md) registerregister, p0.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| SETP \_ comp            |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie folgt:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Speichern Sie für jeden Kanal, der gemäß der Ziel Schreib Maske geschrieben werden kann, das boolesche Ergebnis der Vergleichsoperation zwischen den entsprechenden Kanälen von src0 und Quelle1 (nachdem die Eigenschaften des quellmodifizierers aufgelöst wurden).

Mit Quell Registern können beliebige Komponenten Streifen angegeben werden.

Das Ziel Register ermöglicht willkürliche Schreib Masken.

Das DST-Register muss das Prädikat Register sein.

## <a name="applying-the-predicate-register"></a>Anwenden des Prädikats Register

Wenn das Prädikat Register mit SETP Comp initialisiert wurde \_ , kann es verwendet werden, um eine Anweisung pro Komponente zu steuern. Hier ist die Syntax:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Hierbei gilt:

-   \[!\] ist ein optionaler boolescher Wert.
-   P0 ist das Prädikats Register
-   \[. Swizzle \] ist ein optionales Swizzle, das auf den Inhalt des Prädikats angewendet wird, bevor es zum Maskieren der Anweisung verwendet wird. Zu den verfügbaren Strichen gehören:. xyzw (Standardwert, wenn kein Wert angegeben ist) oder eine beliebige Replikation:. x/. r,. y/. g,. z/. b oder. a/. w.
-   die Anweisung ist eine beliebige aritmetic-oder Textur Anweisung. Dabei kann es sich nicht um eine statische oder dynamische Fluss Steuerungs Anweisung handeln.
-   dest, src0,... sind die von der Anweisung benötigten Register

Angenommen, das Prädikat Register wurde mit den Komponenten Werten (true, true, false, false) eingerichtet, die auf diese Anweisung angewendet werden können:


```
(p0) add r1, r2, r3
```



zum Ausführen einer 2-Komponente hinzufügen.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Die z-und w-Komponenten von R1 werden nicht geschrieben, da das Prädikat Register in den Komponenten z und w false enthielt.

Wenn Sie das Prädikat Register auf eine arithmetische oder Textur Anweisung anwenden, erhöht sich die Anzahl der Anweisungs Slots um 1.

Das Prädikat Register kann auch auf angewendet werden, [Wenn pred-PS](if-pred---ps.md), [callnz pred-PS](callnz-pred---ps.md) und [breakp-PS-](break-p---ps.md) Anweisungen. Diese Fluss Steuerungs Anweisungen weisen keine Zunahme der Anweisungs Slot-Anzahl auf, wenn das Prädikat Register verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




