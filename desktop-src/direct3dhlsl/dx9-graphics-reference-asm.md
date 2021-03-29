---
title: ASM-Shader-Referenz
description: Shader steuern die programmierbare Grafik Pipeline.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104976544"
---
# <a name="asm-shader-reference"></a>ASM-Shader-Referenz

Shader steuern die programmierbare Grafik Pipeline.

## <a name="vertex-shader-reference"></a>Vertex-Shader-Referenz

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Scheitelpunkt-Shader-Unterschiede](dx9-graphics-reference-asm-vs-differences.md) fassen die Unterschiede zwischen Scheitelpunkt-shaderversionen zusammen

## <a name="pixel-shader-reference"></a>Pixel-Shader-Referenz

-   [PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Pixel-shaderunterschiede](dx9-graphics-reference-asm-ps-differences.md) fasst die Unterschiede zwischen den Pixel-Shader-Versionen zusammen.

## <a name="shader-model-4-and-5-reference"></a>Referenz zu Shadermodell 4 und 5

In den Abschnitten [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) und [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) werden die Anweisungen beschrieben, die Shader Model 4 und 5 unterstützen.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Verhalten konstanter Register in assemblyshader

Es gibt zwei Möglichkeiten, Konstante Register in einem assemblyshader festzulegen:

-   Deklarieren Sie eine shaderkonstante in Assemblycode, indem Sie eine der DEF- \* Anweisungen verwenden.
-   Verwenden Sie eine der Set \* \* \* shaderconstant \* API-Methoden.

### <a name="direct3d-9-shader-constants"></a>Direct3D 9-Shader-Konstanten

In Direct3D 9 ist die Lebensdauer der definierten Konstanten in einem bestimmten Shader auf die Ausführung dieses Shaders beschränkt (und ist nicht über schreibbar). Definierte Konstanten in Direct3D 9 haben keine Nebeneffekte außerhalb des Shader.

Hier ist ein Beispiel für die Verwendung von Direct3D 9:


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



In Direct3D 9 ruft der Aufruf von "get \* \* \* shaderconstant" \* nur konstante Werte ab, die über Set \* \* \* shaderconstant festgelegt werden \* .

### <a name="direct3d-8-shader-constants"></a>Direct3D 8-Shader-Konstanten

Dieses Verhalten unterscheidet sich in Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



In Direct3D 8. x wird \* \* \* shaderconstant sofort wirksam. Betrachten Sie folgendes Szenario:


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



Das unerwünschte Ergebnis ist, dass die Reihenfolge, in der die Shader festgelegt werden, das beobachtete Verhalten einzelner Shader beeinflussen könnte.

## <a name="shader-driver-model-requirements"></a>Anforderungen an das Shader-Treibermodell

Direct3D 9-Schnittstellen sind auf Gerätetreiber Schnittstellen-Treiber (DDI) beschränkt, die DirectX 7-Level und höher sind. Führen Sie zum Überprüfen der DDI-Ebene das [DirectX-Diagnose Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) aus, und untersuchen Sie die gespeicherte Textdatei.

Für den Verweis funktionieren Direct3D 8-Schnittstellen nur für DDI-Treiber, die DirectX 6-Level und höher sind.

## <a name="shader-binary-format"></a>Binäres shaderformat

Das bitweise Layout des Shader-Anweisungs Datenstroms wird in D3d9types. h definiert. Wenn Sie Ihren eigenen Shader-Compiler oder die Konstruktions Tools entwerfen möchten und weitere Informationen zum Shader-Tokenstream benötigen, lesen Sie das Direct3D 9 Driver Development Kit (DDK).

## <a name="c-like-shader-language"></a>C-ähnliche Shader-Sprache

Weitere Informationen finden Sie in der [HLSL-Referenz](dx-graphics-hlsl-reference.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis für HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




