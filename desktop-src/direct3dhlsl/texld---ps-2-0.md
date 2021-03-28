---
title: texld-PS_2_0 und aufwärts
description: Beispiel für eine Textur bei einem bestimmten Sampler mithilfe der angegebenen Texturkoordinaten. Diese Anweisung unterscheidet sich von der texld-PS \_ 1 4-Anweisung, die \_ in Pixel-Shader, Version 1 4, verwendet wird \_ .
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516886"
---
# <a name="texld---ps_2_0-and-up"></a>texld-PS \_ 2 \_ 0 und aufwärts

Beispiel für eine Textur bei einem bestimmten Sampler mithilfe der angegebenen Texturkoordinaten. Diese Anweisung unterscheidet sich von der [texld-PS \_ 1 \_ 4-](texld---ps-1-4.md) Anweisung, die in Pixel-Shader, Version 1 4, verwendet wird \_ .

## <a name="syntax"></a>Syntax



| texld DST, src0, Quelle1 |
|-----------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.
-   Quelle1 identifiziert den [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , wobei \# angibt, welche Textur samplingnummer als Stichprobe angegeben wird. Der Sampler hat ihm eine Textur und einen samplerzustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 und PS \_ 2 \_ x

DST muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, und nur. xyzw Mask (Standard Maske) ist zulässig.

src0 muss entweder ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein, ohne Modifizierer oder Swizzle.

Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) sein \# , ohne Modifizierer oder Swizzle.

Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), ist eine angegebene Textur Anweisung ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) möglicherweise höchstens in dritter Reihenfolge abhängig. Eine abhängige Textur Anweisung der ersten Bestellung ist eine Textur Anweisung, in der Folgendes gilt:

-   src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   DST wurde bereits geschrieben und wird nun erneut geschrieben.

Eine abhängige Textur Anweisung in zweiter Reihenfolge wird als Textur Anweisung definiert, die ein temporäres Register (r) liest oder in ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) schreibt, \# dessen Inhalt vor dem Ausführen der Textur Anweisung (möglicherweise indirekt) auf das Ergebnis einer abhängigen Textur Anweisung der ersten Bestellung angewiesen ist. Eine (n) in der Reihenfolge abhängige Textur Anweisung wird von einer (n-1)<sup>th</sup>-<sup>Order-Textur</sup>Anweisung abgeleitet.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Quelle1 muss ein [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein. Swizzle ist für src0 oder Quelle1 zulässig. Das Swizzle wird vor der Textur Suche auf die Textur Koordinate angewendet.

## <a name="remarks"></a>Bemerkungen

Diese Anweisung wird in den folgenden Versionen unterstützt:



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

Die Anzahl der Koordinaten, die erforderlich sind, damit src0 das Textur Beispiel durchführen kann, hängt davon ab, wie Quelle1 deklariert wurde, sowie der. w-Komponente. [ \_ Samplertypen werden mit DCL samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)deklariert. Wenn Quelle1 als 2D-Sampler deklariert ist, muss src0. XY-Koordinaten enthalten. Wenn Quelle1 entweder als Cube-Sampler oder als volumesampler deklariert ist, muss src0 die. XYZ-Koordinaten enthalten. Das Sampling einer Textur mit weniger Dimensionen als in der Textur Koordinate vorhanden ist zulässig, da die zusätzlichen Texturkoordinaten Komponenten ignoriert werden.

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

 

 