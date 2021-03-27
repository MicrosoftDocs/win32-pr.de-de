---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion
description: Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm-Shader-Daten in eine XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762324"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="74e92-105">D3DX \_ float4 \_ to \_ R8G8B8A8 \_ unorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="74e92-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="74e92-106">Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="74e92-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e92-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74e92-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="74e92-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74e92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e92-109">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="74e92-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="74e92-110">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="74e92-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e92-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74e92-111">Return value</span></span>

<span data-ttu-id="74e92-112">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="74e92-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e92-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="74e92-113">Requirements</span></span>



| <span data-ttu-id="74e92-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74e92-114">Requirement</span></span> | <span data-ttu-id="74e92-115">Wert</span><span class="sxs-lookup"><span data-stu-id="74e92-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e92-116">Header</span><span class="sxs-lookup"><span data-stu-id="74e92-116">Header</span></span><br/> | <dl> <span data-ttu-id="74e92-117"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="74e92-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e92-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74e92-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e92-119">Funktionen</span><span class="sxs-lookup"><span data-stu-id="74e92-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="74e92-120">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="74e92-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





