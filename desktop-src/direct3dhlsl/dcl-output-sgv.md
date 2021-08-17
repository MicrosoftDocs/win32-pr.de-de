---
title: dcl_output_sgv (sm4 – asm)
description: dcl \_ output \_ sgv (sm4 - asm)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b3214d262b6ed199e86836a2dd997f8efa6a57ecf99cf43f19630e71ff14b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727014"
---
# <a name="dcl_output_sgv-sm4---asm"></a>dcl \_ output \_ sgv (sm4 - asm)

Deklariert ein Ausgaberegister, das einen [Systemwertparameter](dx-graphics-hlsl-semantics.md) enthält.



| dcl \_ output \_ sgv oN *\[ .mask \]*, *systemValue* |
|-----------------------------------------------|



 



| Element                                                                                                                               | Beschreibung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[in \] Ein Ausgabedatenregister; *N* ist eine ganze Zahl, die die Registernummer angibt.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*<br/>                                                         | \[in \] Optional. Eine Komponentenmaske (.xyzw), die angibt, welche der Registerkomponenten verwendet werden soll.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[in \] Der Systemwertname, bei dem es sich um eine Zeichenfolge handelt (siehe [Systemwertsemantik)](dx-graphics-hlsl-semantics.md)ohne das \_ Präfix "SV".<br/> |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_output_sgv o4.x, primitiveID
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

 

 





