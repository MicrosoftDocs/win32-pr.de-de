---
title: label (sm4 - asm)
description: Gibt den Anfang einer Unterroutine an.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9075aa14d72893d7c7862361b44ff636dd9bb6fda62563087ca2404bd1d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986460"
---
# <a name="label-sm4---asm"></a>label (sm4 - asm)

Gibt den Anfang einer Unterroutine an.



| Label l\# |
|-----------|



 



| Element                                                       | Beschreibung                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[in \] Die Bezeichnungsnummer.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine **Bezeichnung** kann nur direkt nach einer [**ret-Anweisung**](ret--sm4---asm-.md) angezeigt werden, die in keiner Flusssteuerungsanweisungen geschachtelt ist.

Der Code vor der ersten **Bezeichnung** in einem Programm ist das Hauptprogramm. Alle Unterroutinen werden am Ende des  Programms angezeigt, angegeben durch Bezeichnungsanweisungen.

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

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

 

 





