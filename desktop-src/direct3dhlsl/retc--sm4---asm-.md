---
title: RETC (SM4-ASM)
description: Bedingter Rückgabe.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976441"
---
# <a name="retc-sm4---asm"></a>RETC (SM4-ASM)

Bedingter Rückgabe.



| RETC { \_ z \|\_NZ} src0. Select- \_ Komponente |
|----------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[im \] Register, um die Bedingung zu testen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn in einer Unterroutine, wird diese Anweisung bedingt an die Anweisung nach dem-Befehl zurückgegeben. Wenn Sie sich nicht innerhalb einer Unterroutine befinden, beendet diese Anweisung die Programmausführung.

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

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

-   **RETC** kann beliebig oft in einem Programm vorkommen.
-   Die letzte Anweisung in einem Hauptprogramm oder einer Unterroutine darf keine **RETC- \_ z** -oder **RETC- \_ NZ** sein. Stattdessen kann der bedingungslose [ret](ret--sm4---asm-.md) verwendet werden.
-   Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, gibt **ret \_ NZ** zurück. Wenn alle Bits NULL sind, wird von **RETC \_ z** zurückgegeben.

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

 

 





