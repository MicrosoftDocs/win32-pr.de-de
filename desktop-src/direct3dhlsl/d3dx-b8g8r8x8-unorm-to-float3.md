---
title: D3DX_B8G8R8X8_UNORM_to_FLOAT3-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm-Shader-Daten in eine XMFLOAT3.
ms.assetid: 0987d71a-89a4-4751-9f32-08e2490204d2
keywords:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6397f271899c2a8d73ed1ba84a04f3c02514fb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982108"
---
# <a name="d3dx_b8g8r8x8_unorm_to_float3-function"></a><span data-ttu-id="e460b-104">D3DX \_ B8G8R8X8 \_ unorm \_ to \_ FLOAT3-Funktion</span><span class="sxs-lookup"><span data-stu-id="e460b-104">D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3 function</span></span>

<span data-ttu-id="e460b-105">Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm-Shader-Daten in eine XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="e460b-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="e460b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e460b-106">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e460b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e460b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e460b-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="e460b-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e460b-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="e460b-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e460b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e460b-110">Return value</span></span>

<span data-ttu-id="e460b-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="e460b-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e460b-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e460b-112">Requirements</span></span>



| <span data-ttu-id="e460b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e460b-113">Requirement</span></span> | <span data-ttu-id="e460b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e460b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e460b-115">Header</span><span class="sxs-lookup"><span data-stu-id="e460b-115">Header</span></span><br/> | <dl> <span data-ttu-id="e460b-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="e460b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e460b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e460b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e460b-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="e460b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e460b-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="e460b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





