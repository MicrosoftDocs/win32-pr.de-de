---
title: Bezeichnung (SM4-ASM)
description: Gibt den Anfang einer Unterroutine an.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719416"
---
# <a name="label-sm4---asm"></a>Bezeichnung (SM4-ASM)

Gibt den Anfang einer Unterroutine an.



| Bezeichnung l\# |
|-----------|



 



| Element                                                       | BESCHREIBUNG                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*int\#*<br/> | \[in \] der Nummer der Bezeichnung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine **Bezeichnung** kann nur direkt nach einer [**ret**](ret--sm4---asm-.md) -Anweisung angezeigt werden, die in keiner der Fluss Steuerungs Anweisungen enthalten ist.

Der Code vor der ersten **Bezeichnung** in einem Programm ist das Hauptprogramm. Alle Unterroutinen werden am Ende des Programms angezeigt, das durch Bezeichnungs Anweisungen **angegeben wird.**

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

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

 

 





