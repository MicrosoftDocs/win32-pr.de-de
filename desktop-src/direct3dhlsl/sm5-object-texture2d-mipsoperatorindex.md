---
title: 'Texture2D:: MIPS. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2D:: MIPS. Operator-Funktion'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
keywords:
- MIPS. Operator Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981169"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="bb309-105">Texture2D:: MIPS. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb309-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="bb309-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="bb309-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb309-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb309-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="bb309-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb309-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb309-109">*mipslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb309-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb309-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="bb309-110">Type: **uint**</span></span>

<span data-ttu-id="bb309-111">Der MIP-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="bb309-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="bb309-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb309-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb309-113">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="bb309-113">Type: **uint2**</span></span>

<span data-ttu-id="bb309-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="bb309-114">The index position.</span></span> <span data-ttu-id="bb309-115">Enthält die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="bb309-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb309-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb309-116">Return value</span></span>

<span data-ttu-id="bb309-117">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="bb309-117">Type: **R**</span></span>

<span data-ttu-id="bb309-118">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="bb309-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb309-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb309-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="bb309-120">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="bb309-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="bb309-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bb309-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bb309-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="bb309-122">Vertex</span></span> | <span data-ttu-id="bb309-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="bb309-123">Hull</span></span> | <span data-ttu-id="bb309-124">Domain</span><span class="sxs-lookup"><span data-stu-id="bb309-124">Domain</span></span> | <span data-ttu-id="bb309-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="bb309-125">Geometry</span></span> | <span data-ttu-id="bb309-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="bb309-126">Pixel</span></span> | <span data-ttu-id="bb309-127">Compute</span><span class="sxs-lookup"><span data-stu-id="bb309-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bb309-128">x</span><span class="sxs-lookup"><span data-stu-id="bb309-128">x</span></span>      | <span data-ttu-id="bb309-129">x</span><span class="sxs-lookup"><span data-stu-id="bb309-129">x</span></span>    | <span data-ttu-id="bb309-130">x</span><span class="sxs-lookup"><span data-stu-id="bb309-130">x</span></span>      | <span data-ttu-id="bb309-131">x</span><span class="sxs-lookup"><span data-stu-id="bb309-131">x</span></span>        | <span data-ttu-id="bb309-132">x</span><span class="sxs-lookup"><span data-stu-id="bb309-132">x</span></span>     | <span data-ttu-id="bb309-133">x</span><span class="sxs-lookup"><span data-stu-id="bb309-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bb309-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bb309-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb309-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bb309-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="bb309-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="bb309-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




