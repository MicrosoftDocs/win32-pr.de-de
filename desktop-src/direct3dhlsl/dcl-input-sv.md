---
title: dcl_input_sv (SM4-ASM)
description: DCL- \_ Eingabe \_ SV (SM4-ASM)
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719487"
---
# <a name="dcl_input_sv-sm4---asm"></a>DCL- \_ Eingabe \_ SV (SM4-ASM)

Deklariert ein Shader-Input-Register, das erwartet, dass ein [System Wert](dx-graphics-hlsl-semantics.md) aus einer vorherigen Phase bereitgestellt wird.



| DCL- \_ Eingabe \_ SV v *N \[ . \] Mask*, *systemvaluename \[ , InterpolationMode \]* |
|------------------------------------------------------------------------|



 



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
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemvaluename</em><br/></td>
<td>in Der Name des System Werts, bei dem es sich um eine Zeichenfolge (siehe <a href="dx-graphics-hlsl-semantics.md">System-Wert-Semantik</a>) ohne das &quot; &quot; Präfix SV_ handelt.<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>InterpolationMode</em><br/></td>
<td>[in] Optional. Der Interpolations Modus, der beeinflusst, wie Werte während der rasterisierung berechnet werden. der-Modus wird nur von einem Pixelshader verwendet. Es kann sich um einen der folgenden Werte handeln: <br/>
<ul>
<li>Constant-interpolieren nicht zwischen Register Werten.</li>
<li>Linear-interpolieren linear zwischen den Register Werten.</li>
<li>linearcentroid-identisch mit linear, aber Schwerpunkt beim Multisampling.</li>
<li>linearnoperspektive-identisch mit linear, aber ohne Perspektiven Korrektur.</li>
<li>linearnoperspectivecentroid-identisch mit linear, aber ohne Perspektiven Korrektur und Schwerpunkt beim Multisampling.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Eine Komponenten Maske für eine System Wert Deklaration kann eine beliebige Teilmenge von \[ xyzw sein \] ; Deklarationen können sich möglicherweise nicht überlappen (jede Deklaration muss der Sequenz-xyzw entsprechen). Beim Deklarieren von skalaren System Werten (z. b. Clip Distance und Auslesen Distance) können Sie mehrere System Werte in einem einzelnen Register deklarieren. Stellen Sie in diesem Fall sicher, dass andere Modifizierer wie die Interpolations Modi Stimmen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Hier einige Beispiele:


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
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

 

 





