---
title: D3DX_UINT2_to_R16G16_UINT-Funktion
description: Packt den angegebenen XMUINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ uint.
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- D3DX_UINT2_to_R16G16_UINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995884"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a><span data-ttu-id="ed787-104">D3DX \_ UINT2 \_ to \_ R16G16 \_ uint-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed787-104">D3DX\_UINT2\_to\_R16G16\_UINT function</span></span>

<span data-ttu-id="ed787-105">Packt den angegebenen XMUINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="ed787-105">Packs the given XMUINT2 back into a DXGI\_FORMAT\_R16G16\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed787-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed787-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ed787-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed787-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed787-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="ed787-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ed787-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="ed787-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed787-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed787-110">Return value</span></span>

<span data-ttu-id="ed787-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="ed787-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed787-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ed787-112">Requirements</span></span>



| <span data-ttu-id="ed787-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed787-113">Requirement</span></span> | <span data-ttu-id="ed787-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ed787-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed787-115">Header</span><span class="sxs-lookup"><span data-stu-id="ed787-115">Header</span></span><br/> | <dl> <span data-ttu-id="ed787-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="ed787-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed787-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed787-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed787-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="ed787-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ed787-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="ed787-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





