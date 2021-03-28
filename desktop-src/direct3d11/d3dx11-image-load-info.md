---
title: D3DX11_IMAGE_LOAD_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_LOAD_INFO-Struktur (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO Struktur Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO Struktur Zeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982556"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="d6d17-107">Bibliothek d3dx11 \_ Image \_ Load \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="d6d17-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="d6d17-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6d17-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="d6d17-109">Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d6d17-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="d6d17-110">Der Wert Bibliothek d3dx11 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6d17-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d17-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6d17-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="d6d17-112">Member</span><span class="sxs-lookup"><span data-stu-id="d6d17-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="d6d17-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="d6d17-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-115">Die Ziel Breite der Textur.</span><span class="sxs-lookup"><span data-stu-id="d6d17-115">The target width of the texture.</span></span> <span data-ttu-id="d6d17-116">Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="d6d17-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="d6d17-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-119">Die Zielhöhe der Textur.</span><span class="sxs-lookup"><span data-stu-id="d6d17-119">The target height of the texture.</span></span> <span data-ttu-id="d6d17-120">Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.</span><span class="sxs-lookup"><span data-stu-id="d6d17-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-121">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="d6d17-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-122">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-123">Die Tiefe der Textur.</span><span class="sxs-lookup"><span data-stu-id="d6d17-123">The depth of the texture.</span></span> <span data-ttu-id="d6d17-124">Dies gilt nur für Volumentexturen.</span><span class="sxs-lookup"><span data-stu-id="d6d17-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-125">**Firstmiplevel**</span><span class="sxs-lookup"><span data-stu-id="d6d17-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-126">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-127">Die höchste Auflösung der MipMap-Ebene der Textur.</span><span class="sxs-lookup"><span data-stu-id="d6d17-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="d6d17-128">Wenn dieser Wert größer als 0 ist, wird firstmiplevel nach dem Laden der Textur der MipMap-Ebene 0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6d17-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-129">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="d6d17-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-130">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-131">Die maximale Anzahl von MipMap-Ebenen in der Textur.</span><span class="sxs-lookup"><span data-stu-id="d6d17-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="d6d17-132">Weitere Informationen finden Sie in den Hinweisen unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="d6d17-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="d6d17-133">Die Verwendung von 0 oder Bibliothek d3dx11 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d17-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-134">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="d6d17-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-135">Type: **[ **D3D11 \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-136">Die Art und Weise, in der die Textur Ressource verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6d17-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="d6d17-137">Siehe [**D3D11 \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="d6d17-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="d6d17-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-139">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-140">Die Pipeline Stufen, an die die Textur gebunden werden darf.</span><span class="sxs-lookup"><span data-stu-id="d6d17-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="d6d17-141">Siehe [**D3D11 \_ Bind- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="d6d17-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-142">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="d6d17-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-143">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-144">Die Zugriffsberechtigungen der CPU für die Textur Ressource.</span><span class="sxs-lookup"><span data-stu-id="d6d17-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="d6d17-145">Siehe [**D3D11 \_ CPU \_ - \_ Zugriffsflag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="d6d17-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-146">**Fehlflags**</span><span class="sxs-lookup"><span data-stu-id="d6d17-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-147">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-148">Verschiedene Ressourcen Eigenschaften (siehe [**D3D11 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="d6d17-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-149">**Format**</span><span class="sxs-lookup"><span data-stu-id="d6d17-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-150">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-151">Eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , die das Format angibt, in dem sich die Textur befindet, nachdem Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d6d17-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-152">**Filter**</span><span class="sxs-lookup"><span data-stu-id="d6d17-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-153">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-154">Filtert die Textur mithilfe des angegebenen Filters (nur beim erneuten Sampling).</span><span class="sxs-lookup"><span data-stu-id="d6d17-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="d6d17-155">Siehe [**Bibliothek d3dx11 \_ Filter- \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="d6d17-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-157">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6d17-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-158">Filtert die Textur-MIP-Ebenen mithilfe des angegebenen Filters (nur beim Erzeugen von Mipmaps).</span><span class="sxs-lookup"><span data-stu-id="d6d17-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="d6d17-159">Gültige Werte sind Bibliothek d3dx11 \_ Filter \_ None, Bibliothek d3dx11 \_ Filter \_ Point, Bibliothek d3dx11 \_ Filter \_ linear oder Bibliothek d3dx11 \_ Filter \_ Dreieck.</span><span class="sxs-lookup"><span data-stu-id="d6d17-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="d6d17-160">Siehe [**Bibliothek d3dx11 \_ Filter- \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d17-161">**psrcinfo**</span><span class="sxs-lookup"><span data-stu-id="d6d17-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d6d17-162">Type: **[ **Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6d17-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="d6d17-163">Informationen zum ursprünglichen Image.</span><span class="sxs-lookup"><span data-stu-id="d6d17-163">Information about the original image.</span></span> <span data-ttu-id="d6d17-164">Siehe [**Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="d6d17-165">Kann mit [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6d17-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6d17-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6d17-166">Remarks</span></span>

<span data-ttu-id="d6d17-167">Wenn Sie die Struktur initialisieren, können Sie ein beliebiges Element auf Bibliothek d3dx11 default festlegen, \_ und D3DX initialisiert es mit einem Standardwert aus der Quell Textur, wenn die Textur geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d6d17-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="d6d17-168">Diese Struktur kann von APIs verwendet werden, die folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="d6d17-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="d6d17-169">Erstellen Sie Ressourcen, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="d6d17-170">Erstellen Sie Datenprozessoren, z. b. [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) oder [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="d6d17-171">Die Standardwerte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d6d17-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="d6d17-172">Im folgenden finden Sie ein kurzes Beispiel, in dem diese Struktur verwendet wird, um beim Laden einer Textur das Pixel Format bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6d17-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="d6d17-173">Den gesamten Code finden Sie unter HDRFormats10. cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d6d17-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="d6d17-174">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d6d17-174">Requirements</span></span>



| <span data-ttu-id="d6d17-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6d17-175">Requirement</span></span> | <span data-ttu-id="d6d17-176">Wert</span><span class="sxs-lookup"><span data-stu-id="d6d17-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d17-177">Header</span><span class="sxs-lookup"><span data-stu-id="d6d17-177">Header</span></span><br/> | <dl> <span data-ttu-id="d6d17-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6d17-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d17-179">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6d17-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d17-180">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d6d17-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

