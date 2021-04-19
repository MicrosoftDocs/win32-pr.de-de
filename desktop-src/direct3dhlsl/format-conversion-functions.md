---
title: Formatkonvertierungs Funktionen (HLSL-Referenz)
description: Der-Abschnitt enthält die Format Konvertierungs Funktionen, die in COMPUTE-und Pixel-Shadern verwendet werden.
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 355fb59aa6a94e144daf05942b40d3f685daff51
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222878"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="97a44-103">Formatkonvertierungs Funktionen (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="97a44-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="97a44-104">Der-Abschnitt enthält die Format Konvertierungs Funktionen, die in COMPUTE-und Pixel-Shadern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97a44-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="97a44-105">Konverterfunktionen</span><span class="sxs-lookup"><span data-stu-id="97a44-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="97a44-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97a44-106">Related topics</span></span>](#related-topics)

> <span data-ttu-id="97a44-107">Der D3DX_DXGIFormatConvert. INL-Header wird im Legacy-DirectX-SDK ausgeliefert und ist für die C++-Unterstützung auf xnamath angewiesen.</span><span class="sxs-lookup"><span data-stu-id="97a44-107">The D3DX_DXGIFormatConvert.inl header ships in the legacy DirectX SDK and relied on XNAMath for C++ support.</span></span> <span data-ttu-id="97a44-108">Es ist auch im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) enthalten.</span><span class="sxs-lookup"><span data-stu-id="97a44-108">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span> <span data-ttu-id="97a44-109">Die neueste Version verwendet directxmath für die C++-Unterstützung, und alle Funktionen werden im **DirectX** C++-Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="97a44-109">The latest version uses DirectXMath for C++ support, and all functions are defined in the **DirectX** C++ namespace.</span></span>

## <a name="converter-functions"></a><span data-ttu-id="97a44-110">Konverterfunktionen</span><span class="sxs-lookup"><span data-stu-id="97a44-110">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="97a44-111">DXGI- \_ Format \_ R10G10B10A2 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="97a44-111">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="97a44-112">**D3DX \_ R10G10B10A2 \_ unorm \_ zu \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-112">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="97a44-113">**D3DX \_ float4 \_ auf \_ R10G10B10A2 \_ unorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-113">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="97a44-114">DXGI- \_ Format \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="97a44-114">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="97a44-115">**D3DX \_ R10G10B10A2 \_ uint \_ in \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="97a44-115">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="97a44-116">**D3DX \_ UINT4 \_ bis \_ R10G10B10A2 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="97a44-116">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="97a44-117">DXGI- \_ Format \_ R8G8B8A8 \_ unorm:</span><span class="sxs-lookup"><span data-stu-id="97a44-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="97a44-118">**D3DX \_ R8G8B8A8 \_ unorm \_ zu \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-118">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="97a44-119">**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-119">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="97a44-120">DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="97a44-120">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="97a44-121">**D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ auf \_ float4 \_ ungenau**</span><span class="sxs-lookup"><span data-stu-id="97a44-121">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="97a44-122">**D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ auf \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-122">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="97a44-123">**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="97a44-123">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="97a44-124">DXGI- \_ Format \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="97a44-124">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="97a44-125">**D3DX \_ R8G8B8A8 \_ uint \_ in \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="97a44-125">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="97a44-126">**D3DX \_ UINT4 \_ bis \_ R8G8B8A8 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="97a44-126">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="97a44-127">DXGI- \_ Format \_ R8G8B8A8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="97a44-127">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="97a44-128">**D3DX \_ R8G8B8A8 \_ snorm \_ auf \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-128">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="97a44-129">**D3DX \_ float4 \_ bis \_ R8G8B8A8 \_ snorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-129">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="97a44-130">DXGI- \_ Format \_ R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="97a44-130">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="97a44-131">**D3DX \_ R8G8B8A8 \_ Sint \_ in \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="97a44-131">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="97a44-132">**D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ Sint**</span><span class="sxs-lookup"><span data-stu-id="97a44-132">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="97a44-133">DXGI- \_ Format \_ B8G8R8A8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="97a44-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="97a44-134">**D3DX \_ B8G8R8A8 \_ unorm \_ zu \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-134">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="97a44-135">**D3DX \_ float4 \_ auf \_ B8G8R8A8 \_ unorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-135">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="97a44-136">DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="97a44-136">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="97a44-137">**D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ auf \_ float4 \_ ungenau**</span><span class="sxs-lookup"><span data-stu-id="97a44-137">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="97a44-138">**D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ auf \_ float4**</span><span class="sxs-lookup"><span data-stu-id="97a44-138">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="97a44-139">**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="97a44-139">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="97a44-140">DXGI- \_ Format \_ B8G8R8X8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="97a44-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="97a44-141">**D3DX \_ B8G8R8X8 \_ unorm \_ zu \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="97a44-141">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="97a44-142">**D3DX \_ FLOAT3 \_ auf \_ B8G8R8X8 \_ unorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-142">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="97a44-143">DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="97a44-143">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="97a44-144">**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ auf \_ FLOAT3 \_ ungenau**</span><span class="sxs-lookup"><span data-stu-id="97a44-144">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="97a44-145">**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ auf \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="97a44-145">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="97a44-146">**D3DX \_ FLOAT3 \_ auf \_ B8G8R8X8 \_ unorm \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="97a44-146">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="97a44-147">DXGI- \_ Format \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="97a44-147">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="97a44-148">**D3DX \_ R16G16 \_ float \_ zu \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="97a44-148">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="97a44-149">**D3DX \_ FLOAT2 \_ to \_ R16G16 \_ float**</span><span class="sxs-lookup"><span data-stu-id="97a44-149">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="97a44-150">DXGI- \_ Format \_ R16G16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="97a44-150">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="97a44-151">**D3DX \_ R16G16 \_ unorm \_ zu \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="97a44-151">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="97a44-152">**D3DX \_ FLOAT2 \_ auf \_ R16G16 \_ unorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-152">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="97a44-153">DXGI- \_ Format \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="97a44-153">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="97a44-154">**D3DX \_ R16G16 \_ uint \_ in \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="97a44-154">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="97a44-155">**D3DX \_ UINT2 \_ bis \_ R16G16 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="97a44-155">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="97a44-156">DXGI- \_ Format \_ R16G16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="97a44-156">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="97a44-157">**D3DX \_ R16G16 \_ snorm \_ auf \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="97a44-157">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="97a44-158">**D3DX \_ FLOAT2 \_ bis \_ R16G16 \_ snorm**</span><span class="sxs-lookup"><span data-stu-id="97a44-158">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="97a44-159">DXGI- \_ Format \_ R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="97a44-159">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="97a44-160">**D3DX \_ R16G16 \_ Sint \_ in \_ int2**</span><span class="sxs-lookup"><span data-stu-id="97a44-160">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="97a44-161">**D3DX \_ int2 \_ to \_ R16G16 \_ Sint**</span><span class="sxs-lookup"><span data-stu-id="97a44-161">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="97a44-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97a44-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a44-163">Referenz zur Inline Format Konvertierung</span><span class="sxs-lookup"><span data-stu-id="97a44-163">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="97a44-164">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="97a44-164">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
