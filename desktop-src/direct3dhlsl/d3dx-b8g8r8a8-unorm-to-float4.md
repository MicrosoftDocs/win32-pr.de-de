---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982114"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a><span data-ttu-id="51dcc-104">D3DX \_ B8G8R8A8 \_ unorm \_ to \_ float4-Funktion</span><span class="sxs-lookup"><span data-stu-id="51dcc-104">D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="51dcc-105">Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="51dcc-105">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="51dcc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51dcc-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="51dcc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51dcc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51dcc-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="51dcc-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="51dcc-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="51dcc-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51dcc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51dcc-110">Return value</span></span>

<span data-ttu-id="51dcc-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="51dcc-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="51dcc-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="51dcc-112">Requirements</span></span>



| <span data-ttu-id="51dcc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51dcc-113">Requirement</span></span> | <span data-ttu-id="51dcc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="51dcc-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51dcc-115">Header</span><span class="sxs-lookup"><span data-stu-id="51dcc-115">Header</span></span><br/> | <dl> <span data-ttu-id="51dcc-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="51dcc-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51dcc-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51dcc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51dcc-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="51dcc-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="51dcc-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="51dcc-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





