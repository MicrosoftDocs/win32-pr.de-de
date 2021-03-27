---
title: Modifiziererer für PS_2_0 und höher
description: Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856984"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modifiziererer für PS \_ 2 \_ 0 und höher

Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungs Modifizierern, die von Pixel Shader Version 2 \_ 0 und höher implementiert werden.



| Name                                     | Syntax     | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Schwerpunkt](#centroid)                    | \_Schwerpunkt | x    | x    | x     | x    | x     |
| [Partielle \_ Genauigkeit](#partial-precision) | \_Trupp       | x    | x    | x     | x    | x     |
| [Sättigen](#saturate)                    | \_gesetzt      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Schwerpunkt

Der Schwerpunkt-Modifizierer ist ein optionaler Modifizierer, der die Attribut interpolung innerhalb des Gültigkeits Bereichs des primitiven aufbindet, wenn ein Multisampling-Pixel Center nicht vom primitiven abgedeckt wird. Dies kann in [Centroid-Stichproben](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)angezeigt werden.

Sie können den Schwerpunkt-Modifizierer auf eine Assemblyanweisung anwenden, wie hier gezeigt:


```
dcl_texcoord0_centroid v0
```



Sie können auch den Schwerpunkt-Modifizierer auf eine Semantik anwenden, wie hier gezeigt:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Darüber hinaus wird für jedes [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v), das \# mit einer Farb Semantik deklariert wurde, der Schwerpunkt automatisch angewendet. Aus Attributen berechnete Farbverläufe, bei denen es sich um einen Schwerpunkt Wert handelt, sind nicht unbedingt genau.

## <a name="partial-precision"></a>Partielle Genauigkeit

Der Anweisungs Modifizierer partielle Genauigkeit \_ gibt Bereiche an, in denen partielle Genauigkeit zulässig ist, vorausgesetzt, dass die zugrunde liegende Implementierung dies unterstützt. Implementierungen können den-Modifizierer jederzeit ignorieren und die betroffenen Vorgänge mit vollständiger Genauigkeit ausführen.

Der \_ PP-Modifizierer kann in zwei Kontexten vorkommen:

-   In einer Texturkoordinaten Deklaration, die das Übergeben von Texturkoordinaten an den Pixelshader in Form mit teilweiser Genauigkeit ermöglicht. Dies ermöglicht z. b. die Verwendung von Texturkoordinaten, um Farbdaten an den Pixelshader zu übertragen. Dies kann bei einigen Implementierungen mit einer partiellen Genauigkeit schneller erfolgen als mit der vollständigen Genauigkeit. Wenn dieser Modifizierer nicht vorhanden ist, müssen die Texturkoordinaten vollständig übermittelt werden.
-   In jeder Anweisung einschließlich Textur Ladeanweisungen. Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein partielles Genauigkeits Ergebnis speichern darf. Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit vollständiger Genauigkeit (unabhängig von der Eingabe Genauigkeit) ausgeführt werden.

Beispiele:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Sättigung

Der Bezeichner der bearbeitungsanweisungsmodifizierer ( \_ Sat) füllt das Anweisungs Ergebnis \[ vor dem \] Schreiben in das Ziel Register (oder bindet es) bis zum Bereich 0, 1.

Der \_ Sat-Anweisungs Modifizierer kann mit einer beliebigen Anweisung außer [FRC-PS](frc---ps.md), [SinCos-PS](sincos---ps.md)und allen Textanweisungen verwendet werden \* .

Für PS \_ 2 \_ 0, PS \_ 2 \_ x und PS \_ 2 \_ SW \_ kann der Sat-Anweisungs Modifizierer nicht mit Anweisungen verwendet werden, die in Ausgabe Register geschrieben werden ([Ausgabe Farbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) oder [Ausgabe tiefen Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Diese Einschränkung gilt nicht für PS \_ 3 \_ 0 und höher.

Beispiel:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




