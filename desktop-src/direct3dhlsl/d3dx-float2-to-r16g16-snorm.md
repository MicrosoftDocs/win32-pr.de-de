---
title: D3DX_FLOAT2_to_R16G16_SNORM-Funktion
description: Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ snorm.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961636"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="97c1f-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ snorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="97c1f-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="97c1f-105">Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ snorm.</span><span class="sxs-lookup"><span data-stu-id="97c1f-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c1f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="97c1f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="97c1f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="97c1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c1f-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="97c1f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="97c1f-109">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="97c1f-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c1f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97c1f-110">Return value</span></span>

<span data-ttu-id="97c1f-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="97c1f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c1f-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="97c1f-112">Requirements</span></span>



| <span data-ttu-id="97c1f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97c1f-113">Requirement</span></span> | <span data-ttu-id="97c1f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="97c1f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c1f-115">Header</span><span class="sxs-lookup"><span data-stu-id="97c1f-115">Header</span></span><br/> | <dl> <span data-ttu-id="97c1f-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="97c1f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c1f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97c1f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c1f-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="97c1f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="97c1f-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="97c1f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





