---
title: texbeml – ps
description: Wenden Sie eine falsche Umgebungszuordnungstransformation mit Leuchtdichtekorrektur an. Dies wird erreicht, indem die Texturadressendaten des Zielregisters mithilfe von Adressperturndaten (du,dv), einer 2D-Bumpumgebungsmatrix und Leuchtdichte geändert werden.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c549e93829c3165d4921342d4e74a8dc15bc1518f7c88aa205f8afc889fae95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788064"
---
# <a name="texbeml---ps"></a>texbeml – ps

Wenden Sie eine falsche Umgebungszuordnungstransformation mit Leuchtdichtekorrektur an. Dies wird erreicht, indem die Texturadressendaten des Zielregisters mithilfe von Adressperturndaten (du,dv), einer 2D-Bumpumgebungsmatrix und Leuchtdichte geändert werden.

## <a name="syntax"></a>Syntax



| texbeml dst, src |
|------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Die rot-grünen Farbdaten im src-Register werden als die Stördaten (du,dv) interpretiert. Die Blaufarbdaten im src-Register werden als Leuchtdichtedaten interpretiert.

Diese Anweisung transformiert die roten und grünen Komponenten im Quellregister mithilfe der 2D-Bump-Umgebungszuordnungsmatrix. Das Ergebnis wird dem Texturkoordinatensatz hinzugefügt, der der Zielregisternummer entspricht. Eine Leuchtdichtekorrektur wird mithilfe des Ludominanzwerts und der Werte der Biastexturphase angewendet. Das Ergebnis wird verwendet, um die aktuelle Texturphase zu beproben.

Dies kann für eine Vielzahl von Techniken verwendet werden, die auf Einer bestimmten Adresse basieren, z. B. für eine falsche Umgebungszuordnung pro Pixel.

Dieser Vorgang interpretiert du und dv immer als signierte Mengen. Für die Versionen 1 0 und 1 1 ist der Eingabemodifizierer Source \_ \_ Register Signed [Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) \_ (bx2) für das Eingabeargument nicht zulässig.

Diese Anweisung erzeugt definierte Ergebnisse, wenn Eingabetexturen Daten im gemischten Format enthalten. Weitere Informationen zu Oberflächenformaten finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



Dieses Beispiel zeigt die Berechnungen, die innerhalb der -Anweisung durchgeführt werden.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u' = TextureCoordinates(stage m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00(Stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10(Stage m) \* t(n)<sub>G</sub>

v' = TextureCoordinates(stage m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01(stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11(stage m) \* t(n)<sub>G</sub>

t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates

t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub>\*

\[(t(n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE(Stage m)) +

D3DTSS \_ BUMPENVLOFFSET(Stage m)\]

Registerdaten, die von einer [texbem-](texbem---ps.md) oder texbeml-Anweisung gelesen wurden, können nicht später gelesen werden, außer von einem anderen Texbem oder texbeml.


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

Hier ist ein Beispiel-Shader mit den identifizierten Texturzuordnungen und den identifizierten Texturstufen.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Für dieses Beispiel sind die folgenden Texturen in den folgenden Texturphasen erforderlich.

-   Phase 0 wird eine Bumpmap mit (du, dv)-Stördaten zugewiesen.
-   Phase 1 wird eine Texturkarte mit Farbdaten zugewiesen.
-   texbeml legt die Matrixdaten auf der Texturphase fest, für die stichprobenentnahmen werden. Dies ist anders als die Funktionalität der festen Funktionspipeline, bei der die Stördaten und die Matrizen dieselbe Texturphase belegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 