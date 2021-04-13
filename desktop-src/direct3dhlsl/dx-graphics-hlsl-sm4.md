---
title: Shadermodell 4
description: Shadermodell 4 ist eine supermenge der Funktionen in Shader Model 3, mit dem Unterschied, dass Shader Model 4 die Funktionen in Shader Model 1 nicht unterstützt.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389782"
---
# <a name="shader-model-4"></a>Shadermodell 4

Shadermodell 4 ist eine supermenge der Funktionen in [Shader Model 3](dx-graphics-hlsl-sm3.md), mit dem Unterschied, dass Shader Model 4 die Funktionen in Shader Model 1 nicht unterstützt. Es wurde mithilfe eines gemeinsamen Shader-Kerns entworfen, der allen programmierbaren Shadern eine Reihe allgemeiner Features bietet, die nur mit HLSL programmierbar sind.



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
<td>Register Satz</td>
<td>Der Register Satz kann über Member in Konstanten-und Textur Puffern mit HLSL-Semantik für Elemente wie Komponenten Verpackung aufgerufen werden.
<ul>
<li>Pixel-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Register-ps_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Register-ps_4_1</a>)</li>
<li>Vertex-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Register-vs_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Register-vs_4_1</a>)</li>
<li>Geometry-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Register-gs_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Register-gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex-Shader Max</td>
<td>Keine Einschränkung</td>
</tr>
<tr class="even">
<td>Pixel-Shader max.</td>
<td>Keine Einschränkung</td>
</tr>
<tr class="odd">
<td>Neue shaderprofile hinzugefügt</td>
<td>gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 *</td>
</tr>
<tr class="even">
<td>Neues Effect-Framework Profil hinzugefügt</td>
<td>fx_4_0, fx_4_1 *</td>
</tr>
</tbody>
</table>



 

\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 und FX \_ 4 \_ 1 werden auf Direct3D 10,1 oder höher unterstützt.

Shadermodell 4 unterstützt eine neue Pipeline Stufe – die Geometry-Shader-Stufe –, die zum Erstellen oder Ändern vorhandener Geometrie verwendet werden kann. Sie enthält auch zwei neue Objekttypen: ein Stream-Output-Objekt, das für das Streamen von Daten aus der Geometrie Phase konzipiert wurde, und ein auf Vorlagen basiertes Textur Objekt, das Textur-Samplings implementiert.

-   [Common-Shader-Kern](dx-graphics-hlsl-common-core.md)
-   [Konstanten](dx-graphics-hlsl-constants.md)
-   [Geometry-Shader-Objekt](dx-graphics-hlsl-geometry-shader.md)
-   [Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
-   [Texture-Objekt](dx-graphics-hlsl-to-type.md)

Shadermodell 4 unterstützt Verpackungs Regeln, mit denen festgelegt wird, wie eng Daten beim Speichern angeordnet werden können. Diese Regeln werden in [Verpackungs Regeln für konstante Variablen](dx-graphics-hlsl-packing-rules.md) beschrieben.

Im Abschnitt [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) werden die Assemblyanweisungen beschrieben, die das Shadermodell 4 und das Shader-Modell 4,1 unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




