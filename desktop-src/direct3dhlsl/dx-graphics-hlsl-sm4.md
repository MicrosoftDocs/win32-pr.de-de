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
# <a name="shader-model-4"></a><span data-ttu-id="5c5f1-103">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5c5f1-103">Shader Model 4</span></span>

<span data-ttu-id="5c5f1-104">Shadermodell 4 ist eine supermenge der Funktionen in [Shader Model 3](dx-graphics-hlsl-sm3.md), mit dem Unterschied, dass Shader Model 4 die Funktionen in Shader Model 1 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="5c5f1-105">Es wurde mithilfe eines gemeinsamen Shader-Kerns entworfen, der allen programmierbaren Shadern eine Reihe allgemeiner Features bietet, die nur mit HLSL programmierbar sind.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c5f1-106">Feature</span><span class="sxs-lookup"><span data-stu-id="5c5f1-106">Feature</span></span></th>
<th><span data-ttu-id="5c5f1-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="5c5f1-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c5f1-108">Instruktionssatz</span><span class="sxs-lookup"><span data-stu-id="5c5f1-108">Instruction Set</span></span></td>
<td><span data-ttu-id="5c5f1-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL-Funktionen</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c5f1-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c5f1-110">Register Satz</span><span class="sxs-lookup"><span data-stu-id="5c5f1-110">Register Set</span></span></td>
<td><span data-ttu-id="5c5f1-111">Der Register Satz kann über Member in Konstanten-und Textur Puffern mit HLSL-Semantik für Elemente wie Komponenten Verpackung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="5c5f1-112">Pixel-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Register-ps_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Register-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="5c5f1-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="5c5f1-113">Vertex-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Register-vs_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Register-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="5c5f1-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="5c5f1-114">Geometry-Shader-Register (siehe <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Register-gs_4_0</a> und <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Register-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="5c5f1-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c5f1-115">Vertex-Shader Max</span><span class="sxs-lookup"><span data-stu-id="5c5f1-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="5c5f1-116">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="5c5f1-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c5f1-117">Pixel-Shader max.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="5c5f1-118">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="5c5f1-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c5f1-119">Neue shaderprofile hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="5c5f1-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="5c5f1-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="5c5f1-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c5f1-121">Neues Effect-Framework Profil hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="5c5f1-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="5c5f1-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="5c5f1-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5c5f1-123">\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 und FX \_ 4 \_ 1 werden auf Direct3D 10,1 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="5c5f1-124">Shadermodell 4 unterstützt eine neue Pipeline Stufe – die Geometry-Shader-Stufe –, die zum Erstellen oder Ändern vorhandener Geometrie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="5c5f1-125">Sie enthält auch zwei neue Objekttypen: ein Stream-Output-Objekt, das für das Streamen von Daten aus der Geometrie Phase konzipiert wurde, und ein auf Vorlagen basiertes Textur Objekt, das Textur-Samplings implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="5c5f1-126">Common-Shader-Kern</span><span class="sxs-lookup"><span data-stu-id="5c5f1-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="5c5f1-127">Konstanten</span><span class="sxs-lookup"><span data-stu-id="5c5f1-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="5c5f1-128">Geometry-Shader-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c5f1-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="5c5f1-129">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c5f1-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="5c5f1-130">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c5f1-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="5c5f1-131">Shadermodell 4 unterstützt Verpackungs Regeln, mit denen festgelegt wird, wie eng Daten beim Speichern angeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="5c5f1-132">Diese Regeln werden in [Verpackungs Regeln für konstante Variablen](dx-graphics-hlsl-packing-rules.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="5c5f1-133">Im Abschnitt [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) werden die Assemblyanweisungen beschrieben, die das Shadermodell 4 und das Shader-Modell 4,1 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c5f1-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c5f1-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c5f1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c5f1-135">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="5c5f1-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




