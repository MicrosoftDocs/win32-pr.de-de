---
description: Verschiedene primitive Treiberfunktionsflags.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343135"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="a3f39-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="a3f39-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="a3f39-104">Verschiedene primitive Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="a3f39-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3f39-105">#Definieren</span><span class="sxs-lookup"><span data-stu-id="a3f39-105">#define</span></span></td>
<td><span data-ttu-id="a3f39-106">Wert</span><span class="sxs-lookup"><span data-stu-id="a3f39-106">Value</span></span></td>
<td><span data-ttu-id="a3f39-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3f39-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="a3f39-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="a3f39-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="a3f39-109">0x00000002L</span></span></td>
<td><span data-ttu-id="a3f39-110">Das Gerät kann die Änderung des Tiefenpuffers bei Pixelvorgängen aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a3f39-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="a3f39-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="a3f39-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="a3f39-112">0x00000010L</span></span></td>
<td><span data-ttu-id="a3f39-113">Der Treiber führt kein Dreiecksculling aus.</span><span class="sxs-lookup"><span data-stu-id="a3f39-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="a3f39-114">Dies entspricht dem D3DCULL_NONE Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></span><span class="sxs-lookup"><span data-stu-id="a3f39-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="a3f39-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="a3f39-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a3f39-116">0x00000020L</span></span></td>
<td><span data-ttu-id="a3f39-117">Der Treiber unterstützt im Uhrzeigersinn dreiecksweises Culling durch D3DRS_CULLMODE Zustand.</span><span class="sxs-lookup"><span data-stu-id="a3f39-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="a3f39-118">(Dies gilt nur für Dreiecksprimitive.) Dieses Flag entspricht dem D3DCULL_CW Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></span><span class="sxs-lookup"><span data-stu-id="a3f39-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="a3f39-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="a3f39-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="a3f39-120">0x00000040L</span></span></td>
<td><span data-ttu-id="a3f39-121">Der Treiber unterstützt gegen den Uhrzeigersinn Culling durch den D3DRS_CULLMODE Zustand.</span><span class="sxs-lookup"><span data-stu-id="a3f39-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="a3f39-122">(Dies gilt nur für Dreiecksprimitive.) Dieses Flag entspricht dem D3DCULL_CCW des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></span><span class="sxs-lookup"><span data-stu-id="a3f39-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="a3f39-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="a3f39-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a3f39-124">0x00000100L</span></span></td>
<td><span data-ttu-id="a3f39-125">Das Gerät unterstützt kanalspezifische Schreibvorgänge für den Renderzielfarbpuffer über den D3DRS_COLORWRITEENABLE Zustand.</span><span class="sxs-lookup"><span data-stu-id="a3f39-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="a3f39-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="a3f39-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="a3f39-127">0x00000200L</span></span></td>
<td><span data-ttu-id="a3f39-128">Das Gerät klammern skalierte Punkte mit einer Größe von mehr als 1,0 ordnungsgemäß in benutzerdefinierte Clippingebenen ein.</span><span class="sxs-lookup"><span data-stu-id="a3f39-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="a3f39-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="a3f39-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="a3f39-130">0x00000200L</span></span></td>
<td><span data-ttu-id="a3f39-131">Geräteclips nachtransformationsbasierte Scheitelpunktprimitiven.</span><span class="sxs-lookup"><span data-stu-id="a3f39-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="a3f39-132">Geben Sie D3DUSAGE_DONOTCLIP an, wenn die Pipeline keinen Clipping durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="a3f39-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="a3f39-133">In diesem Fall müssen möglicherweise zusätzliche Softwareclips zur Zeichnenzeit ausgeführt werden, sodass sich der Scheitelpunktpuffer im Systemspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="a3f39-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="a3f39-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="a3f39-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="a3f39-135">0x00000400L</span></span></td>
<td><span data-ttu-id="a3f39-136">Das Gerät unterstützt <a href="d3dta.md">D3DTA</a> für die temporäre Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a3f39-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="a3f39-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="a3f39-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="a3f39-138">0x00000800L</span></span></td>
<td><span data-ttu-id="a3f39-139">Das Gerät unterstützt andere Alphamischungsvorgänge als D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="a3f39-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="a3f39-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="a3f39-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a3f39-141">0x00000100L</span></span></td>
<td><span data-ttu-id="a3f39-142">Ein Verweisgerät, das nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a3f39-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="a3f39-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="a3f39-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-144">0x00004000L</span></span></td>
<td><span data-ttu-id="a3f39-145">Das Gerät unterstützt unabhängige Schreibmasken für mehrere Elementtexturen oder mehrere Renderziele.</span><span class="sxs-lookup"><span data-stu-id="a3f39-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="a3f39-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="a3f39-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-147">0x00008000L</span></span></td>
<td><span data-ttu-id="a3f39-148">Das Gerät unterstützt phasenspezifische Konstanten.</span><span class="sxs-lookup"><span data-stu-id="a3f39-148">Device supports per-stage constants.</span></span> <span data-ttu-id="a3f39-149">Siehe D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a3f39-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="a3f39-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="a3f39-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-151">0x00200000L</span></span></td>
<td><span data-ttu-id="a3f39-152">Das Gerät unterstützt die Konvertierung in sRGB nach dem Mischen.</span><span class="sxs-lookup"><span data-stu-id="a3f39-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3f39-153">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a3f39-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a3f39-154">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3f39-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="a3f39-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="a3f39-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-156">0x00010000L</span></span></td>
<td><span data-ttu-id="a3f39-157">Das Gerät unterstützt separates Und-Alpha.</span><span class="sxs-lookup"><span data-stu-id="a3f39-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="a3f39-158">Viele Geräte verwenden den alphanularen Specular-Kanal, um den Faktor zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a3f39-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="a3f39-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="a3f39-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-160">0x00020000L</span></span></td>
<td><span data-ttu-id="a3f39-161">Das Gerät unterstützt separate Blend-Einstellungen für den Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="a3f39-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="a3f39-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="a3f39-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-163">0x00040000L</span></span></td>
<td><span data-ttu-id="a3f39-164">Das Gerät unterstützt unterschiedliche Bittiefen für mehrere Renderziele.</span><span class="sxs-lookup"><span data-stu-id="a3f39-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f39-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="a3f39-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="a3f39-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-166">0x00080000L</span></span></td>
<td><span data-ttu-id="a3f39-167">Das Gerät unterstützt Postpixel-Shadervorgänge für mehrere Renderziele.</span><span class="sxs-lookup"><span data-stu-id="a3f39-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f39-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="a3f39-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="a3f39-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="a3f39-169">0x00100000L</span></span></td>
<td><span data-ttu-id="a3f39-170">Das Gerät verbindet den Blendfaktor pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="a3f39-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a3f39-171">Diese Konstanten werden vom PrimitiveMiscCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3f39-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a3f39-172">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="a3f39-172">Constant Information</span></span>



| <span data-ttu-id="a3f39-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3f39-173">Requirement</span></span>                         |  <span data-ttu-id="a3f39-174">Wert</span><span class="sxs-lookup"><span data-stu-id="a3f39-174">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="a3f39-175">Header</span><span class="sxs-lookup"><span data-stu-id="a3f39-175">Header</span></span>                   | <span data-ttu-id="a3f39-176">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="a3f39-176">d3d9caps.h</span></span> |
| <span data-ttu-id="a3f39-177">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="a3f39-177">Minimum operating system</span></span> | <span data-ttu-id="a3f39-178">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a3f39-178">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a3f39-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3f39-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f39-180">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a3f39-180">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
