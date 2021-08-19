---
title: texldb – ps
description: Voreingenommene Texturladeanweisung. In dieser Anweisung wird das vierte Element (.a oder .w) verwendet, um die Detailebene der Textursampling unmittelbar vor der Stichprobenentnahme zu verzerren.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddf340840e377ee03641ae33c0731f27e90ce4760cad4ddb6c636c1831fa80ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505793"
---
# <a name="texldb---ps"></a>texldb – ps

Voreingenommene Texturladeanweisung. In dieser Anweisung wird das vierte Element (.a oder .w) verwendet, um die Detailebene der Textursampling unmittelbar vor der Stichprobenentnahme zu verzerren.

## <a name="syntax"></a>Syntax



| texldb dst, src0, src1 |
|------------------------|



 

Hierbei gilt:

-   dst ist das Zielregister.
-   src0 ist ein Quellregister, das die Texturkoordinaten für das Texturbeispiel bereitstellt. Siehe [Texturkoordinatenregister.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifiziert den [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s), \# wobei \# angibt, welche Textur-Samplernummer entnommen werden soll. Der Sampler hat ihm eine Textur und einen sampler-Zustand zugeordnet, der durch [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)definiert wird.

Informationen zu den Einschränkungen bei der Verwendung von texldb finden Sie in der Anweisung [texld - ps \_ 2 \_ 0 und up.](texld---ps-2-0.md)

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 und ps \_ 2 \_ x

dst muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) \# sein, und nur die XYZW-Maske (Standardmaske) ist zulässig.

src0 muss entweder ein [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# (t) oder ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) ohne \# Modifizierer oder Swizzle sein.

src1 muss ein [Sampler (Direct3D 9 asm-ps) (s)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# sein, ohne Modifizierer oder Swizzle.

Wenn das D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT-Cap-Bit nicht festgelegt ist (in D3DPSHADERCAPS2 \_ 0), kann eine bestimmte Texturanweisung (texld, texldp, texldb, texldd) höchstens von der dritten Reihenfolge abhängen. Eine in erster Ordnung abhängige Texturanweisung ist eine Texturanweisung, in der eine der beiden

-   src0 ist ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst wurde zuvor geschrieben und jetzt erneut geschrieben.

Eine abhängige Texturanweisung der zweiten Ordnung wird als Texturanweisung definiert, die ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) liest oder \# schreibt, dessen Inhalt vor dem Ausführen der Texturanweisung (möglicherweise indirekt) vom Ergebnis einer abhängigen Texturanweisung erster Ordnung abhängt. Eine (n)<sup>th-order-abhängige</sup>Texturanweisung wird von einer Texturanweisung (n - 1)<sup>mit</sup>der Reihenfolge abgeleitet.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 muss ein [Sampler (Direct3D 9 asm-ps) (s)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# ohne Modifizierer sein. Swizzle ist für src1 zulässig, und wenn sie angewendet werden, werden die Ergebnisse der Textursuche vor dem Schreiben in dst vorverwendet.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb verzerrt die Detailebene der Mipmap, die normalerweise als Teil des Beispielprozesses durch den (signierten) Wert in src0.w berechnet wird. Positive Biaswerte führen dazu, dass kleinere Mipmaps ausgewählt werden und umgekehrt. Für ps \_ 2 \_ 0 und ps \_ 2 \_ x können Biaswerte im Bereich \[ von -3,0, +3,0 \] liegen. Für ps \_ 3 \_ 0 können Biaswerte im Bereich \[ von -16,0, +15,0 \] liegen. Verschiebungswerte außerhalb dieser Bereiche führen zu nicht definierten Ergebnissen. Der Samplerzustand D3DSAMP \_ MIPMAPLODBIAS wird weiterhin berücksichtigt, und die Texldb-Voreingenommenheit wird hinzugefügt, jedoch pro Pixel. Nachdem die voreingenommene Detailebene berechnet wurde, wird D3DSAMP \_ MAXMIPLEVEL weiterhin berücksichtigt, und das Texturbeispiel tritt auf. Nach texldb ist der Inhalt von src0 nicht betroffen (es sei denn, dst ist dasselbe Register).

Die Anzahl der Koordinaten, die für src0 zum Ausführen des Texturbeispiels erforderlich sind, hängt davon ab, wie src1 deklariert wurde, sowie die W-Komponente. Samplertypen werden mit [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)deklariert. Wenn src1 als 2D-Sampler deklariert ist, muss src0 XYW-Koordinaten enthalten. Wenn src1 entweder als Cube-Sampler oder als Volume-Sampler deklariert wird, muss src0 .xyzw-Koordinaten enthalten. Das Sampling einer 2D-Textur mit XYZW-Koordinaten ist zulässig (die Z-Koordinate wird ignoriert).

Wenn die Quelltextur weniger als vier Komponenten enthält, werden die Standardwerte in den fehlenden Komponenten platziert. Die Standardwerte hängen vom Texturformat ab, wie in der folgenden Tabelle gezeigt:



| Texturformat                                                                                          | Standardwerte       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ A8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Alle Tiefen-/Schablonenformate                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 