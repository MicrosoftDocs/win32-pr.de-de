---
title: dcl_input (SM4-ASM)
description: DCL \_ -Eingabe (SM4-ASM)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993230"
---
# <a name="dcl_input-sm4---asm"></a>DCL \_ -Eingabe (SM4-ASM)

Deklariert ein Shader-Input-Register.



| DCL- \_ Eingabe *v \[ . mask \] \[ , InterpolationMode \]* |
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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em><br/></td>
<td>in Ein Scheitelpunkt Datenregister. <br/>
<ul>
<li><em>N</em> ist eine ganze Zahl, die die Registernummer identifiziert.</li>
<li><em>[. mask]</em> ist eine optionale Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>InterpolationMode</em><br/></td>
<td>[in] Optional. Der Interpolations Modus, der nur für Pixel-Shader-Eingabe Register berücksichtigt wird. Es kann sich um einen der folgenden Werte handeln: <br/>
<ul>
<li>Constant-interpolieren nicht zwischen Register Werten.</li>
<li>Linear-interpolieren linear zwischen den Register Werten.</li>
<li>linearcentroid-identisch mit linear, aber Schwerpunkt beim Multisampling.</li>
<li>linearnoperspektive-identisch mit linear, aber ohne Perspektiven Korrektur.</li>
<li>linearnoperspectivecentroid-identisch mit linear, Schwerpunkt bei Multisampling, keine Perspektiven Korrektur.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Interpolations Hinweise

Standardmäßig werden Vertex-Attribute bei der Durchführung von Multisampling-Antialiasing von einem Pixel Center interpoliert. Wenn ein Pixel Center nicht abgedeckt wird, wird ein Attribut vor der interpolung zu einem Pixel Center hoch-

Bei einem Pixel, das nicht vollständig abgedeckt ist, oder bei einem Attribut, das kein Pixel Center abdeckt, können Sie eine Schwerpunkt-Stichprobenentnahme angeben, die erzwingt, dass die Stichprobenentnahme irgendwo innerhalb des betroffenen Bereichs des Pixels erfolgt. Da eine Beispiel Maske (sofern verwendet) vor dem Berechnen des Schwerpunkts angewendet wird, kann der von der Beispiel Maske maskierte Beispiel Speicherort nicht als Schwerpunkt ausgewählt werden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Verwenden Sie [DCL \_ input \_ SV (SM4-ASM)](dcl-input-sv.md), um die Eingabe als System Wert zu identifizieren.

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Hier einige Beispiele.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





