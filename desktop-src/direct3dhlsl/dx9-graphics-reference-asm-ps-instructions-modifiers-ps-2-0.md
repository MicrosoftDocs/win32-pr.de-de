---
title: Modifizierer für ps_2_0 und höher
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer für ps_2_0 und höher.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989285"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modifizierer für ps \_ 2 \_ 0 und höher

Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird.

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungsmodifizierern, die von Version 2 0 und höher des Pixelshader implementiert \_ werden.



| Name                                     | Syntax     | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Schwerpunkt](#centroid)                    | \_Schwerpunkt | x    | x    | x     | x    | x     |
| [Partielle \_ Genauigkeit](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [Sättigen](#saturate)                    | \_sat      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Schwerpunkt

Der Schwerpunktmodifizierer ist ein optionaler Modifizierer, der die Attributinterpolation innerhalb des Bereichs des Primitiven einbindet, wenn ein Multisample-Pixelmittelpunkt nicht vom Primitiven abgedeckt wird. Dies ist unter [Schwerpunktstichproben zu](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)sehen.

Sie können den Schwerpunktmodifizierer wie hier gezeigt auf eine Assemblyanweisung anwenden:


```
dcl_texcoord0_centroid v0
```



Sie können den Schwerpunktmodifizierer auch auf eine Semantik anwenden, wie hier gezeigt:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Darüber hinaus wird für jedes [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ), das \# mit einer Farbsemantik deklariert wird, automatisch ein Schwerpunkt angewendet. Farbverläufe, die aus Attributen berechnet werden, für die Schwerpunktstichproben erstellt werden, sind nicht garantiert genau.

## <a name="partial-precision"></a>Partielle Genauigkeit

Der Anweisungsmodifizierer für partielle Genauigkeit ( \_ pp) gibt Bereiche an, in denen partielle Genauigkeit akzeptabel ist, vorausgesetzt, die zugrunde liegende Implementierung unterstützt dies. Implementierungen können den Modifizierer immer ignorieren und die betroffenen Vorgänge mit voller Genauigkeit ausführen.

Der \_ pp-Modifizierer kann in zwei Kontexten auftreten:

-   In einer Texturkoordinatendeklaration, um die Übergabe von Texturkoordinaten an den Pixelshader in Form von teilweiser Genauigkeit zu ermöglichen. Dies ermöglicht beispielsweise die Verwendung von Texturkoordinaten, um Farbdaten an den Pixelshader weiterzuleiten, was in einigen Implementierungen mit teilweiser Genauigkeit schneller als mit vollständiger Genauigkeit sein kann. Wenn dieser Modifizierer nicht vorhanden ist, müssen Texturkoordinaten mit voller Genauigkeit übergeben werden.
-   Für jede Anweisung, einschließlich Anweisungen zum Laden von Texturen. Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf. Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit voller Genauigkeit ausgeführt werden (unabhängig von der Eingabegenauigkeit).

Beispiele:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Sättigung

Der Saturate-Anweisungsmodifizierer ( \_ sat) sättigt (oder klammscht) das Anweisungsergebnis auf den Bereich \[ 0, 1, \] bevor er in das Zielregister schreibt.

Der \_ Sat-Anweisungsmodifizierer kann mit jeder Anweisung außer [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)und beliebigen Texanweisungen verwendet \* werden.

Für ps \_ 2 \_ 0, ps \_ 2 \_ x und ps \_ 2 sw kann der \_ \_ Sat-Anweisungsmodifizierer nicht mit Anweisungen verwendet werden, die in Ausgaberegister schreiben ([Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) oder [Ausgabetieferegister](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Diese Einschränkung gilt nicht für PS \_ 3 \_ 0 und höher.

Beispiel:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




