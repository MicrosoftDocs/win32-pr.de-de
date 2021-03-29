---
title: 'Texture2D:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2D:: Operator-Funktion'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981704"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="3243c-105">Texture2D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="3243c-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="3243c-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="3243c-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3243c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3243c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="3243c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3243c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3243c-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3243c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3243c-110">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="3243c-110">Type: **uint2**</span></span>

<span data-ttu-id="3243c-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="3243c-111">The index position.</span></span> <span data-ttu-id="3243c-112">Enthält die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="3243c-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3243c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3243c-113">Return value</span></span>

<span data-ttu-id="3243c-114">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="3243c-114">Type: **R**</span></span>

<span data-ttu-id="3243c-115">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="3243c-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3243c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3243c-116">Remarks</span></span>

<span data-ttu-id="3243c-117">Diese Methode greift immer auf die erste MIP-Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="3243c-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="3243c-118">Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3243c-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="3243c-119">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3243c-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3243c-120">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3243c-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3243c-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3243c-121">Vertex</span></span> | <span data-ttu-id="3243c-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="3243c-122">Hull</span></span> | <span data-ttu-id="3243c-123">Domain</span><span class="sxs-lookup"><span data-stu-id="3243c-123">Domain</span></span> | <span data-ttu-id="3243c-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3243c-124">Geometry</span></span> | <span data-ttu-id="3243c-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="3243c-125">Pixel</span></span> | <span data-ttu-id="3243c-126">Compute</span><span class="sxs-lookup"><span data-stu-id="3243c-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3243c-127">x</span><span class="sxs-lookup"><span data-stu-id="3243c-127">x</span></span>      | <span data-ttu-id="3243c-128">x</span><span class="sxs-lookup"><span data-stu-id="3243c-128">x</span></span>    | <span data-ttu-id="3243c-129">x</span><span class="sxs-lookup"><span data-stu-id="3243c-129">x</span></span>      | <span data-ttu-id="3243c-130">x</span><span class="sxs-lookup"><span data-stu-id="3243c-130">x</span></span>        | <span data-ttu-id="3243c-131">x</span><span class="sxs-lookup"><span data-stu-id="3243c-131">x</span></span>     | <span data-ttu-id="3243c-132">x</span><span class="sxs-lookup"><span data-stu-id="3243c-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3243c-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3243c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3243c-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3243c-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="3243c-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3243c-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




