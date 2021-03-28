---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995788"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="31eee-105">D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ in \_ float4 \_ ungenau-Funktion</span><span class="sxs-lookup"><span data-stu-id="31eee-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="31eee-106">Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="31eee-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="31eee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="31eee-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="31eee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="31eee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31eee-109">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="31eee-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="31eee-110">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="31eee-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31eee-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31eee-111">Return value</span></span>

<span data-ttu-id="31eee-112">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="31eee-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="31eee-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31eee-113">Remarks</span></span>

<span data-ttu-id="31eee-114">Diese Funktion verwendet shaderanweisungen, die keine hohe genug Genauigkeit aufweisen, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31eee-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="31eee-115">Die Alternative Funktion [**D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ to \_ float4**](d3dx-r10g10b10a2-unorm-to-float4.md) verwendet eine im Shader gespeicherte Such Tabelle, um eine exakte sRGB-Konvertierung für die Gleit Komma Zahl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31eee-115">The alternative function [**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="31eee-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="31eee-116">Requirements</span></span>



| <span data-ttu-id="31eee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31eee-117">Requirement</span></span> | <span data-ttu-id="31eee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="31eee-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31eee-119">Header</span><span class="sxs-lookup"><span data-stu-id="31eee-119">Header</span></span><br/> | <dl> <span data-ttu-id="31eee-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31eee-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31eee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31eee-122">Funktionen</span><span class="sxs-lookup"><span data-stu-id="31eee-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="31eee-123">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="31eee-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





