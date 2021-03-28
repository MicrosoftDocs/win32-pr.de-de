---
title: 'Texture3D:: MIPS. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture3D:: MIPS. Operator-Funktion'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219189"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="4a388-105">Texture3D:: MIPS. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a388-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="4a388-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="4a388-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a388-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a388-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="4a388-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a388-109">*mipslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a388-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a388-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="4a388-110">Type: **uint**</span></span>

<span data-ttu-id="4a388-111">Der MIP-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="4a388-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="4a388-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a388-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a388-113">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="4a388-113">Type: **uint3**</span></span>

<span data-ttu-id="4a388-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="4a388-114">The index position.</span></span> <span data-ttu-id="4a388-115">Enthält die Koordinaten (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="4a388-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a388-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a388-116">Return value</span></span>

<span data-ttu-id="4a388-117">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="4a388-117">Type: **R**</span></span>

<span data-ttu-id="4a388-118">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="4a388-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a388-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a388-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="4a388-120">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="4a388-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="4a388-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4a388-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4a388-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4a388-122">Vertex</span></span> | <span data-ttu-id="4a388-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="4a388-123">Hull</span></span> | <span data-ttu-id="4a388-124">Domain</span><span class="sxs-lookup"><span data-stu-id="4a388-124">Domain</span></span> | <span data-ttu-id="4a388-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4a388-125">Geometry</span></span> | <span data-ttu-id="4a388-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="4a388-126">Pixel</span></span> | <span data-ttu-id="4a388-127">Compute</span><span class="sxs-lookup"><span data-stu-id="4a388-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4a388-128">x</span><span class="sxs-lookup"><span data-stu-id="4a388-128">x</span></span>      | <span data-ttu-id="4a388-129">x</span><span class="sxs-lookup"><span data-stu-id="4a388-129">x</span></span>    | <span data-ttu-id="4a388-130">x</span><span class="sxs-lookup"><span data-stu-id="4a388-130">x</span></span>      | <span data-ttu-id="4a388-131">x</span><span class="sxs-lookup"><span data-stu-id="4a388-131">x</span></span>        | <span data-ttu-id="4a388-132">x</span><span class="sxs-lookup"><span data-stu-id="4a388-132">x</span></span>     | <span data-ttu-id="4a388-133">x</span><span class="sxs-lookup"><span data-stu-id="4a388-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4a388-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a388-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a388-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4a388-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="4a388-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4a388-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




