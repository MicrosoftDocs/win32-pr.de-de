---
title: retc (sm4 - asm)
description: Bedingte Rückgabe.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d65cf64c3c1fb7945f93053f280be3eb3bd9d5fe76e34f30102316b1f1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853740"
---
# <a name="retc-sm4---asm"></a>retc (sm4 - asm)

Bedingte Rückgabe.



| retc{ \_ z\|\_nz} src0.select-Komponente \_ |
|----------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in Das Register, mit dem die Bedingung getestet werden \] soll.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn sich diese Anweisung innerhalb einer Unterroutine befindet, kehrt sie nach dem Aufruf bedingt zur Anweisung zurück. Wenn sich diese Anweisung nicht in einer Unterroutine befindet, wird die Programmausführung beendet.

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>Beschränkungen

-   **Retc** kann beliebig oft an einer beliebigen Stelle in einem Programm angezeigt werden.
-   Die letzte Anweisung in einem Hauptprogramm oder einer Unterroutine kann kein **retc \_ z** oder **retc \_ nz** sein. Stattdessen kann die bedingungslose [Wiederholung](ret--sm4---asm-.md) verwendet werden.
-   Das von *src0* bereitgestellte 32-Bit-Register wird auf Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, wird **ret \_ nz** zurückgegeben. Wenn alle Bits 0 (null) sind, wird **retc \_ z** zurückgegeben.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





