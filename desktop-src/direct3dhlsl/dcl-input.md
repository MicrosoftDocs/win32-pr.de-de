---
title: dcl_input (sm4 - asm)
description: dcl \_ input (sm4 - asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8214287a4afb4c683a94e213cdfed133c03219e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467007"
---
# <a name="dcl_input-sm4---asm"></a>dcl \_ input (sm4 - asm)

Deklariert ein Shadereingaberegister.



| dcl \_ input v *N \[ .mask , \] \[ interpolationMode \]* |
|-------------------------------------------------|



 




| Element | BESCHREIBUNG | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br /> | [in] Ein Vertexdatenregister. <br /><ul><li><em>N ist</em> eine ganze Zahl, die die Registernummer identifiziert.</li><li><em>[.mask] ist</em> eine optionale Komponentenmaske (.xyzw), die angibt, welche der Registerkomponenten verwendet werden soll.</li></ul> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>Interpolationmode</em><br /> | [in] Optional. Der Interpolationsmodus, der nur bei Pixel-Shadereingaberegistern verwendet wird. Es kann sich um einen der folgenden Werte handeln: <br /><ul><li>constant: Interpolieren Sie nicht zwischen Registerwerten.</li><li>linear: Lineare Interpolation zwischen Registerwerten.</li><li>linearCentroid: identisch mit linearem, aber beim Multisampling festgeklammerten Schwerpunkt.</li><li>linearNoperspective: identisch mit linear, aber ohne Perspektivkorrektur.</li><li>linearNoperspectiveCentroid– identisch mit linearem Schwerpunkt, der beim Multisampling an den Klammern klammert wird, keine Perspektivkorrektur.</li></ul> | 




 

### <a name="interpolation-notes"></a>Interpolationshinweise

Standardmäßig werden Scheitelpunktattribute von einem Pixelmittelpunkt interpoliert, wenn Multisample-Antialiasing verwendet wird. Wenn ein Pixelcenter nicht abgedeckt wird, wird ein Attribut vor der Interpolation zu einem Pixelcenter extrapoliert.

Für ein Pixel, das nicht vollständig abgedeckt ist, oder ein Attribut, das keinen Pixelzentrierungsbereich verdeckt, können Sie schwerpunktsyntierte Stichprobenentnahme angeben, die erzwingt, dass die Stichprobenentnahme an einer stelle innerhalb des abgedeckten Bereichs des Pixels erfolgt. Da eine Beispielmaske (sofern verwendet) angewendet wird, bevor der Schwerpunkt berechnet wird, kann jeder von der Beispielmaske maskierte Beispielspeicherort nicht als Schwerpunktposition ausgewählt werden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Verwenden Sie dcl input [ \_ sv \_ (sm4 - asm),](dcl-input-sv.md)um die Eingabe als Systemwert zu identifizieren.

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu erleichtern. Sie können mit shader Model 4 keinen Shader in der Assemblysprache erstellen.

## <a name="example"></a>Beispiel

Die folgende Auflistung enthält einige Beispiele:


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





