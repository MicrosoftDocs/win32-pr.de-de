---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB-Funktion
description: Packt das angegebene XMFLOAT4 in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219640"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a><span data-ttu-id="a9a7b-104">D3DX \_ float4 \_ to \_ B8G8R8A8 \_ unorm \_ sRGB-Funktion</span><span class="sxs-lookup"><span data-stu-id="a9a7b-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="a9a7b-105">Packt das angegebene XMFLOAT4 in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB uint.</span><span class="sxs-lookup"><span data-stu-id="a9a7b-105">Packs the given XMFLOAT4 into a DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a7b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a7b-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="a9a7b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a7b-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="a9a7b-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a7b-109">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="a9a7b-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a7b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9a7b-110">Return value</span></span>

<span data-ttu-id="a9a7b-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="a9a7b-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a7b-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a9a7b-112">Requirements</span></span>



| <span data-ttu-id="a9a7b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9a7b-113">Requirement</span></span> | <span data-ttu-id="a9a7b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a9a7b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a7b-115">Header</span><span class="sxs-lookup"><span data-stu-id="a9a7b-115">Header</span></span><br/> | <dl> <span data-ttu-id="a9a7b-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="a9a7b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a7b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a7b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a7b-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="a9a7b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a9a7b-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="a9a7b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





