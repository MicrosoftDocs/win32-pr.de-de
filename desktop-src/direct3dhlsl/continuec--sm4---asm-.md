---
title: continuec (sm4 - asm)
description: Setzt die Ausführung am Anfang der aktuellen Schleife bedingt fort.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d909c199dc0ceaa4e5498429f1ac3a136d3fb75d930e392d7f6fd8230e5b49b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909057"
---
# <a name="continuec-sm4---asm"></a>continuec (sm4 - asm)

Setzt die Ausführung am Anfang der aktuellen Schleife bedingt fort.



| continuec{ \_ z\|\_nz} src0.select-Komponente \_ |
|---------------------------------------------|



 



| Begriff                                                            | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente, für die die Bedingung getestet werden soll.<br/> |



 

## <a name="remarks"></a>Hinweise

**continuec** kann nur innerhalb einer [Schleife](loop--sm4---asm-.md) oder [in endloop](endloop--sm4---asm-.md)verwendet werden.

Im folgenden Beispiel wird die Verwendung der **continuec-Anweisung** veranschaulicht.


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



Das Tokenformat enthält zur Vereinfachung den Offset der entsprechenden Schleifenanweisung im Shader.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





