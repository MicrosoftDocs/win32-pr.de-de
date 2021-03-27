---
title: 'Texture1DArray:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture1DArray:: Operator-Funktion'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
keywords:
- Operator Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981632"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="b9ae4-105">Texture1DArray:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9ae4-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="b9ae4-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ae4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9ae4-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="b9ae4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9ae4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ae4-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ae4-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ae4-110">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="b9ae4-110">Type: **uint2**</span></span>

<span data-ttu-id="b9ae4-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-111">The index position.</span></span> <span data-ttu-id="b9ae4-112">Die erste Komponente enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="b9ae4-113">Die zweite Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ae4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9ae4-114">Return value</span></span>

<span data-ttu-id="b9ae4-115">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="b9ae4-115">Type: **R**</span></span>

<span data-ttu-id="b9ae4-116">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9ae4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9ae4-117">Remarks</span></span>

<span data-ttu-id="b9ae4-118">Diese Methode greift immer auf die erste MIP-Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="b9ae4-119">Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**MIP. Operator \[ \] \[ \]**](sm5-object-texture1darray-mipsoperatorindex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b9ae4-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="b9ae4-120">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b9ae4-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b9ae4-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b9ae4-121">Vertex</span></span> | <span data-ttu-id="b9ae4-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="b9ae4-122">Hull</span></span> | <span data-ttu-id="b9ae4-123">Domain</span><span class="sxs-lookup"><span data-stu-id="b9ae4-123">Domain</span></span> | <span data-ttu-id="b9ae4-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b9ae4-124">Geometry</span></span> | <span data-ttu-id="b9ae4-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="b9ae4-125">Pixel</span></span> | <span data-ttu-id="b9ae4-126">Compute</span><span class="sxs-lookup"><span data-stu-id="b9ae4-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b9ae4-127">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-127">x</span></span>      | <span data-ttu-id="b9ae4-128">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-128">x</span></span>    | <span data-ttu-id="b9ae4-129">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-129">x</span></span>      | <span data-ttu-id="b9ae4-130">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-130">x</span></span>        | <span data-ttu-id="b9ae4-131">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-131">x</span></span>     | <span data-ttu-id="b9ae4-132">x</span><span class="sxs-lookup"><span data-stu-id="b9ae4-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b9ae4-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9ae4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ae4-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b9ae4-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="b9ae4-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b9ae4-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




