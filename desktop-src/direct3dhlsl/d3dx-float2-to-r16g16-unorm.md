---
title: D3DX_FLOAT2_to_R16G16_UNORM-Funktion
description: Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ unorm.
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- D3DX_FLOAT2_to_R16G16_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995907"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a><span data-ttu-id="42a98-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ unorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="42a98-104">D3DX\_FLOAT2\_to\_R16G16\_UNORM function</span></span>

<span data-ttu-id="42a98-105">Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="42a98-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a98-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a98-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="42a98-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a98-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="42a98-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="42a98-109">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="42a98-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a98-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42a98-110">Return value</span></span>

<span data-ttu-id="42a98-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="42a98-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a98-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="42a98-112">Requirements</span></span>



| <span data-ttu-id="42a98-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a98-113">Requirement</span></span> | <span data-ttu-id="42a98-114">Wert</span><span class="sxs-lookup"><span data-stu-id="42a98-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a98-115">Header</span><span class="sxs-lookup"><span data-stu-id="42a98-115">Header</span></span><br/> | <dl> <span data-ttu-id="42a98-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="42a98-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a98-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a98-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a98-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="42a98-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="42a98-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="42a98-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





