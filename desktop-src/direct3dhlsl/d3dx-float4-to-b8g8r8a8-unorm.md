---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM-Funktion
description: Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm.
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982197"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a><span data-ttu-id="144e0-104">D3DX \_ float4 \_ to \_ B8G8R8A8 \_ unorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="144e0-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM function</span></span>

<span data-ttu-id="144e0-105">Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="144e0-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_B8G8R8A8\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="144e0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="144e0-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="144e0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="144e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="144e0-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="144e0-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="144e0-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="144e0-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="144e0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="144e0-110">Return value</span></span>

<span data-ttu-id="144e0-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="144e0-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="144e0-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="144e0-112">Requirements</span></span>



| <span data-ttu-id="144e0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="144e0-113">Requirement</span></span> | <span data-ttu-id="144e0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="144e0-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144e0-115">Header</span><span class="sxs-lookup"><span data-stu-id="144e0-115">Header</span></span><br/> | <dl> <span data-ttu-id="144e0-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="144e0-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144e0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="144e0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144e0-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="144e0-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="144e0-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="144e0-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





