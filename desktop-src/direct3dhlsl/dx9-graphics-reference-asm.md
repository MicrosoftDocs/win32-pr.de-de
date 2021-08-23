---
title: Asm-Shaderreferenz
description: Shader sind die Steuerung der programmierbaren Grafikpipeline.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9dbeb680b7131581b3891e59bb6bd2db0d6e5c19eb6279c47b83d22f01b5000e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119544"
---
# <a name="asm-shader-reference"></a>Asm-Shaderreferenz

Shader sind die Steuerung der programmierbaren Grafikpipeline.

## <a name="vertex-shader-reference"></a>Vertex-Shaderreferenz

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [Vs. \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Vertex-Shader-Unterschiede](dx9-graphics-reference-asm-vs-differences.md) fasst die Unterschiede zwischen Vertex-Shaderversionen zusammen.

## <a name="pixel-shader-reference"></a>Pixel-Shaderreferenz

-   [ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [ps \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Unter Unterschiede zwischen Pixel-Shadern](dx9-graphics-reference-asm-ps-differences.md) werden die Unterschiede zwischen den Shaderversionen von Pixeln zusammengefasst.

## <a name="shader-model-4-and-5-reference"></a>Shadermodell 4- und 5-Referenz

In [den Abschnitten Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) und [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) werden die Anweisungen beschrieben, die shader model 4 und 5 unterstützen.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Verhalten konstanter Register in Assembly-Shadern

Es gibt zwei Möglichkeiten zum Festlegen konstanter Register in einem Assembly-Shader:

-   Deklarieren Sie eine Shaderkonstation im Assemblycode mithilfe einer der \* Def-Anweisungen.
-   Verwenden Sie eine der Set \* \* \* ShaderConstant-API-Methoden. \*

### <a name="direct3d-9-shader-constants"></a>Direct3D 9 Shader-Konstanten

In Direct3D 9 ist die Lebensdauer definierter Konstanten in einem bestimmten Shader auf die Ausführung dieses Shaders beschränkt (und nicht überschreibbar). Definierte Konstanten in Direct3D 9 haben keine Nebeneffekte außerhalb des Shaders.

Hier ist ein Beispiel mit Direct3D 9:


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



In Direct3D 9 ruft der Aufruf von Get ShaderConstant nur konstante Werte ab, die über \* \* \* \* Set \* \* \* ShaderConstant festgelegt \* wurden.

### <a name="direct3d-8-shader-constants"></a>Direct3D 8 Shader-Konstanten

Dieses Verhalten ist in Direct3D 8.x anders.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



In Direct3D 8.x wird \* \* \* Set ShaderConstant sofort wirksam. Betrachten Sie folgendes Szenario:


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



Das unerwünschte Ergebnis ist, dass sich die Reihenfolge, in der die Shader festgelegt werden, auf das beobachtete Verhalten einzelner Shader auswirken kann.

## <a name="shader-driver-model-requirements"></a>Anforderungen an das Shadertreibermodell

Direct3D 9-Schnittstellen sind auf DDI-Treiber (Device Driver Interface) beschränkt, bei denen es sich um DirectX 7-Treiber oder höher handelt. Um die DDI-Ebene zu überprüfen, führen Sie das [DirectX-Diagnosetool aus,](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) und untersuchen Sie die gespeicherte Textdatei.

Als Referenz können Direct3D 8-Schnittstellen nur auf DDI-Treibern mit DirectX 6-Ebene und höher verwendet werden.

## <a name="shader-binary-format"></a>Shader-Binärformat

Das bitweise Layout des Shaderanweisungsstreams wird in D3d9types.h definiert. Wenn Sie Ihren eigenen Shadercompiler oder Ihre eigenen Konstruktionstools entwerfen möchten und weitere Informationen zum Shadertokenstream wünschen, lesen Sie das Direct3D 9 Driver Development Kit (DDK).

## <a name="c-like-shader-language"></a>C-like Shader Language

Informationen zu einer C- like-Shader-Sprache finden Sie in der [HLSL-Referenz.](dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




