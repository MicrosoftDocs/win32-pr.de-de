---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4-Funktion
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91311bb83aa034410361bea631aa79f86737ff65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354297"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="a79db-105">D3DX \_ B8G8R8A8 \_ unorm \_ sRGB \_ in die \_ float4-Funktion</span><span class="sxs-lookup"><span data-stu-id="a79db-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="a79db-106">Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="a79db-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a79db-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="a79db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a79db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a79db-109">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="a79db-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a79db-110">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="a79db-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a79db-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a79db-111">Return value</span></span>

<span data-ttu-id="a79db-112">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="a79db-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a79db-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a79db-113">Requirements</span></span>



| <span data-ttu-id="a79db-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a79db-114">Requirement</span></span> | <span data-ttu-id="a79db-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a79db-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a79db-116">Header</span><span class="sxs-lookup"><span data-stu-id="a79db-116">Header</span></span><br/> | <dl> <span data-ttu-id="a79db-117"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="a79db-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a79db-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a79db-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79db-119">Funktionen</span><span class="sxs-lookup"><span data-stu-id="a79db-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a79db-120">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="a79db-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





