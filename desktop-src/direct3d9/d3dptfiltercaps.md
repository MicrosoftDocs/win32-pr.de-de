---
description: Textur Filter Konstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041520"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="34648-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="34648-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="34648-104">Textur Filter Konstanten.</span><span class="sxs-lookup"><span data-stu-id="34648-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34648-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="34648-105">#define</span></span></td>
<td><span data-ttu-id="34648-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34648-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="34648-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="34648-108">Das Gerät unterstützt das Chrome-filtern.</span><span class="sxs-lookup"><span data-stu-id="34648-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="34648-109">Dieser Filter wird durch den D3DTEXF_CONVOLUTIONMONO Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34648-110">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="34648-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="34648-111">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34648-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="34648-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="34648-113">Das Gerät unterstützt die Stichproben Filterung pro Phase für Lupen Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="34648-114">Der Filter für die Punkt-Stichproben Vergrößerung wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="34648-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="34648-116">Das Gerät unterstützt die pro-Phase-bilineare Interpolations Filterung für lupmaps.</span><span class="sxs-lookup"><span data-stu-id="34648-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="34648-117">Der bilineare Interpolations-Mipmapping-Filter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="34648-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="34648-119">Das Gerät unterstützt die pro-Phase-anisotrope Filterung für Lupen Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="34648-120">Der anisotrope Vergrößerungs Filter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="34648-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="34648-122">Das Gerät unterstützt eine einstufige, pyramidenförmige Beispiel Filterung für Lupen Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="34648-123">Der pyramidenförmige Lupen Filter wird durch den D3DTEXF_PYRAMIDALQUAD Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="34648-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="34648-125">Das Gerät unterstützt das pro-Phase-Gaußsche Quad-Filtern für Lupen.</span><span class="sxs-lookup"><span data-stu-id="34648-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="34648-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="34648-127">Das Gerät unterstützt die phasenweise-Stichproben Filterung zum Minimieren von Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="34648-128">Der Punkt-Sample-minierationsfilter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="34648-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="34648-130">Das Gerät unterstützt das stufenweise lineare Filtern zum Minimieren von Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="34648-131">Der lineare minierationsfilter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="34648-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="34648-133">Das Gerät unterstützt die pro-Phase-anisotrope Filterung zum Minimieren von Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="34648-134">Der anisotrope Minimierung-Filter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="34648-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="34648-136">Das Gerät unterstützt eine einstufige, pyramidenförmige Beispiel Filterung für das Minimieren von Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="34648-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="34648-138">Das Gerät unterstützt die stufenweise gausische Quad-Filterung für das Minimieren von Texturen.</span><span class="sxs-lookup"><span data-stu-id="34648-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34648-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="34648-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="34648-140">Das Gerät unterstützt eine pro-Phase-Punkt-Beispiel Filterung für Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="34648-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="34648-141">Der "Point-Sample Mipmapping"-Filter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34648-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="34648-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="34648-143">Das Gerät unterstützt die pro-Phase-bilineare Interpolations Filterung für Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="34648-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="34648-144">Der bilineare Interpolations-Mipmapping-Filter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34648-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="34648-145">Diese Konstanten werden von den Elementen TextureFilterCaps, cubetexturefiltercaps, volumetexturefiltercaps und vertextexturefiltercaps von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="34648-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="34648-146">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="34648-146">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="34648-147">Header</span><span class="sxs-lookup"><span data-stu-id="34648-147">Header</span></span>                   | <span data-ttu-id="34648-148">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="34648-148">d3d9caps.h</span></span> |
| <span data-ttu-id="34648-149">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="34648-149">Minimum operating system</span></span> | <span data-ttu-id="34648-150">Windows 98</span><span class="sxs-lookup"><span data-stu-id="34648-150">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34648-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34648-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34648-152">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="34648-152">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
