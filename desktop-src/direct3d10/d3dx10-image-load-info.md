---
description: Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. Der Wert d3dx10 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: D3DX10_IMAGE_LOAD_INFO-Struktur (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369319"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="8ae88-104">D3dx10 \_ Image \_ Load \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="8ae88-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="8ae88-105">Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8ae88-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="8ae88-106">Der Wert d3dx10 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ae88-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae88-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae88-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="8ae88-108">Member</span><span class="sxs-lookup"><span data-stu-id="8ae88-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ae88-109">**Width**</span><span class="sxs-lookup"><span data-stu-id="8ae88-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-111">Die Ziel Breite der Textur.</span><span class="sxs-lookup"><span data-stu-id="8ae88-111">The target width of the texture.</span></span> <span data-ttu-id="8ae88-112">Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="8ae88-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-113">**Height**</span><span class="sxs-lookup"><span data-stu-id="8ae88-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-115">Die Zielhöhe der Textur.</span><span class="sxs-lookup"><span data-stu-id="8ae88-115">The target height of the texture.</span></span> <span data-ttu-id="8ae88-116">Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.</span><span class="sxs-lookup"><span data-stu-id="8ae88-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-117">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="8ae88-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-119">Die Tiefe der Textur.</span><span class="sxs-lookup"><span data-stu-id="8ae88-119">The depth of the texture.</span></span> <span data-ttu-id="8ae88-120">Dies gilt nur für Volumentexturen.</span><span class="sxs-lookup"><span data-stu-id="8ae88-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-121">**Firstmiplevel**</span><span class="sxs-lookup"><span data-stu-id="8ae88-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-123">Die höchste Auflösung der MipMap-Ebene der Textur.</span><span class="sxs-lookup"><span data-stu-id="8ae88-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="8ae88-124">Wenn dieser Wert größer als 0 ist, wird firstmiplevel nach dem Laden der Textur der MipMap-Ebene 0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8ae88-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-125">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="8ae88-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-127">Die maximale Anzahl von MipMap-Ebenen, die die Textur enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="8ae88-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="8ae88-128">Die Verwendung von 0 oder d3dx10 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae88-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-129">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="8ae88-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-130">Type: **[ **d3d10 \_ Usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-131">Die Art und Weise, in der die Textur Ressource verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae88-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="8ae88-132">Siehe [**d3d10 \_ Usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="8ae88-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="8ae88-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-134">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-135">Die Pipeline Stufen, an die die Textur gebunden werden darf.</span><span class="sxs-lookup"><span data-stu-id="8ae88-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="8ae88-136">Siehe [**d3d10 \_ Bind- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="8ae88-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-137">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="8ae88-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-138">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-139">Die Zugriffsberechtigungen der CPU für die Textur Ressource.</span><span class="sxs-lookup"><span data-stu-id="8ae88-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="8ae88-140">Siehe [**d3d10 \_ CPU \_ - \_ Zugriffsflag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="8ae88-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-141">**Fehlflags**</span><span class="sxs-lookup"><span data-stu-id="8ae88-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-142">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-143">Verschiedene Ressourcen Eigenschaften (siehe [**d3d10 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="8ae88-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-144">**Format**</span><span class="sxs-lookup"><span data-stu-id="8ae88-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-145">Typ: **[ **DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-146">Das Format, in dem sich die Textur befindet, nachdem Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="8ae88-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="8ae88-147">Siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8ae88-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="8ae88-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-149">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-150">Filtert die Textur mithilfe des angegebenen Filters (nur beim erneuten Sampling).</span><span class="sxs-lookup"><span data-stu-id="8ae88-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="8ae88-151">Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8ae88-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="8ae88-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-153">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae88-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-154">Filtert die Textur-MIP-Ebenen mithilfe des angegebenen Filters (nur beim Erzeugen von Mipmaps).</span><span class="sxs-lookup"><span data-stu-id="8ae88-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="8ae88-155">Gültige Werte sind d3dx10 \_ Filter \_ None, d3dx10 \_ Filter \_ Point, d3dx10 \_ Filter \_ linear oder d3dx10 \_ Filter \_ Dreieck.</span><span class="sxs-lookup"><span data-stu-id="8ae88-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="8ae88-156">Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8ae88-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ae88-157">**psrcinfo**</span><span class="sxs-lookup"><span data-stu-id="8ae88-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8ae88-158">Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae88-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="8ae88-159">Informationen zum ursprünglichen Image.</span><span class="sxs-lookup"><span data-stu-id="8ae88-159">Information about the original image.</span></span> <span data-ttu-id="8ae88-160">Siehe [**d3dx10 \_ Image \_ Info**](d3dx10-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="8ae88-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="8ae88-161">Kann mit [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)oder [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8ae88-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ae88-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ae88-162">Remarks</span></span>

<span data-ttu-id="8ae88-163">Wenn Sie die Struktur initialisieren, können Sie ein beliebiges Element auf d3dx10 default festlegen, \_ und D3DX initialisiert es mit einem Standardwert aus der Quell Textur, wenn die Textur geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8ae88-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="8ae88-164">Diese Struktur kann von APIs verwendet werden, die folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="8ae88-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="8ae88-165">Erstellen Sie Ressourcen, z. b. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="8ae88-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="8ae88-166">Erstellen Sie Datenprozessoren, z. b. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) oder [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="8ae88-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae88-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ae88-167">Requirements</span></span>



| <span data-ttu-id="8ae88-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ae88-168">Requirement</span></span> | <span data-ttu-id="8ae88-169">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae88-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae88-170">Header</span><span class="sxs-lookup"><span data-stu-id="8ae88-170">Header</span></span><br/> | <dl> <span data-ttu-id="8ae88-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae88-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae88-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ae88-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae88-173">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8ae88-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
