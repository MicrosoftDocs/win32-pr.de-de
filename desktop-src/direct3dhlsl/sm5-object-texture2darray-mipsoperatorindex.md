---
title: 'Texture2DArray:: MIPS. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2DArray:: MIPS. Operator-Funktion'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761826"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="41ea8-105">Texture2DArray:: MIPS. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="41ea8-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="41ea8-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="41ea8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ea8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="41ea8-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="41ea8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="41ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ea8-109">*mipslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41ea8-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ea8-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="41ea8-110">Type: **uint**</span></span>

<span data-ttu-id="41ea8-111">Der MIP-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="41ea8-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="41ea8-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41ea8-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ea8-113">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="41ea8-113">Type: **uint3**</span></span>

<span data-ttu-id="41ea8-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="41ea8-114">The index position.</span></span> <span data-ttu-id="41ea8-115">Die erste und die zweite Komponente enthalten die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="41ea8-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="41ea8-116">Die dritte Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="41ea8-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ea8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41ea8-117">Return value</span></span>

<span data-ttu-id="41ea8-118">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="41ea8-118">Type: **R**</span></span>

<span data-ttu-id="41ea8-119">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="41ea8-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ea8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41ea8-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="41ea8-121">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="41ea8-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="41ea8-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="41ea8-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="41ea8-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="41ea8-123">Vertex</span></span> | <span data-ttu-id="41ea8-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="41ea8-124">Hull</span></span> | <span data-ttu-id="41ea8-125">Domain</span><span class="sxs-lookup"><span data-stu-id="41ea8-125">Domain</span></span> | <span data-ttu-id="41ea8-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="41ea8-126">Geometry</span></span> | <span data-ttu-id="41ea8-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="41ea8-127">Pixel</span></span> | <span data-ttu-id="41ea8-128">Compute</span><span class="sxs-lookup"><span data-stu-id="41ea8-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="41ea8-129">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-129">x</span></span>      | <span data-ttu-id="41ea8-130">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-130">x</span></span>    | <span data-ttu-id="41ea8-131">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-131">x</span></span>      | <span data-ttu-id="41ea8-132">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-132">x</span></span>        | <span data-ttu-id="41ea8-133">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-133">x</span></span>     | <span data-ttu-id="41ea8-134">x</span><span class="sxs-lookup"><span data-stu-id="41ea8-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="41ea8-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="41ea8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ea8-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="41ea8-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="41ea8-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="41ea8-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




