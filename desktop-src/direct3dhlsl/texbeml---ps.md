---
title: texbeml-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation mit Beleuchtungs Korrektur. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV), einer 2D-Stoß Umgebungs Matrix und einer Leuchtkraft geändert werden.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949066"
---
# <a name="texbeml---ps"></a>texbeml-PS

Anwenden einer gefälschten Bump Environment-Map-Transformation mit Beleuchtungs Korrektur. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV), einer 2D-Stoß Umgebungs Matrix und einer Leuchtkraft geändert werden.

## <a name="syntax"></a>Syntax



| texbeml DST, src |
|------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Die roten und grünen Farbdaten im src-Register werden als Perturbation-Daten (du, DV) interpretiert. Die blauen Farbdaten im src-Register werden als Beleuchtungs Daten interpretiert.

Diese Anweisung transformiert die roten und grünen Komponenten im Quell Register mithilfe der 2D-Bump-Umgebungs mappingmatrix. Das Ergebnis wird dem Texturkoordinaten Satz hinzugefügt, der der Ziel Registernummer entspricht. Eine Leuchtkraft Korrektur wird mithilfe des Leuchtkraft Werts und der Bias-Textur Stufen Werte angewendet. Das Ergebnis wird verwendet, um eine Stichprobe der aktuellen Textur Phase durchzuführen.

Dies kann für eine Vielzahl von Techniken verwendet werden, die auf der Adress Erfassung basieren, wie z. b. eine gefälschte Umgebungs Zuordnung pro Pixel.

Mit diesem Vorgang werden du und DV immer als signierte Mengen interpretiert. Für die Versionen 1 \_ 0 und 1 \_ 1 ist der Eingabe Modifizierer für die [Quell Registrierung mit signierter Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) für das Eingabe Argument nicht zulässig.

Diese Anweisung erzeugt definierte Ergebnisse, wenn Eingabe Texturen gemischte Formatierungsdaten enthalten. Weitere Informationen zu Oberflächen Formaten finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



In diesem Beispiel werden die in der-Anweisung durchgeführten Berechnungen veranschaulicht.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u ' = TextureCoordinates (Stufe m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (Stufe m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (Stufe m) \* t (n)<sub>G</sub>

v ' = TextureCoordinates (Stufe m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (Stufe m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (Stufe m) \* t (n)<sub>G</sub>

t (m)<sub>RGBA</sub> = texturesample (Stufe m) mit (u ', v ') als Koordinaten

t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*

\[(t (n)<sub>B</sub> \* D3DTSS \_ bumpenvlscale (Stufe m) +

D3DTSS \_ bumpenvloffset (Stufe m)\]

Das Registrieren von Daten, die von einer [texbem](texbem---ps.md) -oder texbeml-Anweisung gelesen wurden, kann später nicht mehr gelesen werden, mit Ausnahme von anderen texbem oder texbeml.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
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
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Für dieses Beispiel sind die folgenden Texturen in den folgenden Textur Phasen erforderlich.

-   Phase 0 wird eine Bump Map mit (du-, DV-) perturingdaten zugewiesen.
-   Phase 1 wird eine Textur Zuordnung mit Farbdaten zugewiesen.
-   texbeml legt die Matrix Daten auf der Textur Stufe fest, für die ein Sampling durchgeführt wird. Dies unterscheidet sich von der Funktionalität der Fixed-Funktions Pipeline, bei der die Leistungsdaten und Matrizen dieselbe Textur Phase belegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 