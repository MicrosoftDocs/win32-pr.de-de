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
# <a name="shader-model-2"></a><span data-ttu-id="08085-103">Shadermodell 2</span><span class="sxs-lookup"><span data-stu-id="08085-103">Shader Model 2</span></span>

<span data-ttu-id="08085-104">Shader Model 2 hat [Shader Model 1](dx-graphics-hlsl-sm1.md)zusätzliche Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="08085-104">Shader Model 2 added additional capabilities to [shader model 1](dx-graphics-hlsl-sm1.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08085-105">Feature</span><span class="sxs-lookup"><span data-stu-id="08085-105">Feature</span></span></td>
<td><span data-ttu-id="08085-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="08085-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08085-107">Instruktionssatz</span><span class="sxs-lookup"><span data-stu-id="08085-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="08085-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL-Funktionen</strong></a></span><span class="sxs-lookup"><span data-stu-id="08085-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="08085-109">Assemblyanweisungen (siehe <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Anweisungen-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instructions-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">PS_2_0 Anweisungen</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Anweisungen</a>)</span><span class="sxs-lookup"><span data-stu-id="08085-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08085-110">Register Satz</span><span class="sxs-lookup"><span data-stu-id="08085-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="08085-111">Pixel-Shader-Register (siehe <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">PS_2_0 Register</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Register</a>)</span><span class="sxs-lookup"><span data-stu-id="08085-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</span></span></li>
<li><span data-ttu-id="08085-112">Vertex-Shader-Register (siehe <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Register-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Register vs_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="08085-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registers - vs_2_x</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08085-113">Pixel-Shader max.</span><span class="sxs-lookup"><span data-stu-id="08085-113">Pixel Shader Max</span></span></td>
<td><ul>
<li><span data-ttu-id="08085-114">PS_2_0-32 Textur + 64 Arithmetik</span><span class="sxs-lookup"><span data-stu-id="08085-114">ps_2_0 - 32 texture + 64 arithmetic</span></span></li>
<li><span data-ttu-id="08085-115">ps_2_x-96 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. D3DPSHADERCAPS2_0. numinstructionslots.</span><span class="sxs-lookup"><span data-stu-id="08085-115">ps_2_x - 96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2_0.NumInstructionSlots.</span></span> <span data-ttu-id="08085-116">Siehe D3DPSHADERCAPS2_0</span><span class="sxs-lookup"><span data-stu-id="08085-116">See D3DPSHADERCAPS2_0</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08085-117">Vertex-Shader Max</span><span class="sxs-lookup"><span data-stu-id="08085-117">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="08085-118">256-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="08085-118">256 instructions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08085-119">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="08085-119">Shader Profiles</span></span></td>
<td><span data-ttu-id="08085-120">PS_2_0, ps_2_x VS_2_0, vs_2_x</span><span class="sxs-lookup"><span data-stu-id="08085-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="08085-121">Weitere Informationen zum Shader-Modell 2 finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="08085-121">For more details on shader model 2, see:</span></span>

-   <span data-ttu-id="08085-122">[Pixel-Shader 2,0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel-Shader 2. x](dx9-graphics-reference-asm-ps-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="08085-122">[Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)</span></span>
-   <span data-ttu-id="08085-123">[Vertex-Shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex-Shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="08085-123">[Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="08085-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08085-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08085-125">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="08085-125">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




