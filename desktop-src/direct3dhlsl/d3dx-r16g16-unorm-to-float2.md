---
title: D3DX_R16G16_UNORM_to_FLOAT2-Funktion
description: Entpackt DXGI- \_ Format \_ R16G16 \_ unorm-Shader-Daten in eine XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- D3DX_R16G16_UNORM_to_FLOAT2-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354556"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a><span data-ttu-id="6b8ba-104">D3DX \_ R16G16 \_ unorm \_ to \_ FLOAT2-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b8ba-104">D3DX\_R16G16\_UNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="6b8ba-105">Entpackt DXGI- \_ Format \_ R16G16 \_ unorm-Shader-Daten in eine XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-105">Unpacks DXGI\_FORMAT\_R16G16\_UNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8ba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b8ba-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="6b8ba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b8ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8ba-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="6b8ba-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8ba-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8ba-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b8ba-110">Return value</span></span>

<span data-ttu-id="6b8ba-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8ba-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6b8ba-112">Requirements</span></span>



| <span data-ttu-id="6b8ba-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b8ba-113">Requirement</span></span> | <span data-ttu-id="6b8ba-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6b8ba-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8ba-115">Header</span><span class="sxs-lookup"><span data-stu-id="6b8ba-115">Header</span></span><br/> | <dl> <span data-ttu-id="6b8ba-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="6b8ba-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8ba-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b8ba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8ba-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="6b8ba-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="6b8ba-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="6b8ba-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





