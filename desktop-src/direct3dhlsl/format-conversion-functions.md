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
# <a name="format-conversion-functions-hlsl-reference"></a>Formatkonvertierungs Funktionen (HLSL-Referenz)

Der-Abschnitt enthält die Format Konvertierungs Funktionen, die in COMPUTE-und Pixel-Shadern verwendet werden.

-   [Konverterfunktionen](#converter-functions)
-   [Zugehörige Themen](#related-topics)

> Der D3DX_DXGIFormatConvert. INL-Header wird im Legacy-DirectX-SDK ausgeliefert und ist für die C++-Unterstützung auf xnamath angewiesen. Es ist auch im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) enthalten. Die neueste Version verwendet directxmath für die C++-Unterstützung, und alle Funktionen werden im **DirectX** C++-Namespace definiert.

## <a name="converter-functions"></a>Konverterfunktionen

### <a name="dxgi_format_r10g10b10a2_unorm"></a>DXGI- \_ Format \_ R10G10B10A2 \_ unorm

<dl>

[**D3DX \_ R10G10B10A2 \_ unorm \_ zu \_ float4**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**D3DX \_ float4 \_ auf \_ R10G10B10A2 \_ unorm**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>DXGI- \_ Format \_ R10G10B10A2 \_ uint

<dl>

[**D3DX \_ R10G10B10A2 \_ uint \_ in \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ bis \_ R10G10B10A2 \_ uint**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>DXGI- \_ Format \_ R8G8B8A8 \_ unorm:

<dl>

[**D3DX \_ R8G8B8A8 \_ unorm \_ zu \_ float4**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB

<dl>

[**D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ auf \_ float4 \_ ungenau**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ auf \_ float4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>DXGI- \_ Format \_ R8G8B8A8 \_ uint

<dl>

[**D3DX \_ R8G8B8A8 \_ uint \_ in \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ bis \_ R8G8B8A8 \_ uint**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>DXGI- \_ Format \_ R8G8B8A8 \_ snorm

<dl>

[**D3DX \_ R8G8B8A8 \_ snorm \_ auf \_ float4**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**D3DX \_ float4 \_ bis \_ R8G8B8A8 \_ snorm**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>DXGI- \_ Format \_ R8G8B8A8 \_ Sint

<dl>

[**D3DX \_ R8G8B8A8 \_ Sint \_ in \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ Sint**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>DXGI- \_ Format \_ B8G8R8A8 \_ unorm

<dl>

[**D3DX \_ B8G8R8A8 \_ unorm \_ zu \_ float4**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**D3DX \_ float4 \_ auf \_ B8G8R8A8 \_ unorm**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB

<dl>

[**D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ auf \_ float4 \_ ungenau**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ auf \_ float4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ float4 \_ auf \_ R8G8B8A8 \_ unorm \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>DXGI- \_ Format \_ B8G8R8X8 \_ unorm

<dl>

[**D3DX \_ B8G8R8X8 \_ unorm \_ zu \_ FLOAT3**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**D3DX \_ FLOAT3 \_ auf \_ B8G8R8X8 \_ unorm**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB

<dl>

[**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ auf \_ FLOAT3 \_ ungenau**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ auf \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**D3DX \_ FLOAT3 \_ auf \_ B8G8R8X8 \_ unorm \_ sRGB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>DXGI- \_ Format \_ R16G16 \_ float

<dl>

[**D3DX \_ R16G16 \_ float \_ zu \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**D3DX \_ FLOAT2 \_ to \_ R16G16 \_ float**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>DXGI- \_ Format \_ R16G16 \_ unorm

<dl>

[**D3DX \_ R16G16 \_ unorm \_ zu \_ FLOAT2**](d3dx-r16g16-unorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ auf \_ R16G16 \_ unorm**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>DXGI- \_ Format \_ R16G16 \_ uint

<dl>

[**D3DX \_ R16G16 \_ uint \_ in \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**D3DX \_ UINT2 \_ bis \_ R16G16 \_ uint**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>DXGI- \_ Format \_ R16G16 \_ snorm

<dl>

[**D3DX \_ R16G16 \_ snorm \_ auf \_ FLOAT2**](d3dx-r16g16-snorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ bis \_ R16G16 \_ snorm**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>DXGI- \_ Format \_ R16G16 \_ Sint

<dl>

[**D3DX \_ R16G16 \_ Sint \_ in \_ int2**](d3dx-r16g16-sint-to-int2.md)  
[**D3DX \_ int2 \_ to \_ R16G16 \_ Sint**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Inline Format Konvertierung](inline-format-conversion-reference.md)
</dt> <dt>

[Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
