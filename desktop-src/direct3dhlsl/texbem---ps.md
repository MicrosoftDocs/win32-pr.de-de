---
title: texbem-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV) und einer 2D-Bump-Umgebungs Matrix geändert werden.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976696"
---
# <a name="texbem---ps"></a>texbem-PS

Anwenden einer gefälschten Bump Environment-Map-Transformation. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV) und einer 2D-Bump-Umgebungs Matrix geändert werden.

## <a name="syntax"></a>Syntax



| texbem DST, src |
|-----------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

Die roten und grünen Farbdaten im src-Register werden als Perturbation-Daten (du, DV) interpretiert.

Diese Anweisung transformiert rote und grüne Komponenten im Quell Register mithilfe der 2D-Bump-Umgebungs mappingmatrix. Das Ergebnis wird dem Texturkoordinaten Satz hinzugefügt, der der Ziel Registernummer entspricht, und wird zum Beispiel für die aktuelle Textur Phase verwendet.

Mit diesem Vorgang werden du und DV immer als signierte Mengen interpretiert. Für die Versionen 1 \_ 0 und 1 \_ 1 ist der Eingabe Modifizierer für die [Quell Registrierung mit signierter Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) für das Eingabe Argument nicht zulässig.

Diese Anweisung erzeugt definierte Ergebnisse, wenn Eingabe Texturen signierte Formatierungsdaten enthalten. Daten im gemischten Format funktionieren nur, wenn die ersten beiden Kanäle signierte Daten enthalten. Weitere Informationen zu Oberflächen Formaten finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

Dies kann für eine Vielzahl von Techniken verwendet werden, die auf der Adress Umgebung basieren, einschließlich gefälschter Umgebungs Zuordnung pro Pixel und diffuses Beleuchtung (Bump-Zuordnung).

Bei der Verwendung dieser Anweisung müssen Textur Register der folgenden Sequenz folgen.


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



Die Berechnungen in der Anweisung sind unten dargestellt.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u ' = TextureCoordinates (Stufe m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (Phase m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (Phase m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (Phase m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (Stufe m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (Phase m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = texturesample (Stufe m)

Verwenden von (u ', v ') als Koordinaten

Das Registrieren von Daten, die von einer texbem-PS [-oder texbeml-PS-](texbeml---ps.md) Anweisung gelesen wurden, kann später nicht mehr gelesen werden, außer von anderen texbem-PS oder texbeml-PS.


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem erfordert die folgenden Texturen in den folgenden Textur Phasen.

-   Phase 0 wird eine Bump Map mit (du-, DV-) perturingdaten zugewiesen.
-   Phase 1 verwendet eine Textur Zuordnung mit Farbdaten.
-   Diese Anweisung legt die Matrix Daten auf der Textur Stufe fest, für die ein Sampling durchgeführt wird.
-   Dies unterscheidet sich von der Funktionalität der Fixed-Funktions Pipeline, bei der die Leistungsdaten und Matrizen dieselbe Textur Phase belegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 