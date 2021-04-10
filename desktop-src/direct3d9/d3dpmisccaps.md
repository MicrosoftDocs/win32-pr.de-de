---
description: Verschiedene Treiber primitive funktionsflags.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214238"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="f17c9-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="f17c9-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="f17c9-104">Verschiedene Treiber primitive funktionsflags.</span><span class="sxs-lookup"><span data-stu-id="f17c9-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f17c9-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="f17c9-105">#define</span></span></td>
<td><span data-ttu-id="f17c9-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f17c9-106">Value</span></span></td>
<td><span data-ttu-id="f17c9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f17c9-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="f17c9-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="f17c9-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="f17c9-109">0x00000002L</span></span></td>
<td><span data-ttu-id="f17c9-110">Das Gerät kann die Änderung des tiefen Puffers bei Pixel Vorgängen aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f17c9-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="f17c9-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="f17c9-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="f17c9-112">0x00000010L</span></span></td>
<td><span data-ttu-id="f17c9-113">Der Treiber führt keine Dreiecks Berechnung durch.</span><span class="sxs-lookup"><span data-stu-id="f17c9-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="f17c9-114">Dies entspricht dem D3DCULL_NONE-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="f17c9-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="f17c9-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="f17c9-116">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="f17c9-116">0x00000020L</span></span></td>
<td><span data-ttu-id="f17c9-117">Der Treiber unterstützt die Dreiecks Berechnung im Uhrzeigersinn durch den D3DRS_CULLMODE Zustand.</span><span class="sxs-lookup"><span data-stu-id="f17c9-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="f17c9-118">(Dies gilt nur für Dreiecks primitive.) Dieses Flag entspricht dem D3DCULL_CW-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="f17c9-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="f17c9-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="f17c9-120">0x00000040l</span><span class="sxs-lookup"><span data-stu-id="f17c9-120">0x00000040L</span></span></td>
<td><span data-ttu-id="f17c9-121">Der Treiber unterstützt gegen den Uhrzeigersinn im Uhrzeigersinn durch den D3DRS_CULLMODE Zustand.</span><span class="sxs-lookup"><span data-stu-id="f17c9-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="f17c9-122">(Dies gilt nur für Dreiecks primitive.) Dieses Flag entspricht dem D3DCULL_CCW-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="f17c9-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="f17c9-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="f17c9-124">0x00000100l</span><span class="sxs-lookup"><span data-stu-id="f17c9-124">0x00000100L</span></span></td>
<td><span data-ttu-id="f17c9-125">Das Gerät unterstützt pro-Channel-Schreibvorgänge für den Renderziel-Farb Puffer durch den D3DRS_COLORWRITEENABLE Zustand.</span><span class="sxs-lookup"><span data-stu-id="f17c9-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="f17c9-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="f17c9-127">0x00000200l</span><span class="sxs-lookup"><span data-stu-id="f17c9-127">0x00000200L</span></span></td>
<td><span data-ttu-id="f17c9-128">Das Gerät schneidet skalierte Punkte mit einer Größe von mehr als 1,0 auf benutzerdefinierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="f17c9-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="f17c9-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="f17c9-130">0x00000200l</span><span class="sxs-lookup"><span data-stu-id="f17c9-130">0x00000200L</span></span></td>
<td><span data-ttu-id="f17c9-131">Geräte Clips nach umgewandelten Scheitel Punkten.</span><span class="sxs-lookup"><span data-stu-id="f17c9-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="f17c9-132">Geben Sie D3DUSAGE_DONOTCLIP an, wenn die Pipeline kein Clipping durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="f17c9-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="f17c9-133">In diesem Fall muss möglicherweise zur zeichnungszeit ein zusätzliches Software Clipping durchgeführt werden, sodass der Vertex-Puffer sich im Systemspeicher befinden muss.</span><span class="sxs-lookup"><span data-stu-id="f17c9-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="f17c9-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="f17c9-135">0x00000400l</span><span class="sxs-lookup"><span data-stu-id="f17c9-135">0x00000400L</span></span></td>
<td><span data-ttu-id="f17c9-136">Das Gerät unterstützt <a href="d3dta.md">D3DTA</a> für ein temporäres Register.</span><span class="sxs-lookup"><span data-stu-id="f17c9-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="f17c9-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="f17c9-138">0x00000800l</span><span class="sxs-lookup"><span data-stu-id="f17c9-138">0x00000800L</span></span></td>
<td><span data-ttu-id="f17c9-139">Das Gerät unterstützt andere Alpha-Mischungs Vorgänge als D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="f17c9-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="f17c9-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="f17c9-141">0x00000100l</span><span class="sxs-lookup"><span data-stu-id="f17c9-141">0x00000100L</span></span></td>
<td><span data-ttu-id="f17c9-142">Ein Referenzgerät, das nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f17c9-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="f17c9-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="f17c9-144">0x00004000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-144">0x00004000L</span></span></td>
<td><span data-ttu-id="f17c9-145">Das Gerät unterstützt unabhängige Schreib Masken für mehrere Element Texturen oder mehrere Renderingziele.</span><span class="sxs-lookup"><span data-stu-id="f17c9-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="f17c9-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="f17c9-147">0x00008000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-147">0x00008000L</span></span></td>
<td><span data-ttu-id="f17c9-148">Das Gerät unterstützt stufenübergreifende Konstanten.</span><span class="sxs-lookup"><span data-stu-id="f17c9-148">Device supports per-stage constants.</span></span> <span data-ttu-id="f17c9-149">Siehe D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f17c9-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="f17c9-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="f17c9-151">0x00200000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-151">0x00200000L</span></span></td>
<td><span data-ttu-id="f17c9-152">Das Gerät unterstützt nach dem mischen die Konvertierung in sRGB.</span><span class="sxs-lookup"><span data-stu-id="f17c9-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f17c9-153">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="f17c9-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="f17c9-154">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f17c9-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="f17c9-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="f17c9-156">0x00010000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-156">0x00010000L</span></span></td>
<td><span data-ttu-id="f17c9-157">Das Gerät unterstützt separate Nebel-und Glanz alpha.</span><span class="sxs-lookup"><span data-stu-id="f17c9-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="f17c9-158">Viele Geräte verwenden den Glanz Alphakanal, um den Nebel Faktor zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f17c9-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="f17c9-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="f17c9-160">0x00020000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-160">0x00020000L</span></span></td>
<td><span data-ttu-id="f17c9-161">Das Gerät unterstützt separate Blend-Einstellungen für den Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="f17c9-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="f17c9-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="f17c9-163">0x00040000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-163">0x00040000L</span></span></td>
<td><span data-ttu-id="f17c9-164">Das Gerät unterstützt verschiedene Bits-tiefen für mehrere Renderziele.</span><span class="sxs-lookup"><span data-stu-id="f17c9-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f17c9-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="f17c9-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="f17c9-166">0x00080000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-166">0x00080000L</span></span></td>
<td><span data-ttu-id="f17c9-167">Das Gerät unterstützt Post-Pixel-Shader-Vorgänge für mehrere Renderziele.</span><span class="sxs-lookup"><span data-stu-id="f17c9-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f17c9-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="f17c9-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="f17c9-169">0x00100000l</span><span class="sxs-lookup"><span data-stu-id="f17c9-169">0x00100000L</span></span></td>
<td><span data-ttu-id="f17c9-170">Geräte Klammern blenden Sie den Faktor pro Scheitelpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="f17c9-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f17c9-171">Diese Konstanten werden vom primitivefehlcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f17c9-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="f17c9-172">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="f17c9-172">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f17c9-173">Header</span><span class="sxs-lookup"><span data-stu-id="f17c9-173">Header</span></span>                   | <span data-ttu-id="f17c9-174">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="f17c9-174">d3d9caps.h</span></span> |
| <span data-ttu-id="f17c9-175">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f17c9-175">Minimum operating system</span></span> | <span data-ttu-id="f17c9-176">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f17c9-176">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f17c9-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f17c9-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f17c9-178">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f17c9-178">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
