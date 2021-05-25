---
description: Texturfilterkonst konstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343085"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="82d8d-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="82d8d-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="82d8d-104">Texturfilterkonst konstanten.</span><span class="sxs-lookup"><span data-stu-id="82d8d-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82d8d-105">#Definieren</span><span class="sxs-lookup"><span data-stu-id="82d8d-105">#define</span></span></td>
<td><span data-ttu-id="82d8d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82d8d-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="82d8d-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="82d8d-108">Das Gerät unterstützt monotone Konvolutionsfilterung.</span><span class="sxs-lookup"><span data-stu-id="82d8d-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="82d8d-109">Dieser Filter wird durch den D3DTEXF_CONVOLUTIONMONO des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82d8d-110">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="82d8d-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="82d8d-111">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82d8d-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="82d8d-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="82d8d-113">Das Gerät unterstützt die punktbasierte Stichprobenfilterung pro Stufe für die Vergrößerung von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="82d8d-114">Der Punktbeispiel-Vergrößerungsfilter wird durch den D3DTEXF_POINT des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="82d8d-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="82d8d-116">Das Gerät unterstützt die mehrstufige bilineare Interpolationsfilterung für die Vergrößerung von Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="82d8d-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="82d8d-117">Der mipmapping-Filter für die bilineare Interpolation wird durch den D3DTEXF_LINEAR des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="82d8d-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="82d8d-119">Das Gerät unterstützt die phasenbasierte anisotrope Filterung für die Vergrößerung von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="82d8d-120">Der anisotrope Vergrößerungsfilter wird durch den D3DTEXF_ANISOTROPIC des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="82d8d-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="82d8d-122">Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe zum Vergrößern von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="82d8d-123">Der pyramidale Lupenfilter wird durch den D3DTEXF_PYRAMIDALQUAD Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="82d8d-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="82d8d-125">Das Gerät unterstützt die Pro-Stage-Filterung von Gaußschen Quadern zum Vergrößern von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="82d8d-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="82d8d-127">Das Gerät unterstützt die Punktsamplingfilterung pro Phase, um Texturen zu verminen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="82d8d-128">Der Point-Sample-Minderfilter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="82d8d-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="82d8d-130">Das Gerät unterstützt die lineare Filterung pro Stufe zum Verminen von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="82d8d-131">Der lineare Minderungsfilter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="82d8d-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="82d8d-133">Das Gerät unterstützt die phasenspezifische Anisotrope Filterung für die Vergrößerung von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="82d8d-134">Der Filter für die anisotrope Minification wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="82d8d-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="82d8d-136">Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe, um Texturen zu verminen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="82d8d-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="82d8d-138">Das Gerät unterstützt die Pro-Stage-Filterung von Gaußschen Quadern zum Verminen von Texturen.</span><span class="sxs-lookup"><span data-stu-id="82d8d-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d8d-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="82d8d-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="82d8d-140">Das Gerät unterstützt die Punktbeispielfilterung pro Phase für Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="82d8d-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="82d8d-141">Der point-sample mipmapping-Filter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d8d-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="82d8d-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="82d8d-143">Das Gerät unterstützt die mehrstufige bilineare Interpolationsfilterung für Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="82d8d-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="82d8d-144">Der mipmapping-Filter für die bilineare Interpolation wird durch den D3DTEXF_LINEAR des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d8d-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82d8d-145">Diese Konstanten werden von TextureFilterCaps-, CubeTextureFilterCaps-, VolumeTextureFilterCaps- und VertexTextureFilterCaps-Membern von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="82d8d-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="82d8d-146">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="82d8d-146">Constant Information</span></span>



|  <span data-ttu-id="82d8d-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82d8d-147">Requirement</span></span>                        | <span data-ttu-id="82d8d-148">Wert</span><span class="sxs-lookup"><span data-stu-id="82d8d-148">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="82d8d-149">Header</span><span class="sxs-lookup"><span data-stu-id="82d8d-149">Header</span></span>                   | <span data-ttu-id="82d8d-150">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="82d8d-150">d3d9caps.h</span></span> |
| <span data-ttu-id="82d8d-151">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="82d8d-151">Minimum operating system</span></span> | <span data-ttu-id="82d8d-152">Windows 98</span><span class="sxs-lookup"><span data-stu-id="82d8d-152">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82d8d-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82d8d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d8d-154">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="82d8d-154">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
