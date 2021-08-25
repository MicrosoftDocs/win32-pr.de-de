---
title: dcl_inputPrimitive (sm4 - asm)
description: dcl \_ inputPrimitive (sm4 - asm)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479896"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>dcl \_ inputPrimitive (sm4 - asm)

Deklariert den primitiven Typ für Geometry-Shader-Eingaben.



| dcl \_ *inputPrimitive-Typ* |
|----------------------------|



 




| Element | BESCHREIBUNG | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>Typ</em><br /> | [in] Primitiver Eingabedatentyp, der einer der folgenden ist: <br /><ul><li><em>point</em> - point list</li><li><em>line</em> - line list</li><li><em>dreieck</em> – Dreiecksliste</li><li><em>line_adj:</em> Zeilenliste mit Adjacency-Daten</li><li><em>triangle_adj:</em> Dreiecksliste mit Adjacency-Daten</li></ul> | 




 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu erleichtern. Sie können mit shader Model 4 keinen Shader in der Assemblysprache erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





