---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB-Funktion
description: Packt den angegebenen XMFLOAT3 zurück in ein DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995854"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="0b8ca-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ unorm \_ sRGB-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b8ca-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="0b8ca-105">Packt den angegebenen XMFLOAT3 zurück in ein DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="0b8ca-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8ca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b8ca-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="0b8ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b8ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8ca-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="0b8ca-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="0b8ca-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="0b8ca-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b8ca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b8ca-110">Return value</span></span>

<span data-ttu-id="0b8ca-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="0b8ca-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8ca-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0b8ca-112">Requirements</span></span>



| <span data-ttu-id="0b8ca-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b8ca-113">Requirement</span></span> | <span data-ttu-id="0b8ca-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0b8ca-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8ca-115">Header</span><span class="sxs-lookup"><span data-stu-id="0b8ca-115">Header</span></span><br/> | <dl> <span data-ttu-id="0b8ca-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="0b8ca-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b8ca-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8ca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8ca-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="0b8ca-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="0b8ca-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="0b8ca-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





