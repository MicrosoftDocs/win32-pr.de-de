---
title: texldb-PS
description: Unausgewogene Textur Lade Anweisung. Diese Anweisung verwendet das vierte Element (. a oder. w), um die Detailstufe der Textur Stichprobe direkt vor der Stichprobenentnahme zu überdenken.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101783"
---
# <a name="texldb---ps"></a>texldb-PS

Unausgewogene Textur Lade Anweisung. Diese Anweisung verwendet das vierte Element (. a oder. w), um die Detailstufe der Textur Stichprobe direkt vor der Stichprobenentnahme zu überdenken.

## <a name="syntax"></a>Syntax



| texldb DST, src0, Quelle1 |
|------------------------|



 

Hierbei gilt:

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt. Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   Quelle1 identifiziert den [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , wobei \# angibt, welche Textur samplingnummer als Stichprobe angegeben wird. Der Sampler hat ihm eine Textur und einen samplerzustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.

Informationen zu den Einschränkungen bei der Verwendung von texldb finden Sie in der [texld-PS \_ 2 \_ 0-und up-](texld---ps-2-0.md) Anweisung.

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 und PS \_ 2 \_ x

DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, und nur. xyzw Mask (Standard Maske) ist zulässig.

src0 muss entweder ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, ohne Modifizierer oder Swizzle.

Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# , ohne Modifizierer oder Swizzle.

Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), ist eine angegebene Textur Anweisung (texld, texldp, texldb, texldd) möglicherweise höchstens in dritter Reihenfolge abhängig. Eine abhängige Textur Anweisung der ersten Bestellung ist eine Textur Anweisung, in der Folgendes gilt:

-   src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   DST wurde bereits geschrieben und wird nun erneut geschrieben.

Eine abhängige Textur Anweisung in zweiter Reihenfolge wird als Textur Anweisung definiert, die ein temporäres Register (r) liest oder in ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) schreibt, \# dessen Inhalt vor dem Ausführen der Textur Anweisung (möglicherweise indirekt) auf das Ergebnis einer abhängigen Textur Anweisung der ersten Bestellung angewiesen ist. Eine (n) in der Reihenfolge abhängige Textur Anweisung wird von einer (n-1)<sup>th</sup>-<sup>Order-Textur</sup>Anweisung abgeleitet.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein. "Swizzle" ist auf Quelle1 zulässig. wenn diese Anwendung angewendet wird, werden die Ergebnisse der Textur Suche vor dem Schreiben in den DST vorgezeichnet.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb Bias die MipMap-Detailebene, die normalerweise als Teil des Beispiel Prozesses durch den (signierten) Wert in src0. w berechnet wird. Positive Bias-Werte führen dazu, dass kleinere Mipmaps ausgewählt werden und umgekehrt. Für PS \_ 2 \_ 0 und PS \_ 2 \_ x können sich die biaswerte im Bereich von \[ -3,0, + 3,0 befinden \] . Bei PS \_ 3 \_ 0 können sich die Werte für die Anzahl der Werte im Bereich von \[ -16,0, + 15,0 befinden \] . Durch biaswerte außerhalb dieser Bereiche werden nicht definierte Ergebnisse erzeugt. Der samplerstatus D3DSAMP \_ mipmaplodbias wird immer noch berücksichtigt, und der texldb-Bias wird diesem hinzugefügt, jedoch pro Pixel. Nachdem der ebenengrad ausführlich berechnet wurde, \_ wird D3DSAMP MaxMipLevel weiterhin berücksichtigt, und das Textur Beispiel wird angezeigt. Nach der texldb ist der Inhalt von src0 nicht betroffen (es sei denn, DST ist dasselbe Register).

Die Anzahl der Koordinaten, die erforderlich sind, damit src0 das Textur Beispiel durchführen kann, hängt davon ab, wie Quelle1 deklariert wurde, sowie der. w-Komponente. [ \_ Samplertypen werden mit DCL samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)deklariert. Wenn Quelle1 als 2D-Sampler deklariert ist, muss src0. xyw-Koordinaten enthalten. Wenn Quelle1 entweder als Cube-Sampler oder als volumesampler deklariert ist, muss src0. xyzw-Koordinaten enthalten. Die Stichprobenentnahme einer 2D-Textur mit xyzw-Koordinaten ist zulässig (die. z-Koordinate wird ignoriert).

Wenn die Quell Textur weniger als vier Komponenten enthält, werden die fehlenden Komponenten als Standardwerte festgelegt. Standardwerte hängen vom Textur Format ab, wie in der folgenden Tabelle gezeigt:



| Textur Format                                                                                          | Standardwerte       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = a = 1,0          |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = a = 1,0      |
| Alle tiefen/Schablonen Formate                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 