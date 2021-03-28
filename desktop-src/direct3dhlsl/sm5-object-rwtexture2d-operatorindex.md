---
title: 'RWTexture2D:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | RWTexture2D:: Operator-Funktion'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
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
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981633"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="2c9fd-105">RWTexture2D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c9fd-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="2c9fd-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c9fd-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="2c9fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c9fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c9fd-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c9fd-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c9fd-110">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="2c9fd-110">Type: **uint2**</span></span>

<span data-ttu-id="2c9fd-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-111">The index position.</span></span> <span data-ttu-id="2c9fd-112">Enthält die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c9fd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c9fd-113">Return value</span></span>

<span data-ttu-id="2c9fd-114">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="2c9fd-114">Type: **R**</span></span>

<span data-ttu-id="2c9fd-115">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c9fd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c9fd-116">Remarks</span></span>

<span data-ttu-id="2c9fd-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2c9fd-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2c9fd-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2c9fd-118">Vertex</span></span> | <span data-ttu-id="2c9fd-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="2c9fd-119">Hull</span></span> | <span data-ttu-id="2c9fd-120">Domain</span><span class="sxs-lookup"><span data-stu-id="2c9fd-120">Domain</span></span> | <span data-ttu-id="2c9fd-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2c9fd-121">Geometry</span></span> | <span data-ttu-id="2c9fd-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c9fd-122">Pixel</span></span> | <span data-ttu-id="2c9fd-123">Compute</span><span class="sxs-lookup"><span data-stu-id="2c9fd-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2c9fd-124">x</span><span class="sxs-lookup"><span data-stu-id="2c9fd-124">x</span></span>     | <span data-ttu-id="2c9fd-125">x</span><span class="sxs-lookup"><span data-stu-id="2c9fd-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2c9fd-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c9fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9fd-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="2c9fd-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="2c9fd-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2c9fd-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




