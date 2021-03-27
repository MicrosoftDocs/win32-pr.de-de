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
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="ade35-103">Shader-Modell 3 (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="ade35-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="ade35-104">Shader Model 3 hat [Shader Model 2](dx-graphics-hlsl-sm2.md)zusätzliche Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ade35-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ade35-105">Feature</span><span class="sxs-lookup"><span data-stu-id="ade35-105">Feature</span></span></td>
<td><span data-ttu-id="ade35-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="ade35-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ade35-107">Instruktionssatz</span><span class="sxs-lookup"><span data-stu-id="ade35-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="ade35-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL-Funktionen</strong></a></span><span class="sxs-lookup"><span data-stu-id="ade35-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="ade35-109">Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Anweisungen</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Anweisungen vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="ade35-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ade35-110">Register Satz</span><span class="sxs-lookup"><span data-stu-id="ade35-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="ade35-111">Pixel-Shader-Register (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Register</a>)</span><span class="sxs-lookup"><span data-stu-id="ade35-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="ade35-112">Vertex-Shader-Register (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Register-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="ade35-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ade35-113">Pixel-Shader max.</span><span class="sxs-lookup"><span data-stu-id="ade35-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="ade35-114">512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxPixelShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="ade35-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ade35-115">Vertex-Shader Max</span><span class="sxs-lookup"><span data-stu-id="ade35-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="ade35-116">512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxVertexShader30InstructionSlots (siehe <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="ade35-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ade35-117">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="ade35-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="ade35-118">ps_3_0 vs_3_0</span><span class="sxs-lookup"><span data-stu-id="ade35-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ade35-119">Weitere Informationen zu den Shader von Model 3 finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ade35-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="ade35-120">Pixel-Shader 3,0</span><span class="sxs-lookup"><span data-stu-id="ade35-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="ade35-121">Vertex-Shader 3,0</span><span class="sxs-lookup"><span data-stu-id="ade35-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="ade35-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ade35-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade35-123">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="ade35-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 