---
title: continuec (SM4-ASM)
description: Führt die Ausführung am Anfang der aktuellen Schleife bedingt aus.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976368"
---
# <a name="continuec-sm4---asm"></a>continuec (SM4-ASM)

Führt die Ausführung am Anfang der aktuellen Schleife bedingt aus.



| continuec { \_ z \|\_NZ} src0. Select- \_ Komponente |
|---------------------------------------------|



 



| Begriff                                                            | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Komponente, für die die Bedingung getestet werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

**continuec** kann nur innerhalb einer [Schleife](loop--sm4---asm-.md) oder einer [endschleife](endloop--sm4---asm-.md)verwendet werden.

Im folgenden Beispiel wird gezeigt, wie die **continuec** -Anweisung verwendet wird.


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



Das tokenformat enthält den Offset der entsprechenden Schleifen Anweisung im Shader.

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

 

 





