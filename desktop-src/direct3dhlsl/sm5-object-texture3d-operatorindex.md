---
title: 'Texture3D:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture3D:: Operator-Funktion'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761724"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="f83d7-105">Texture3D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="f83d7-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="f83d7-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="f83d7-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f83d7-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="f83d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f83d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83d7-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83d7-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83d7-110">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="f83d7-110">Type: **uint3**</span></span>

<span data-ttu-id="f83d7-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="f83d7-111">The index position.</span></span> <span data-ttu-id="f83d7-112">Enthält die Koordinaten (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="f83d7-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f83d7-113">Return value</span></span>

<span data-ttu-id="f83d7-114">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="f83d7-114">Type: **R**</span></span>

<span data-ttu-id="f83d7-115">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="f83d7-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="f83d7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f83d7-116">Remarks</span></span>

<span data-ttu-id="f83d7-117">Diese Methode greift immer auf die erste MIP-Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="f83d7-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="f83d7-118">Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen den [**\[ \] \[ \] MIP.-Operator**](sm5-object-texture3d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="f83d7-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="f83d7-119">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f83d7-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f83d7-120">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f83d7-120">Vertex</span></span> | <span data-ttu-id="f83d7-121">Hülle</span><span class="sxs-lookup"><span data-stu-id="f83d7-121">Hull</span></span> | <span data-ttu-id="f83d7-122">Domain</span><span class="sxs-lookup"><span data-stu-id="f83d7-122">Domain</span></span> | <span data-ttu-id="f83d7-123">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f83d7-123">Geometry</span></span> | <span data-ttu-id="f83d7-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="f83d7-124">Pixel</span></span> | <span data-ttu-id="f83d7-125">Compute</span><span class="sxs-lookup"><span data-stu-id="f83d7-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f83d7-126">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-126">x</span></span>      | <span data-ttu-id="f83d7-127">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-127">x</span></span>    | <span data-ttu-id="f83d7-128">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-128">x</span></span>      | <span data-ttu-id="f83d7-129">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-129">x</span></span>        | <span data-ttu-id="f83d7-130">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-130">x</span></span>     | <span data-ttu-id="f83d7-131">x</span><span class="sxs-lookup"><span data-stu-id="f83d7-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f83d7-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f83d7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83d7-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f83d7-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="f83d7-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f83d7-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




