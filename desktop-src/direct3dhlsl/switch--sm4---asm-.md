---
title: switch (sm4 - asm)
description: Überträgt die Steuerung abhängig vom Wert eines Selektors an einen anderen Anweisungsblock innerhalb des Switchtexts.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39cb304c1ccf59c188a4e1f20f2b136897d833c80d6eb67cb0eb683d628ab9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724351"
---
# <a name="switch-sm4---asm"></a>switch (sm4 - asm)

Überträgt die Steuerung abhängig vom Wert eines Selektors an einen anderen Anweisungsblock innerhalb des Switchtexts.



| switch src0.selected-Komponente \_ |
|---------------------------------|



 



| Element                                                            | BESCHREIBUNG                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Selektor für die switch-Anweisung.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein **switch** / [endswitch-Konstrukt](endswitch--sm4---asm-.md) verhält sich genau wie ein **Switchkonstrukt** in der Programmiersprache C, mit der folgenden Ausnahme: Für D3D11-Fall können [](case--sm4---asm-.md) / [Standardanweisungen,](default--sm4---asm-.md) die ohne Unterbrechung auf den nächsten **Fallstandard** fallen, keinen Code /  enthalten. [](break--sm4---asm-.md) Es ist zulässig, dass mehrere **Case-Anweisungen,** einschließlich **standard**, sequenziell angezeigt werden und denselben Codeblock gemeinsam nutzen.

Die Bedingung muss eine 32-Bit-Registerkomponente oder eine sofortige Menge sein. Der Gleichheitsvergleich ist bitweise (ganze Zahl).

Wie bei jeder Shaderanweisung in D3D11 kann hardware das **Switchkonstrukt** direkt implementieren oder nicht.

**Switch-Anweisungen** können geschachtelt werden. Jeder **Switchblock** zählt unabhängig von der Anzahl der **Case-Anweisungen** als 1 Ebene im Hinblick auf die Schachtelungstiefe der Flusssteuerung von 64 pro Unterroutine und Main. Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten. Das Verhalten von Ablaufsteuerungsanweisungen über 64 Ebenen pro Unterroutine ist nicht definiert.

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

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

 

 





