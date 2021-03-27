---
title: Shader-Modell 3
description: Shader Model 3 hat Shader Model 2 zusätzliche Funktionen hinzugefügt.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391109"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader-Modell 3 (HLSL-Referenz)

Shader Model 3 hat [Shader Model 2](dx-graphics-hlsl-sm2.md)zusätzliche Funktionen hinzugefügt.



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
<li>Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Anweisungen</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Anweisungen vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Register Satz</td>
<td><ul>
<li>Pixel-Shader-Register (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Register</a>)</li>
<li>Vertex-Shader-Register (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Register-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel-Shader max.</td>
<td>512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxPixelShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Vertex-Shader Max</td>
<td>512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxVertexShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Shaderprofile</td>
<td>ps_3_0 vs_3_0</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu den Shader von Model 3 finden Sie unter:

-   [Pixel-Shader 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Vertex-Shader 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 