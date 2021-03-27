---
title: Angeben von compilerzielen
description: Hier werden die Ziele für verschiedene Profile aufgelistet, die von den D3DCompile \-Funktionen und vom HLSL-Compiler unterstützt werden.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390952"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="cbc8b-103">Angeben von compilerzielen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="cbc8b-104">Sie müssen den Shader-Ziel – Satz von Shader-Funktionen – angeben, die beim Aufrufen der Funktion [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)oder [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) kompiliert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="cbc8b-105">Hier werden die Ziele für verschiedene Profile aufgelistet, die von den **D3DCompile \*** -Funktionen und dem HLSL-Compiler unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="cbc8b-106">Direct3D 11,0-und 11,1-Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="cbc8b-107">Direct3D 10,1-Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="cbc8b-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="cbc8b-108">Direct3D 10,0-Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="cbc8b-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="cbc8b-109">Direct3D-featureebenen der 9,1, 9,2 und 9,3</span><span class="sxs-lookup"><span data-stu-id="cbc8b-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="cbc8b-110">Legacy Direct3D 9-Shader-Modell 3,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="cbc8b-111">Legacy Direct3D 9-Shader-Modell 2,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="cbc8b-112">Legacy Direct3D 9-Shader-Modell 1. x</span><span class="sxs-lookup"><span data-stu-id="cbc8b-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="cbc8b-113">Ältere Effekte</span><span class="sxs-lookup"><span data-stu-id="cbc8b-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="cbc8b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbc8b-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="cbc8b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="cbc8b-116">Direct3D 11,0-und 11,1-Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="cbc8b-117">Im folgenden sind die Shader-Ziele aufgeführt, die von 11,1 11,0 [Direct3D unterstützt](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) werden.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="cbc8b-118">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-118">Target</span></span>   | <span data-ttu-id="cbc8b-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-120">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-120">cs\_5\_0</span></span> | <span data-ttu-id="cbc8b-121">DirectCompute 5,0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="cbc8b-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-122">ds\_5\_0</span></span> | [<span data-ttu-id="cbc8b-123">Domänen-Shader</span><span class="sxs-lookup"><span data-stu-id="cbc8b-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="cbc8b-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-124">gs\_5\_0</span></span> | <span data-ttu-id="cbc8b-125">[Geometry-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="cbc8b-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-126">hs\_5\_0</span></span> | [<span data-ttu-id="cbc8b-127">Rumpf-Shader</span><span class="sxs-lookup"><span data-stu-id="cbc8b-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="cbc8b-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-128">ps\_5\_0</span></span> | <span data-ttu-id="cbc8b-129">[Pixel-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="cbc8b-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-130">vs\_5\_0</span></span> | <span data-ttu-id="cbc8b-131">[Vertex-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="cbc8b-132">Direct3D 10,1-Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="cbc8b-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="cbc8b-133">Dies sind die shaderziele, die von der Direct3D 10,1- [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="cbc8b-134">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-134">Target</span></span>   | <span data-ttu-id="cbc8b-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-136">CS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-136">cs\_4\_1</span></span> | <span data-ttu-id="cbc8b-137">DirectCompute 4,1 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="cbc8b-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="cbc8b-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-138">gs\_4\_1</span></span> | <span data-ttu-id="cbc8b-139">[Geometry-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="cbc8b-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-140">ps\_4\_1</span></span> | <span data-ttu-id="cbc8b-141">[Pixel-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="cbc8b-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-142">vs\_4\_1</span></span> | <span data-ttu-id="cbc8b-143">[Vertex-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="cbc8b-144">Direct3D 10,0-Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="cbc8b-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="cbc8b-145">Dies sind die shaderziele, die von der Direct3D 10,0- [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="cbc8b-146">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-146">Target</span></span>   | <span data-ttu-id="cbc8b-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-148">CS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-148">cs\_4\_0</span></span> | <span data-ttu-id="cbc8b-149">DirectCompute 4,0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="cbc8b-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="cbc8b-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-150">gs\_4\_0</span></span> | <span data-ttu-id="cbc8b-151">[Geometry-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="cbc8b-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-152">ps\_4\_0</span></span> | <span data-ttu-id="cbc8b-153">[Pixel-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="cbc8b-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-154">vs\_4\_0</span></span> | <span data-ttu-id="cbc8b-155">[Vertex-Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc8b-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="cbc8b-156">Direct3D-featureebenen der 9,1, 9,2 und 9,3</span><span class="sxs-lookup"><span data-stu-id="cbc8b-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="cbc8b-157">Im folgenden sind die Shader-Ziele aufgeführt, die die [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 und 9,3 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="cbc8b-158">Wenn Sie die \* \_ \_ HLSL-Shader-Profile der 4 0- \_ Ebene \_ 9 \_ x verwenden, verwenden Sie implizit die [Shader Model 2. x](dx-graphics-hlsl-sm2.md) -Profile zur Unterstützung von Direct3D 9-fähiger Hardware.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="cbc8b-159">Shader Model 2. x-Profile unterstützen ein eingeschränktes Verhalten der Fluss Steuerung als das [Shader-Modell 4. x](dx-graphics-hlsl-sm4.md) und spätere Profile.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbc8b-160">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-160">Target</span></span></th>
<th><span data-ttu-id="cbc8b-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbc8b-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="cbc8b-163">[Pixelshader](/previous-versions//bb205146(v=vs.85)) für 9,1 und 9,2 (ähnliche Grenzwerte wie PS_2_0)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="cbc8b-164">64 arithmetische und 32 Textur Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="cbc8b-165">12 temporäre Register</span><span class="sxs-lookup"><span data-stu-id="cbc8b-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="cbc8b-166">4 Ebenen von abhängigen Lesevorgängen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbc8b-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="cbc8b-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="cbc8b-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel-Shader</a> für 9,3 (ähnliche Grenzwerte für ps_2_x ² mit zusätzlichen shaderfeatures)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="cbc8b-169">512-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-169">512 instructions</span></span></li>
<li><span data-ttu-id="cbc8b-170">32 temporäre Register</span><span class="sxs-lookup"><span data-stu-id="cbc8b-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="cbc8b-171">Statische Fluss Steuerung (maximale Tiefe von 4)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="cbc8b-172">Dynamische Fluss Steuerung (maximale Tiefe von 24)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="cbc8b-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="cbc8b-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="cbc8b-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="cbc8b-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="cbc8b-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="cbc8b-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="cbc8b-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="cbc8b-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="cbc8b-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="cbc8b-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbc8b-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="cbc8b-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9,1 und 9,2 (ähnlich wie VS_2_0)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="cbc8b-180">256-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-180">256 instructions</span></span></li>
<li><span data-ttu-id="cbc8b-181">12 temporäre Register</span><span class="sxs-lookup"><span data-stu-id="cbc8b-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="cbc8b-182">Statische Fluss Steuerung (maximale Tiefe von 1)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbc8b-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="cbc8b-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="cbc8b-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9,3 (ähnlich wie vs_2_a ² mit zusätzlichen shaderfeatures und Instanziierung)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="cbc8b-185">256-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-185">256 instructions</span></span></li>
<li><span data-ttu-id="cbc8b-186">32 temporäre Register</span><span class="sxs-lookup"><span data-stu-id="cbc8b-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="cbc8b-187">Statische Fluss Steuerung (maximale Tiefe von 4)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="cbc8b-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="cbc8b-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="cbc8b-189">Legacy Direct3D 9-Shader-Modell 3,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="cbc8b-190">Im folgenden finden Sie die Shader-Ziele für das Legacy-Direct3D 9-Shader-Modell 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="cbc8b-191">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-191">Target</span></span>    | <span data-ttu-id="cbc8b-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-193">ps\_3\_0</span></span>  | <span data-ttu-id="cbc8b-194">[Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="cbc8b-195">PS \_ 3 ( \_ SW)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-195">ps\_3\_sw</span></span> | <span data-ttu-id="cbc8b-196">[Pixelshader](/previous-versions//bb205146(v=vs.85)) 3,0 (Software)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="cbc8b-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-197">vs\_3\_0</span></span>  | <span data-ttu-id="cbc8b-198">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="cbc8b-199">vs \_ 3- \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbc8b-199">vs\_3\_sw</span></span> | <span data-ttu-id="cbc8b-200">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3,0 (Software)</span><span class="sxs-lookup"><span data-stu-id="cbc8b-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="cbc8b-201">Legacy Direct3D 9-Shader-Modell 2,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="cbc8b-202">Im folgenden finden Sie die Shader-Ziele für das Legacy-Direct3D 9-Shader-Modell 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="cbc8b-203">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-203">Target</span></span>    | <span data-ttu-id="cbc8b-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-205">ps\_2\_0</span></span>  | <span data-ttu-id="cbc8b-206">[Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="cbc8b-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="cbc8b-207">ps\_2\_a</span></span>  | <span data-ttu-id="cbc8b-208">[Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="cbc8b-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="cbc8b-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="cbc8b-209">ps\_2\_b</span></span>  | <span data-ttu-id="cbc8b-210">[Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2B</span><span class="sxs-lookup"><span data-stu-id="cbc8b-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="cbc8b-211">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbc8b-211">ps\_2\_sw</span></span> | <span data-ttu-id="cbc8b-212">[Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2,0-Software</span><span class="sxs-lookup"><span data-stu-id="cbc8b-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="cbc8b-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-213">vs\_2\_0</span></span>  | <span data-ttu-id="cbc8b-214">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="cbc8b-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="cbc8b-215">vs\_2\_a</span></span>  | <span data-ttu-id="cbc8b-216">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="cbc8b-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="cbc8b-217">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbc8b-217">vs\_2\_sw</span></span> | <span data-ttu-id="cbc8b-218">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2,0-Software</span><span class="sxs-lookup"><span data-stu-id="cbc8b-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="cbc8b-219">Legacy Direct3D 9-Shader-Modell 1. x</span><span class="sxs-lookup"><span data-stu-id="cbc8b-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="cbc8b-220">Im folgenden sind die Shader-Ziele für das Legacy Direct3D 9-Shader-Modell 1. x ⁴ aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="cbc8b-221">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-221">Target</span></span>   | <span data-ttu-id="cbc8b-222">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc8b-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-223">tx\_1\_0</span></span> | <span data-ttu-id="cbc8b-224">Textur-Shader-Profil, das Legacy D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) und [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) verwenden</span><span class="sxs-lookup"><span data-stu-id="cbc8b-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="cbc8b-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-225">vs\_1\_1</span></span> | <span data-ttu-id="cbc8b-226">[Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="cbc8b-227">Ältere Effekte</span><span class="sxs-lookup"><span data-stu-id="cbc8b-227">Legacy Effects</span></span>

<span data-ttu-id="cbc8b-228">Im folgenden finden Sie die Wirkungs Ziele für ältere Effekte.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="cbc8b-229">Target</span><span class="sxs-lookup"><span data-stu-id="cbc8b-229">Target</span></span>   | <span data-ttu-id="cbc8b-230">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc8b-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="cbc8b-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-231">fx\_2\_0</span></span> | <span data-ttu-id="cbc8b-232">Effekte (FX) für Direct3D 9 in D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="cbc8b-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="cbc8b-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-233">fx\_4\_0</span></span> | <span data-ttu-id="cbc8b-234">Effekte (FX) für Direct3D 10,0 in d3dx10 ⁵</span><span class="sxs-lookup"><span data-stu-id="cbc8b-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="cbc8b-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbc8b-235">fx\_4\_1</span></span> | <span data-ttu-id="cbc8b-236">Effekte (FX) für Direct3D 10,1 in d3dx10 ⁵</span><span class="sxs-lookup"><span data-stu-id="cbc8b-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="cbc8b-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbc8b-237">fx\_5\_0</span></span> | <span data-ttu-id="cbc8b-238">Effekte (FX) für Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="cbc8b-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="cbc8b-239">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-239">Notes</span></span>

<span data-ttu-id="cbc8b-240">Im folgenden finden Sie einige Hinweise, die in den vorherigen Abschnitten beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="cbc8b-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="cbc8b-241">auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0-und 10,1-Geräten kann DirectCompute optional unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="cbc8b-242">Um die Unterstützung zu überprüfen, verwenden Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ Feature \_ d3d10 \_ X \_ Hardware \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="cbc8b-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="cbc8b-243">auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 ist eine Hardware erforderlich, die den Anforderungen für das [Legacy-Direct3D 9-Shader-Modell 3,0](#legacy-direct3d-9-shader-model-30)entspricht. diese Featureebene verwendet jedoch keine vs \_ 3 0- \_ oder PS \_ 3 0- \_ Ziele.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="cbc8b-244">Verwenden Sie nur Legacy-Direct3D 9-Shader-Modelle mit der Direct3D 9-API.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="cbc8b-245">Verwenden Sie stattdessen die 9. x-Profile mit der API Direct3D 10. x und 11. x.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="cbc8b-246">Die aktuellen HLSL-Shader- **D3DCompile \*** -Funktionen unterstützen keine Legacy-1. x-Pixel-Shader.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="cbc8b-247">Die letzte Version von HLSL zur Unterstützung dieser Ziele war D3DX9 in der Version vom Oktober 2006 des DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="cbc8b-248">Alle Versionen von D3DX und DirectX SDK sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="cbc8b-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="cbc8b-249">Weitere Informationen finden Sie unter [wo ist das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="cbc8b-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbc8b-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbc8b-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc8b-251">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="cbc8b-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 