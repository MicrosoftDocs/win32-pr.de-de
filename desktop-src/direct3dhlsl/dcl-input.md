---
title: dcl_input (sm4 – asm)
description: dcl \_ input (sm4 – asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3242c2f1e753407d239057fdc4af0a6f04d6d83a66e2a22ffb1be929583c21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986740"
---
# <a name="dcl_input-sm4---asm"></a>dcl \_ input (sm4 – asm)

Deklariert ein Shadereingaberegister.



| dcl \_ input v *N \[ .mask , \] \[ interpolationMode \]* |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br/></td>
<td>[in] Ein Scheitelpunktdatenregister. <br/>
<ul>
<li><em>N</em> ist eine ganze Zahl, die die Registernummer identifiziert.</li>
<li><em>[.mask]</em> ist eine optionale Komponentenmaske (.xyzw), die angibt, welche der Registerkomponenten verwendet werden soll.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>Interpolationmode</em><br/></td>
<td>[in] Optional. Der Interpolationsmodus, der nur bei Pixel-Shadereingaberegistern berücksichtigt wird. Es kann sich um einen der folgenden Werte handeln: <br/>
<ul>
<li>constant: Interpolieren Sie nicht zwischen Registerwerten.</li>
<li>linear: Interpolieren Sie linear zwischen Registerwerten.</li>
<li>linearCentroid: entspricht dem linearen, aber beim Multisampling klammerten Schwerpunkt.</li>
<li>linearNoperspective – identisch mit linear, aber ohne perspektivische Korrektur.</li>
<li>linearNoperspectiveCentroid– identisch mit linearer, bei Multisampling geklammerter Schwerpunkt, keine perspektivische Korrektur.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Hinweise zur Interpolation

Standardmäßig werden Scheitelpunktattribute von einem Pixelmittelpunkt interpoliert, wenn Multisample-Antialiasing ausgeführt wird. Wenn ein Pixelmittelpunkt nicht abgedeckt ist, wird ein Attribut vor der Interpolation in einen Pixelmittelpunkt extrapoliert.

Für ein Pixel, das nicht vollständig abgedeckt ist, oder ein Attribut, das keinen Pixelmittelpunkt abdeckt, können Sie einen Schwerpunkt für die Stichprobenentnahme angeben, wodurch die Stichprobenentnahme an einer Stelle innerhalb des abgedeckten Bereichs des Pixels durchgeführt wird. Da eine Beispielmaske (sofern verwendet) angewendet wird, bevor der Schwerpunkt berechnet wird, kann jeder durch die Stichprobenmaske maskierte Beispielspeicherort nicht als Schwerpunktspeicherort ausgewählt werden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Um die Eingabe als Systemwert zu identifizieren, verwenden Sie [dcl \_ input sv \_ (sm4 - asm)](dcl-input-sv.md).

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiele:


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





