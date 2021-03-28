---
title: Switch (SM4-ASM)
description: Überträgt die Steuerung in Abhängigkeit vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038336"
---
# <a name="switch-sm4---asm"></a>Switch (SM4-ASM)

Überträgt die Steuerung in Abhängigkeit vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.



| Switch src0. ausgewählte \_ Komponente |
|---------------------------------|



 



| Element                                                            | BESCHREIBUNG                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Auswahl für die Switch-Anweisung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein **Switch**- / [endswitchkonstrukt](endswitch--sm4---asm-.md) verhält sich genau  wie ein switchkonstrukt in der Programmiersprache C, mit der folgenden Ausnahme: bei Standard Anweisungen für D3D11 [Case](case--sm4---asm-.md) / [](default--sm4---asm-.md) , die bis zum nächsten **Fall** den Standardwert ohne Unterbrechung durchlaufen, /  kann kein Code enthalten sein. [](break--sm4---asm-.md) Es ist zulässig, dass mehrere **Case** -Anweisungen (einschließlich **Standard**) sequenziell angezeigt werden und denselben Codeblock gemeinsam nutzen.

Die Bedingung muss eine 32-Bit-Register Komponente oder eine sofortige Menge sein. Der Gleichheits Vergleich ist bitweise (Integer).

Wie bei jeder shaderanweisung in D3D11 kann das **switchkonstrukt von** Hardware nicht direkt implementiert werden.

**Switch** -Anweisungen können eingebettet werden. Jeder **Switch** -Block zählt als 1 Ebene für die Schachtelungs Schachtelungs Tiefe von 64 pro Unterroutine und Main, unabhängig von der Anzahl der **Case** -Anweisungen. Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten. Das Verhalten von Ablauf Steuerungs Anweisungen, die eine Tiefe von 64 Ebenen überschreiten, ist nicht definiert.

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

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

 

 





