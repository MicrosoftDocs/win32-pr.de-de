---
title: Shadermodell 2
description: Shader Model 2 hat Shader Model 1 zusätzliche Funktionen hinzugefügt.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104993335"
---
# <a name="shader-model-2"></a>Shadermodell 2

Shader Model 2 hat [Shader Model 1](dx-graphics-hlsl-sm1.md)zusätzliche Funktionen hinzugefügt.



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
<li>Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Anweisungen-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instructions-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">PS_2_0 Anweisungen</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Anweisungen</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Register Satz</td>
<td><ul>
<li>Pixel-Shader-Register (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">PS_2_0 Register</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Register</a>)</li>
<li>Vertex-Shader-Register (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Register-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Register vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel-Shader max.</td>
<td><ul>
<li>PS_2_0-32 Textur + 64 Arithmetik</li>
<li>ps_2_x-96 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. D3DPSHADERCAPS2_0. numinstructionslots. Siehe D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex-Shader Max</td>
<td>256-Anweisungen</td>
</tr>
<tr class="even">
<td>Shaderprofile</td>
<td>PS_2_0, ps_2_x VS_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zum Shader-Modell 2 finden Sie unter:

-   [Pixel-Shader 2,0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel-Shader 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex-Shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex-Shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




