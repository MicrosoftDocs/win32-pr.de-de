---
title: 'Texture1DArray:: MIPS. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture1DArray:: MIPS. Operator-Funktion'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050786"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="618c9-105">Texture1DArray:: MIPS. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="618c9-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="618c9-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="618c9-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="618c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="618c9-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="618c9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="618c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="618c9-109">*mipslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="618c9-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="618c9-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="618c9-110">Type: **uint**</span></span>

<span data-ttu-id="618c9-111">Der MIP-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="618c9-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="618c9-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="618c9-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="618c9-113">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="618c9-113">Type: **uint2**</span></span>

<span data-ttu-id="618c9-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="618c9-114">The index position.</span></span> <span data-ttu-id="618c9-115">Die erste Komponente enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="618c9-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="618c9-116">Die zweite Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="618c9-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="618c9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="618c9-117">Return value</span></span>

<span data-ttu-id="618c9-118">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="618c9-118">Type: **R**</span></span>

<span data-ttu-id="618c9-119">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="618c9-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="618c9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="618c9-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="618c9-121">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="618c9-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="618c9-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="618c9-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="618c9-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="618c9-123">Vertex</span></span> | <span data-ttu-id="618c9-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="618c9-124">Hull</span></span> | <span data-ttu-id="618c9-125">Domain</span><span class="sxs-lookup"><span data-stu-id="618c9-125">Domain</span></span> | <span data-ttu-id="618c9-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="618c9-126">Geometry</span></span> | <span data-ttu-id="618c9-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="618c9-127">Pixel</span></span> | <span data-ttu-id="618c9-128">Compute</span><span class="sxs-lookup"><span data-stu-id="618c9-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="618c9-129">x</span><span class="sxs-lookup"><span data-stu-id="618c9-129">x</span></span>      | <span data-ttu-id="618c9-130">x</span><span class="sxs-lookup"><span data-stu-id="618c9-130">x</span></span>    | <span data-ttu-id="618c9-131">x</span><span class="sxs-lookup"><span data-stu-id="618c9-131">x</span></span>      | <span data-ttu-id="618c9-132">x</span><span class="sxs-lookup"><span data-stu-id="618c9-132">x</span></span>        | <span data-ttu-id="618c9-133">x</span><span class="sxs-lookup"><span data-stu-id="618c9-133">x</span></span>     | <span data-ttu-id="618c9-134">x</span><span class="sxs-lookup"><span data-stu-id="618c9-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="618c9-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="618c9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="618c9-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="618c9-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="618c9-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="618c9-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




