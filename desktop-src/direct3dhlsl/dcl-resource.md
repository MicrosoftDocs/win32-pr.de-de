---
title: dcl_resource (SM4-ASM)
description: DCL \_ -Ressource (SM4-ASM)
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719470"
---
# <a name="dcl_resource-sm4---asm"></a>DCL \_ -Ressource (SM4-ASM)

Deklariert eine nicht Multisampling-Shader-Input-Ressource.



| DCL- \_ Ressource *tN*, *ResourceType*, *returnType (e)* |
|-----------------------------------------------------|



 

Deklariert eine Multisampling-Ressource "Shader-Input".



| DCL- \_ Ressource *tN*, *ResourceType \[ size \] NN*, *returnType (e)* |
|---------------------------------------------------------------|



 



| Element                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[im \] Textur Register, wobei *N* eine ganze Zahl ist, die die Registernummer bezeichnet.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*ResourceType*<br/>                                   | \[in \] jedem Objekttyp, der auf der Seite [Textur Objekt](dx-graphics-hlsl-to-type.md) aufgeführt ist.<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*ResourceType- \[ Größe \] NN*<br/> | \[in \] einem Texture2D-oder Texture2DArray-Objekttyp (siehe [Textur-Objekt](dx-graphics-hlsl-to-type.md) Seite); *size* ist eine optionale ganze Zahl, die die Anzahl der Elemente im Array bezeichnet. *NN* ist eine ganze Zahl, die die Anzahl der multisamples bezeichnet.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*ReturnType (e)*<br/>                               | \[der \] Rückgabetyp pro Komponente, der eines der folgenden ist: unorm, snorm, Sint, uint oder float. Die Anzahl der Rückgabe Typen kann bis zu 1 betragen (wenn alle Komponenten denselben Typ aufweisen), kann aber so viele wie vier sein.<br/>                                          |



 

Der Zugriff auf eine Ressource erfolgt in HLSL mithilfe von " [Load](dx-graphics-hlsl-to-load.md)". auf eine Textur, auf die nicht mehr zugegriffen werden kann, kann auch mithilfe einer beliebigen HLSL- [Textur Objekt](dx-graphics-hlsl-to-type.md) -Beispiel Methode zugegriffen werden.

Wenn eine Ressource an eine Shader-Stufe gebunden ist, wird das Ressourcen Format mit dem Rückgabetyp überprüft.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_resource t3, buffer, UNORM
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

 

 





