---
title: D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion
description: Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm-Shader-Daten in eine XMFLOAT4. | D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e24b9f29d2e54f62582407e8ad40488032f8a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354547"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a><span data-ttu-id="b692f-105">D3DX \_ R8G8B8A8 \_ unorm \_ to \_ float4-Funktion</span><span class="sxs-lookup"><span data-stu-id="b692f-105">D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="b692f-106">Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="b692f-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="b692f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b692f-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="b692f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b692f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b692f-109">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="b692f-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="b692f-110">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="b692f-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b692f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b692f-111">Return value</span></span>

<span data-ttu-id="b692f-112">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="b692f-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b692f-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b692f-113">Requirements</span></span>



| <span data-ttu-id="b692f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b692f-114">Requirement</span></span> | <span data-ttu-id="b692f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b692f-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b692f-116">Header</span><span class="sxs-lookup"><span data-stu-id="b692f-116">Header</span></span><br/> | <dl> <span data-ttu-id="b692f-117"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="b692f-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b692f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b692f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b692f-119">Funktionen</span><span class="sxs-lookup"><span data-stu-id="b692f-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="b692f-120">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="b692f-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





