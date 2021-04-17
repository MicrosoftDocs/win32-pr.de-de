---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM-Funktion
description: Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ snorm.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355777"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="429c5-104">D3DX \_ float4 \_ to \_ R8G8B8A8 \_ snorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="429c5-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="429c5-105">Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ snorm.</span><span class="sxs-lookup"><span data-stu-id="429c5-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="429c5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="429c5-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="429c5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="429c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429c5-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="429c5-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="429c5-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="429c5-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="429c5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="429c5-110">Return value</span></span>

<span data-ttu-id="429c5-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="429c5-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="429c5-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="429c5-112">Requirements</span></span>



| <span data-ttu-id="429c5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="429c5-113">Requirement</span></span> | <span data-ttu-id="429c5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="429c5-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="429c5-115">Header</span><span class="sxs-lookup"><span data-stu-id="429c5-115">Header</span></span><br/> | <dl> <span data-ttu-id="429c5-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="429c5-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="429c5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="429c5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429c5-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="429c5-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="429c5-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="429c5-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





