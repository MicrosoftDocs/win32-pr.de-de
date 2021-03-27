---
title: 'Texture2DArray:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2DArray:: Operator-Funktion'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050748"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="74879-105">Texture2DArray:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="74879-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="74879-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="74879-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="74879-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74879-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="74879-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74879-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74879-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74879-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74879-110">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="74879-110">Type: **uint3**</span></span>

<span data-ttu-id="74879-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="74879-111">The index position.</span></span> <span data-ttu-id="74879-112">Die erste und die zweite Komponente enthalten die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="74879-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="74879-113">Die dritte Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="74879-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74879-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74879-114">Return value</span></span>

<span data-ttu-id="74879-115">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="74879-115">Type: **R**</span></span>

<span data-ttu-id="74879-116">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="74879-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="74879-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74879-117">Remarks</span></span>

<span data-ttu-id="74879-118">Diese Methode greift immer auf die erste MIP-Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="74879-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="74879-119">Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2darray-mipsoperatorindex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="74879-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="74879-120">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74879-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="74879-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="74879-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="74879-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="74879-122">Vertex</span></span> | <span data-ttu-id="74879-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="74879-123">Hull</span></span> | <span data-ttu-id="74879-124">Domain</span><span class="sxs-lookup"><span data-stu-id="74879-124">Domain</span></span> | <span data-ttu-id="74879-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="74879-125">Geometry</span></span> | <span data-ttu-id="74879-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="74879-126">Pixel</span></span> | <span data-ttu-id="74879-127">Compute</span><span class="sxs-lookup"><span data-stu-id="74879-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="74879-128">x</span><span class="sxs-lookup"><span data-stu-id="74879-128">x</span></span>      | <span data-ttu-id="74879-129">x</span><span class="sxs-lookup"><span data-stu-id="74879-129">x</span></span>    | <span data-ttu-id="74879-130">x</span><span class="sxs-lookup"><span data-stu-id="74879-130">x</span></span>      | <span data-ttu-id="74879-131">x</span><span class="sxs-lookup"><span data-stu-id="74879-131">x</span></span>        | <span data-ttu-id="74879-132">x</span><span class="sxs-lookup"><span data-stu-id="74879-132">x</span></span>     | <span data-ttu-id="74879-133">x</span><span class="sxs-lookup"><span data-stu-id="74879-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="74879-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74879-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74879-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="74879-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="74879-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="74879-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




