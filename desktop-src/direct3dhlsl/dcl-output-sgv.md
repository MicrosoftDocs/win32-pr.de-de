---
title: dcl_output_sgv (SM4-ASM)
description: DCL \_ \_ -Ausgabe scalable (SM4-ASM)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389596"
---
# <a name="dcl_output_sgv-sm4---asm"></a>DCL \_ \_ -Ausgabe scalable (SM4-ASM)

Deklariert ein Ausgabe Register, das einen [System Wert](dx-graphics-hlsl-semantics.md) Parameter enthält.



| DCL- \_ Ausgabe \_ Scalable on *\[ . \] Mask*, *systemvalue* |
|-----------------------------------------------|



 



| Element                                                                                                                               | BESCHREIBUNG                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[in \] einem Ausgabedaten Register; *N* ist eine ganze Zahl, die die Registernummer bezeichnet.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*<br/>                                                         | \[in \] optional. Eine Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemvaluename*<br/> | \[\]der Name des System Werts, bei dem es sich um eine Zeichenfolge handelt (siehe [System-Wert-Semantik](dx-graphics-hlsl-semantics.md)), ohne das Präfix "SV" \_ .<br/> |



 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_output_sgv o4.x, primitiveID
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

 

 





