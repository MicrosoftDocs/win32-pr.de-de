---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM-Funktion
description: Packt das angegebene XMFLOAT3 in ein DXGI- \_ Format \_ B8G8R8X8 \_ unorm uint.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995902"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a><span data-ttu-id="4cf0d-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ unorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="4cf0d-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM function</span></span>

<span data-ttu-id="4cf0d-105">Packt das angegebene XMFLOAT3 in ein DXGI- \_ Format \_ B8G8R8X8 \_ unorm uint.</span><span class="sxs-lookup"><span data-stu-id="4cf0d-105">Packs the given XMFLOAT3 into a DXGI\_FORMAT\_B8G8R8X8\_UNORM UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf0d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cf0d-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4cf0d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cf0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf0d-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="4cf0d-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4cf0d-109">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="4cf0d-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf0d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cf0d-110">Return value</span></span>

<span data-ttu-id="4cf0d-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="4cf0d-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf0d-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4cf0d-112">Requirements</span></span>



| <span data-ttu-id="4cf0d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cf0d-113">Requirement</span></span> | <span data-ttu-id="4cf0d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4cf0d-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf0d-115">Header</span><span class="sxs-lookup"><span data-stu-id="4cf0d-115">Header</span></span><br/> | <dl> <span data-ttu-id="4cf0d-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="4cf0d-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf0d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cf0d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf0d-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="4cf0d-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4cf0d-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="4cf0d-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





