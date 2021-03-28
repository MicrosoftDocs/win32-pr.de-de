---
title: if (SM4-ASM)
description: Verzweigung auf der Grundlage des logischen OR-Ergebnisses.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992966"
---
# <a name="if-sm4---asm"></a>if (SM4-ASM)

Verzweigung auf der Grundlage des logischen OR-Ergebnisses.



| Wenn { \_ z \|\_NZ} src0. Select- \_ Komponente |
|--------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]enthält die Komponente, auf der die Bedingung getestet werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das tokenformat enthält den Offset der entsprechenden endif-Anweisung im Shader.

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Beschränkungen

-   Die Quell Operanden (bei 4 Komponenten Vektoren) müssen eine einzelne Komponentenauswahl verwenden.
-   Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, **Wenn \_ z** true ist. , Wenn alle Bits 0 (null) sind,, **Wenn \_ NZ** true ist.
-   Fluss Kontroll Blöcke können bis zu 64 tief pro Unterroutine (und Main) verschachteln. Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten. Das Verhalten von Ablauf Steuerungs Anweisungen über 64 Ebenen tief (pro Unterroutine) ist nicht definiert.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





