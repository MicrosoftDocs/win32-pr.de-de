---
title: Unter Berichte (Direct3D 11-Grafiken)
description: In diesem Thema werden Textur-unter Ressourcen oder Teile einer Ressource beschrieben.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039908"
---
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="8cd9c-103">Unter Berichte (Direct3D 11-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="8cd9c-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="8cd9c-104">In diesem Thema werden Textur-unter Ressourcen oder Teile einer Ressource beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="8cd9c-105">Direct3D kann auf eine gesamte Ressource verweisen, oder Sie kann auf Teilmengen einer Ressource verweisen.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="8cd9c-106">Der Begriff "subresource" verweist auf eine Teilmenge einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="8cd9c-107">Ein Puffer ist als einzelne untergeordnete Quelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="8cd9c-108">Texturen sind etwas komplizierter, da einige verschiedene Textur Typen (1D, 2D usw.) aufweisen, von denen einige MipMap-Ebenen und/oder Textur Arrays unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="8cd9c-109">Beginnend mit dem einfachsten Fall wird eine 1D-Textur als einzelne untergeordnete Quelle definiert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![Abbildung einer 1D-Textur](images/d3d10-1d-texture.png)

<span data-ttu-id="8cd9c-111">Dies bedeutet, dass das Array von texeln, die eine 1D-Textur bilden, in einer einzelnen untergeordneten Quelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="8cd9c-112">Wenn Sie eine 1D-Textur mit drei MipMap-Ebenen erweitern, kann Sie wie in der folgenden Abbildung dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![Abbildung einer 1D-Textur mit drei MipMap-Ebenen](images/d3d10-resource-texture1d.png)

<span data-ttu-id="8cd9c-114">Stellen Sie sich dies als eine einzelne Textur vor, die aus drei unter Ressourcen besteht.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="8cd9c-115">Ein unter Bericht kann mit der Detailgenauigkeit (LOD) für eine einzelne Textur indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="8cd9c-116">Wenn Sie ein Array von Texturen verwenden, sind für den Zugriff auf eine bestimmte untergeordnete Quelle sowohl die Lod als auch die jeweilige Textur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="8cd9c-117">Alternativ kombiniert die API diese beiden Informationen in einem einzelnen Null basierten unter Quell Index, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![Abbildung eines NULL basierten unter Quell Indexes](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="8cd9c-119">Auswählen von unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8cd9c-119">Selecting Subresources</span></span>

<span data-ttu-id="8cd9c-120">Einige APIs greifen auf eine gesamte Ressource zu (z. b. die [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) -Methode), von denen andere auf einen Teil einer Ressource zugreifen (z. b. die [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) -Methode oder die [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) -Methode).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="8cd9c-121">Die Methoden, die auf einen Teil einer Ressource zugreifen, verwenden im Allgemeinen eine Ansichts Beschreibung (z. b. die [**D3D11 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) -Struktur), um die unter Ressourcen anzugeben, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="8cd9c-122">Die Abbildungen in den folgenden Abschnitten zeigen die Begriffe, die von einer Ansichts Beschreibung beim Zugriff auf ein Array von Texturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="8cd9c-123">Array Slice</span><span class="sxs-lookup"><span data-stu-id="8cd9c-123">Array Slice</span></span>

<span data-ttu-id="8cd9c-124">Bei einem Array von Texturen enthält jede Textur mit Mipmaps, ein *Array Slice* (dargestellt durch das weiße Rechteck), eine Textur und alle zugehörigen unter Ressourcen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![Abbildung eines Array Slice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="8cd9c-126">MIP-Slice</span><span class="sxs-lookup"><span data-stu-id="8cd9c-126">Mip Slice</span></span>

<span data-ttu-id="8cd9c-127">Ein *MIP-Slice* (dargestellt durch das weiße Rechteck) enthält eine MipMap-Ebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![Abbildung eines MIP-Slice](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="8cd9c-129">Auswählen einer einzelnen untergeordneten Quelle</span><span class="sxs-lookup"><span data-stu-id="8cd9c-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="8cd9c-130">Sie können diese beiden Arten von Slices verwenden, um eine einzelne untergeordnete Quelle auszuwählen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![Abbildung der Auswahl eines unter Berichts mithilfe eines Array Slice und eines MIP-Slice](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="8cd9c-132">Auswählen mehrerer unter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8cd9c-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="8cd9c-133">Oder Sie können diese beiden Arten von Slices mit der Anzahl von MipMap-Ebenen und/oder der Anzahl von Texturen verwenden, um mehrere unter Ressourcen auszuwählen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![Darstellung der Auswahl mehrerer unter Berichte](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="8cd9c-135">Eine [**renderzielansicht**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) kann nur eine einzelne untergeordnete Quelle oder einen MIP-Slice verwenden und darf keine unter Ressourcen aus mehreren MIP-Slice enthalten.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="8cd9c-136">Das heißt, jede Textur in einer renderzielansicht muss dieselbe Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="8cd9c-137">In der [**Ansicht "Shader-Resource**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) " kann ein beliebiger rechteckiger Bereich von unter Berichten ausgewählt werden, wie in der Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8cd9c-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cd9c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd9c-139">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8cd9c-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




