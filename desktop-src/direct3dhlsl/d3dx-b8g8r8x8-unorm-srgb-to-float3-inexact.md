---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982113"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="42caa-105">D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ in \_ FLOAT3 \_ ungenau-Funktion</span><span class="sxs-lookup"><span data-stu-id="42caa-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="42caa-106">Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="42caa-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="42caa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42caa-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="42caa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42caa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42caa-109">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="42caa-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="42caa-110">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="42caa-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42caa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42caa-111">Return value</span></span>

<span data-ttu-id="42caa-112">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="42caa-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="42caa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42caa-113">Remarks</span></span>

<span data-ttu-id="42caa-114">Diese Funktion verwendet shaderanweisungen, die keine hohe genug Genauigkeit aufweisen, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="42caa-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="42caa-115">Die Alternative Funktion [**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) verwendet eine im Shader gespeicherte Such Tabelle, um eine exakte sRGB-Konvertierung für die Gleit Komma Zahl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42caa-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="42caa-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="42caa-116">Requirements</span></span>



| <span data-ttu-id="42caa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42caa-117">Requirement</span></span> | <span data-ttu-id="42caa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="42caa-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42caa-119">Header</span><span class="sxs-lookup"><span data-stu-id="42caa-119">Header</span></span><br/> | <dl> <span data-ttu-id="42caa-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="42caa-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42caa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42caa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42caa-122">Funktionen</span><span class="sxs-lookup"><span data-stu-id="42caa-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="42caa-123">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="42caa-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





