---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexabletemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993239"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>DCL \_ indexabletemp (SM4-ASM)

Deklariert ein indexbares temporäres Register.



| DCL \_ indexabletemp x *N \[ Größe \] , ComponentCount* |
|-------------------------------------------------|



 



| Element                                                                                                                           | BESCHREIBUNG                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*Nr*<br/>                                                                         | \[in \] einer Ganzzahl, die die Registernummer angibt.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[Größe\]*<br/>                                                        | \[in \] einem optionalen ganzzahligen Wert. Die Anzahl der Elemente im Register Array.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[in \] einem optionalen ganzzahligen Wert. Die Anzahl der Komponenten im Register Array.<br/> |



 

Ein Register enthält ausreichend Speicherplatz für einen Wert von 32-Bit-vier Komponenten. die Anzahl der Elemente im Array von temporären Registern (indizierbar und [nicht indizierbar](dcl-temps.md)) darf 4096 nicht überschreiten.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Im folgenden finden Sie einige Beispiele für den Code, der für indizierbare Register generiert wurde.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



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

 

 





