---
title: Shadermodell 4
description: Shadermodell 4 ist eine Obermenge der Funktionen in ShaderModell 3, mit der Ausnahme, dass Shadermodell 4 die Features in ShaderModell 1 nicht unterstützt.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d90444aff674ce876f19f02f21104dd7e42143de5926ba068bbe2c49f427fdde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725887"
---
# <a name="shader-model-4"></a>Shadermodell 4

Shadermodell 4 ist eine Obermenge der Funktionen in [ShaderModell 3,](dx-graphics-hlsl-sm3.md)mit der Ausnahme, dass Shadermodell 4 die Features in ShaderModell 1 nicht unterstützt. Es wurde mit einem Common Shader-Kern entworfen, der allen programmierbaren Shadern, die nur mit HLSL programmierbar sind, einen gemeinsamen Satz von Features bietet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feature</th>
<th>Funktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Instruktionssatz</td>
<td><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL-Funktionen</strong></a></td>
</tr>
<tr class="even">
<td>Registrieren von Set</td>
<td>Auf den Registersatz kann über Member in Konstanten- und Texturpuffern zugegriffen werden, indem die HLSL-Semantik für Dinge wie das Packen von Komponenten verwendet wird.
<ul>
<li>Pixelshaderregister (siehe Register – <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">ps_4_0</a> und Register <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">– ps_4_1</a>)</li>
<li>Vertex-Shaderregister (siehe <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Register – vs_4_0</a> und Register – <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">vs_4_1</a>)</li>
<li>Geometry-Shaderregister (siehe <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Register – gs_4_0</a> und Register – <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex-Shader max</td>
<td>Keine Einschränkung</td>
</tr>
<tr class="even">
<td>Max. Pixel-Shader</td>
<td>Keine Einschränkung</td>
</tr>
<tr class="odd">
<td>Neue Shaderprofile hinzugefügt</td>
<td>gs_4_0, ps_4_0, vs_4_0,*gs_4_1, ps_4_1,* gs_4_1*</td>
</tr>
<tr class="even">
<td>Neues Effect-Framework-Profil hinzugefügt</td>
<td>fx_4_0, fx_4_1*</td>
</tr>
</tbody>
</table>



 

\* – gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1 und fx \_ 4 \_ 1 werden unter Direct3D 10.1 oder höher unterstützt.

ShaderModell 4 unterstützt eine neue Pipelinephase – die geometry-shader-Phase –, die zum Erstellen oder Ändern vorhandener Geometrie verwendet werden kann. Es enthält auch zwei neue Objekttypen: ein Stream-Output-Objekt, das für das Streamen von Daten aus der Geometriephase entwickelt wurde, und ein Texturobjekt mit Vorlagen, das Textursamplingfunktionen implementiert.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Konstanten](dx-graphics-hlsl-constants.md)
-   [Geometry-Shader-Objekt](dx-graphics-hlsl-geometry-shader.md)
-   [Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
-   [Texturobjekt](dx-graphics-hlsl-to-type.md)

Shadermodell 4 unterstützt Komprimierungsregeln, die vorgeben, wie eng Daten beim Speichern angeordnet werden können. Diese Regeln werden unter [Komprimierungsregeln für konstante Variablen](dx-graphics-hlsl-packing-rules.md) beschrieben.

Im Abschnitt [ShaderModell 4-Assembly](dx-graphics-hlsl-sm4-asm.md) werden die Assemblyanweisungen beschrieben, die von Shadermodell 4 und Shadermodell 4.1 unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleich von Shadermodellen und Shaderprofilen](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




