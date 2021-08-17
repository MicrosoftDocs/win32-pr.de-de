---
title: Shadermodell 2
description: Shader Model 2 hat shader model 1 zusätzliche Funktionen hinzugefügt.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23b4caa0e4da92e992eb0486f5a998ad7d21016dc691563f29589c5fc9ab5310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119974"
---
# <a name="shader-model-2"></a>Shadermodell 2

Shader Model 2 hat [shader model 1 zusätzliche Funktionen hinzugefügt.](dx-graphics-hlsl-sm1.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Feature</td>
<td>Funktion</td>
</tr>
<tr class="even">
<td>Instruktionssatz</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL-Funktionen</strong></a></li>
<li>Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, Instructions - <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, ps_2_x <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">Instructions</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Registersatz</td>
<td><ul>
<li>Pixel-Shaderregister (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Register</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Register )</a></li>
<li>Vertex-Shaderregister (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Register –</a>vs_2_0 , <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Register – vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Max. Pixel-Shader</td>
<td><ul>
<li>ps_2_0: 32 Texturen + 64 arithmetische</li>
<li>ps_2_x mindestens 96 und bis zur Anzahl der Slots in D3DCAPS9. D3DPSHADERCAPS2_0.NumInstructionSlots. Siehe D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex-Shader Max.</td>
<td>256-Anweisungen</td>
</tr>
<tr class="even">
<td>Shaderprofile</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu Shadermodell 2 finden Sie unter:

-   [Pixels shader 2.0,](dx9-graphics-reference-asm-ps-2-0.md) [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex-Shader 2.0,](dx9-graphics-reference-asm-vs-2-0.md) [Vertex-Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodelle im Vergleich zu Shaderprofilen](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




