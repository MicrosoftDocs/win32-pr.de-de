---
title: dcl_temps (sm4 - asm)
description: dcl \_ temps (sm4 - asm)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6426caff8ecd347ce8233f15df6b914a53c647ae79fb50a530b531e9207bf1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726808"
---
# <a name="dcl_temps-sm4---asm"></a>dcl \_ temps (sm4 - asm)

Deklariert temporäre Register.



| dcl \_ temps N |
|--------------|



 



| Element                                                   | Beschreibung                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Die Anzahl temporärer Register.<br/> |



 

Jedes Register verfügt über Platz für einen 32-Bit-Wert mit vier Komponenten. Die Gesamtzahl temporärer und [indizierbarer temporärer](dcl-indexabletemp.md) Register muss kleiner oder gleich 4096 sein.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu erleichtern. Sie können mit shader Model 4 keinen Shader in der Assemblysprache erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_temps 10; // Declare r0-r9
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

 

 





