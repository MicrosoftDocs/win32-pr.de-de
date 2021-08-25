---
title: dcl_outputTopology (sm4 – asm)
description: dcl \_ outputTopology (sm4 – asm)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6a3b46dc226a85593a17b02118ed52088ed75d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471996"
---
# <a name="dcl_outputtopology-sm4---asm"></a>dcl \_ outputTopology (sm4 – asm)

Deklariert die Ausgabedaten des primitiven Typs geometry-shader.



| dcl \_ *outputTopology-Typ* |
|----------------------------|



 




| Element | BESCHREIBUNG | 
|------|-------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Typ</em><br /> | [in] Eine primitive Ausgabetopologie, bei der es sich um einen der folgenden Werte handelt: <br /><ul><li><em>Pointlist</em></li><li><em>linestrip</em></li><li><em>trianglestrip</em></li></ul> | 




 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_outputTopology trianglestrip
```



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

 

 





