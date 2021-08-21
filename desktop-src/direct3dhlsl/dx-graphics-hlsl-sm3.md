---
title: Shadermodell 3
description: Shadermodell 3 hat dem Shadermodell 2 zusätzliche Funktionen hinzugefügt.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed2d64ccfb06fc0fe50e5bd0075732c1fd9cbb70ca1e05bda5afd24cd5c5f98f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789540"
---
# <a name="shader-model-3-hlsl-reference"></a>Shadermodell 3 (HLSL-Referenz)

Shadermodell 3 hat dem [Shadermodell 2](dx-graphics-hlsl-sm2.md)zusätzliche Funktionen hinzugefügt.



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
<li>Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Anweisungen,</a> <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Anweisungen – vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Registrieren von Set</td>
<td><ul>
<li>Pixelshaderregister (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Register)</a></li>
<li>Vertex-Shaderregister (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Register – vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Max. Pixel-Shader</td>
<td>Mindestens 512 und bis zur Anzahl der Slots in D3DCAPS9. MaxPixelShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Vertex-Shader max</td>
<td>Mindestens 512 und bis zur Anzahl der Slots in D3DCAPS9. MaxVertexShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Shaderprofile</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu Shadern des Modells 3 finden Sie unter:

-   [Pixelshader 3.0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Vertex-Shader 3.0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleich von Shadermodellen und Shaderprofilen](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 