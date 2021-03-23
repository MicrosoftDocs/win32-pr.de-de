---
title: Unter Berichte (Direct3D 12-Grafiken)
description: Beschreibt, wie eine Ressource in unter Ressourcen aufgeteilt wird und wie auf eine einzelne, mehrere oder ein Slice von unter Ressourcen verwiesen wird.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548696"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="88f4d-103">Unter Berichte (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="88f4d-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="88f4d-104">Beschreibt, wie eine Ressource in unter Ressourcen aufgeteilt wird und wie auf eine einzelne, mehrere oder ein Slice von unter Ressourcen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="88f4d-105">Beispiel unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88f4d-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="88f4d-106">Unter Quell Indizierung</span><span class="sxs-lookup"><span data-stu-id="88f4d-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="88f4d-107">MIP-Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="88f4d-108">Array Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="88f4d-109">Flachen Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="88f4d-110">Mehrere unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88f4d-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="88f4d-111">Subresource-APIs</span><span class="sxs-lookup"><span data-stu-id="88f4d-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="88f4d-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="88f4d-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="88f4d-113">Beispiel unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88f4d-113">Example subresources</span></span>

<span data-ttu-id="88f4d-114">Wenn eine Ressource einen Puffer enthält, enthält Sie einfach eine untergeordnete Quelle mit dem Index 0.</span><span class="sxs-lookup"><span data-stu-id="88f4d-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="88f4d-115">Wenn die Ressource eine Textur (oder ein Textur Array) enthält, ist das verweisen auf die unter Ressourcen komplexer.</span><span class="sxs-lookup"><span data-stu-id="88f4d-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="88f4d-116">Einige APIs greifen auf eine gesamte Ressource zu (z. b. die [**ID3D12GraphicsCommandList:: copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) -Methode), von denen andere auf einen Teil einer Ressource zugreifen (z. b. die [**ID3D12Resource:: Read fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) -Methode).</span><span class="sxs-lookup"><span data-stu-id="88f4d-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="88f4d-117">Die Methoden, die auf einen Teil einer Ressource zugreifen, verwenden im Allgemeinen eine Ansichts Beschreibung (z. b. die [**\_ \_ \_ SRV-Struktur D3D12 TEX2D Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ), um die unter Ressourcen anzugeben, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="88f4d-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="88f4d-118">Eine komplette Liste finden Sie im Abschnitt " [subresource-APIs](#subresource-apis) ".</span><span class="sxs-lookup"><span data-stu-id="88f4d-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="88f4d-119">Unter Quell Indizierung</span><span class="sxs-lookup"><span data-stu-id="88f4d-119">Subresource indexing</span></span>

<span data-ttu-id="88f4d-120">Um eine bestimmte untergeordnete Quelle zu indizieren, werden die MIP-Ebenen zuerst indiziert, wenn jeder Array Eintrag indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![unter Quell Indizierung](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="88f4d-122">MIP-Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-122">Mip slice</span></span>

<span data-ttu-id="88f4d-123">Ein MIP-Slice enthält eine MipMap-Ebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88f4d-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![unter Quell-MIP-Slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="88f4d-125">Array Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-125">Array slice</span></span>

<span data-ttu-id="88f4d-126">Bei einem Array von Texturen enthält jede Textur mit Mipmaps, ein Array Slice, eine Textur und alle zugehörigen MIP-Ebenen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88f4d-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![Teil Quell Array Slices](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="88f4d-128">Flachen Slice</span><span class="sxs-lookup"><span data-stu-id="88f4d-128">Plane slice</span></span>

<span data-ttu-id="88f4d-129">In der Regel werden keine planaren Formate zum Speichern von RGBA-Daten verwendet. in Fällen, in denen es sich handelt (z. b. 24 bpp RGB-Daten), kann eine Ebene das rote Bild, ein grünes Bild und ein blaues Bild darstellen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="88f4d-130">Eine Ebene ist jedoch nicht notwendigerweise eine Farbe, zwei oder mehr Farben können zu einer Ebene kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="88f4d-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="88f4d-131">In der Regel werden planare Daten für Subsampling von YCbCr-und Depth-Stencil-Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="88f4d-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="88f4d-132">Depth-Stencil ist das einzige Format, das Mipmaps, Arrays und mehrere Ebenen vollständig unterstützt (häufig Ebene 0 für Tiefe und Ebene 1 für Schablone).</span><span class="sxs-lookup"><span data-stu-id="88f4d-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="88f4d-133">Die unter Quell Indizierung für ein Array mit zwei Depth-Stencil Bildern, die jeweils über drei MIP-Ebenen verfügen, ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88f4d-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![tiefen Schablone-Indizierung](images/depth-stencil-indexing.png)

<span data-ttu-id="88f4d-135">Unterstichprobe: YCbCr unterstützt Arrays und verfügt über Ebenen, unterstützt jedoch keine Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="88f4d-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="88f4d-136">YCbCr-Bilder verfügen über zwei Ebenen, eine für die Leuchtkraft (Y), für die das menschliche Auge am empfindlichsten ist, und eine für die Chrominanz (sowohl CB als auch CR, Interleaved), für die das menschliche Auge weniger sensibel ist.</span><span class="sxs-lookup"><span data-stu-id="88f4d-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="88f4d-137">Dieses Format ermöglicht die Komprimierung der Chrome-Werte zum Komprimieren eines Bilds, ohne dass sich dies auf die Leuchtkraft auswirkt, und ist aus diesem Grund ein gängiges Video Komprimierungs Format, obwohl es zum Komprimieren von Bildern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="88f4d-138">Das folgende Bild zeigt das NV12-Format, wobei die Chrominanz in ein Viertel der Auflösung der Leuchtkraft komprimiert wurde, was bedeutet, dass die Breite der einzelnen Ebenen identisch ist, und die Chrominanz-Ebene die Hälfte der Höhe der Leuchtkraft Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="88f4d-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="88f4d-139">Die Flächen werden in gleicher Weise wie das oben beschriebene Depth-Stencil Beispiel als unter Ressourcen indiziert.</span><span class="sxs-lookup"><span data-stu-id="88f4d-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![Das nv12-Format](images/ycbcr.png)

<span data-ttu-id="88f4d-141">Planare Formate waren in Direct3D 11 vorhanden, aber einzelne Flächen konnten nicht einzeln adressiert werden, z.. bei Kopier-oder zuordnungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="88f4d-142">Dies wurde in Direct3D 12 geändert, sodass jede Ebene eine eigene untergeordnete Quell-ID erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="88f4d-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="88f4d-143">Vergleichen Sie die beiden folgenden Methoden, um die untergeordnete Quell-ID zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="88f4d-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="88f4d-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="88f4d-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="88f4d-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="88f4d-146">Die meisten Hardware geht davon aus, dass der Arbeitsspeicher für die Ebene n nach der Ebene n-1 immer sofort zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="88f4d-147">Eine Alternative zur Verwendung von unter Berichten besteht darin, dass eine APP eine vollständig separate Ressource pro Ebene zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="88f4d-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="88f4d-148">In diesem Fall versteht die Anwendung, dass die Daten planare sind, und verwendet mehrere Ressourcen, um Sie darzustellen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="88f4d-149">Mehrere unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88f4d-149">Multiple subresources</span></span>

<span data-ttu-id="88f4d-150">In einer Shader-Ressourcen Ansicht können beliebige rechteckige Bereiche von unter Berichten ausgewählt werden, wobei eines der oben beschriebenen Slices und die Verwendung von Feldern in den Sicht Strukturen (z. b. [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), wie in der Abbildung dargestellt, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![Auswahl mehrerer unter Quellen](images/subresource-multiple.png)

<span data-ttu-id="88f4d-152">Eine renderzielansicht kann nur eine einzelne untergeordnete Quelle oder einen MIP-Slice verwenden und darf keine unter Ressourcen aus mehreren MIP-Slice enthalten.</span><span class="sxs-lookup"><span data-stu-id="88f4d-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="88f4d-153">Das heißt, jede Textur in einer renderzielansicht muss dieselbe Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="88f4d-154">In einer Shader-Ressourcen Ansicht können beliebige rechteckige Bereiche von unter Berichten ausgewählt werden, wie in der Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88f4d-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="88f4d-155">Subresource-APIs</span><span class="sxs-lookup"><span data-stu-id="88f4d-155">Subresource APIs</span></span>

<span data-ttu-id="88f4d-156">Die folgenden APIs verweisen auf und arbeiten mit unter Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="88f4d-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="88f4d-157">Aufzählungen:</span><span class="sxs-lookup"><span data-stu-id="88f4d-157">Enumerations:</span></span>

-   [<span data-ttu-id="88f4d-158">**D3D12 \_ Textur \_ \_ kopierungstyp**</span><span class="sxs-lookup"><span data-stu-id="88f4d-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="88f4d-159">Die folgenden Strukturen enthalten *planeslice* -Indizes, die in den meisten *mipslice* -Indizes enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="88f4d-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="88f4d-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="88f4d-161">**D3D12 \_ TEX2D \_ array \_ -RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="88f4d-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="88f4d-163">**D3D12 \_ TEX2D- \_ Array ( \_ SRV)**</span><span class="sxs-lookup"><span data-stu-id="88f4d-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="88f4d-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="88f4d-165">**D3D12 \_ TEX2D \_ array- \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="88f4d-166">Die folgenden Strukturen enthalten *arrayslice* -Indizes, die in den meisten *mipslice* -Indizes enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="88f4d-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="88f4d-167">**D3D12 \_ TEX1D \_ array- \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="88f4d-168">**D3D12 \_ TEX2D \_ array- \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="88f4d-169">**D3D12 \_ TEX2DMS \_ array- \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="88f4d-170">**D3D12 \_ TEX1D \_ array \_ -RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="88f4d-171">**D3D12 \_ TEX2D \_ array \_ -RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="88f4d-172">**D3D12 \_ TEX2DMS \_ array \_ -RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="88f4d-173">**D3D12 \_ TEX1D- \_ Array ( \_ SRV)**</span><span class="sxs-lookup"><span data-stu-id="88f4d-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="88f4d-174">**D3D12 \_ TEX2D- \_ Array ( \_ SRV)**</span><span class="sxs-lookup"><span data-stu-id="88f4d-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="88f4d-175">**D3D12 \_ TEX2DMS- \_ Array ( \_ SRV)**</span><span class="sxs-lookup"><span data-stu-id="88f4d-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="88f4d-176">**D3D12 \_ TEX1D \_ array- \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="88f4d-177">**D3D12 \_ TEX2D \_ array- \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="88f4d-178">Die folgenden Strukturen enthalten *mipslice* -Indizes, aber weder *arrayslice* noch *planeslice* -Indizes.</span><span class="sxs-lookup"><span data-stu-id="88f4d-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="88f4d-179">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="88f4d-180">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="88f4d-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="88f4d-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="88f4d-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="88f4d-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="88f4d-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="88f4d-185">Die folgenden Strukturen verweisen auch auf unter Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="88f4d-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="88f4d-186">[**D3D12 \_ \_Region verwerfen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : eine Struktur, die zur Vorbereitung der verwerfen einer Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="88f4d-187">[**D3D12 \_ Platzierung \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) der untergeordneten Quelle: Fügt der Grundlagen einen Offset zu einer Ressource hinzu.</span><span class="sxs-lookup"><span data-stu-id="88f4d-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="88f4d-188">[**D3D12 \_ Ressourcen \_ Übergangs \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : Beschreibt den Übergang von unter Ressourcen zwischen unterschiedlichen Verwendungen (Shader-Ressource, Renderziel usw.).</span><span class="sxs-lookup"><span data-stu-id="88f4d-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="88f4d-189">[**D3D12 \_ SUBRESOURCE- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : die Daten der untergeordneten Quelle enthalten die Daten selbst und die Zeilen-und Slice-Tonhöhe.</span><span class="sxs-lookup"><span data-stu-id="88f4d-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="88f4d-190">[**D3D12 \_ Ressourcen \_ Bedarf**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) in der unter Quelle: ein Ressourcenbedarf umfasst das Format, die Breite, die Höhe, die Tiefe und die Zeilengröße der unter Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="88f4d-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="88f4d-191">[**D3D12 \_ Subresource- \_ Informationen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : enthält den Offset, die Zeilen-und die Tiefe des unter Berichts.</span><span class="sxs-lookup"><span data-stu-id="88f4d-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="88f4d-192">[**D3D12 \_ SUBRESOURCE- \_ tiult**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : Beschreibt ein gespeichertes unter Quell Volume (siehe [Volume-Kachel Ressourcen](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="88f4d-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="88f4d-193">[**D3D12 \_ \_ \_ Speicherort der Textur Kopie**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : Beschreibt einen Teil einer Textur zum Kopieren.</span><span class="sxs-lookup"><span data-stu-id="88f4d-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="88f4d-194">[**D3D12 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : Beschreibt die Koordinaten einer gekachelten Ressource.</span><span class="sxs-lookup"><span data-stu-id="88f4d-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="88f4d-195">Methoden:</span><span class="sxs-lookup"><span data-stu-id="88f4d-195">Methods:</span></span>

-   <span data-ttu-id="88f4d-196">[**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : Ruft Informationen zu einer Ressource ab, damit eine Kopie erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="88f4d-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="88f4d-197">[**ID3D12Device:: getresourcetielt**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="88f4d-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="88f4d-198">[**ID3D12GraphicsCommandList:: resolvesubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : kopiert eine untergeordnete Quelle mit mehreren Stichproben in eine untergeordnete Quelle, die nicht mehrere Stichproben enthält.</span><span class="sxs-lookup"><span data-stu-id="88f4d-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="88f4d-199">[**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : gibt einen Zeiger auf die angegebenen Daten in der Ressource zurück und verweigert den GPU-Zugriff auf die untergeordnete Quelle.</span><span class="sxs-lookup"><span data-stu-id="88f4d-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="88f4d-200">[**ID3D12Resource:: Read fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : kopiert Daten aus einer unter Quelle oder einem rechteckigen Bereich einer unter Quelle.</span><span class="sxs-lookup"><span data-stu-id="88f4d-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="88f4d-201">[**ID3D12Resource:: unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : hebt die Zuordnung des angegebenen Speicherbereichs auf und macht den Zeiger auf die Ressource ungültig.</span><span class="sxs-lookup"><span data-stu-id="88f4d-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="88f4d-202">Gibt den GPU-Zugriff auf die untergeordnete Quelle wieder.</span><span class="sxs-lookup"><span data-stu-id="88f4d-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="88f4d-203">[**ID3D12Resource:: Write-in subresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : kopiert Daten in eine untergeordnete Quelle oder einen rechteckigen Bereich eines unter Berichts.</span><span class="sxs-lookup"><span data-stu-id="88f4d-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="88f4d-204">Texturen müssen sich im allgemeinen Status des [**D3D12- \_ Ressourcen \_ Zustands \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) befinden, damit der CPU-Zugriff über " [**Write**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) " und "read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) " rechtmäßig ist, aber Puffer nicht.</span><span class="sxs-lookup"><span data-stu-id="88f4d-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="88f4d-205">Der CPU-Zugriff auf eine Ressource erfolgt in der Regel über [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span><span class="sxs-lookup"><span data-stu-id="88f4d-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88f4d-206">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="88f4d-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f4d-207">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="88f4d-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




