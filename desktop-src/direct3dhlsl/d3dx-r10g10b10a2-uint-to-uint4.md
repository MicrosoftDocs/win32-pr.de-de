---
title: D3DX_R10G10B10A2_UINT_to_UINT4-Funktion
description: Entpackt das DXGI- \_ Format \_ R10G10B10A2 \_ uint-Shader-Daten in eine XMINT4.
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- D3DX_R10G10B10A2_UINT_to_UINT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378b013ad077c787253b4a58f24082d1c64b416f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982492"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a><span data-ttu-id="4a1cd-104">D3DX \_ R10G10B10A2 \_ uint \_ to \_ UINT4-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a1cd-104">D3DX\_R10G10B10A2\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="4a1cd-105">Entpackt das DXGI- \_ Format \_ R10G10B10A2 \_ uint-Shader-Daten in eine XMINT4.</span><span class="sxs-lookup"><span data-stu-id="4a1cd-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1cd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a1cd-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4a1cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a1cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1cd-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="4a1cd-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1cd-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="4a1cd-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1cd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a1cd-110">Return value</span></span>

<span data-ttu-id="4a1cd-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="4a1cd-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1cd-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4a1cd-112">Requirements</span></span>



| <span data-ttu-id="4a1cd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a1cd-113">Requirement</span></span> | <span data-ttu-id="4a1cd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4a1cd-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1cd-115">Header</span><span class="sxs-lookup"><span data-stu-id="4a1cd-115">Header</span></span><br/> | <dl> <span data-ttu-id="4a1cd-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="4a1cd-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1cd-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a1cd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1cd-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="4a1cd-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4a1cd-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="4a1cd-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





