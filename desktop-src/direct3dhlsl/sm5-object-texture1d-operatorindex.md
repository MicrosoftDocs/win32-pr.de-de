---
title: 'Texture1D:: Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable für ein Texture1D-Wert zurück.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102715"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="47f1f-104">Texture1D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="47f1f-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="47f1f-105">Gibt eine schreibgeschützte Ressourcen Variable für ein [**Texture1D**](sm5-object-texture1d.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="47f1f-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47f1f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f1f-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="47f1f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47f1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f1f-108">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47f1f-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f1f-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="47f1f-109">Type: **uint**</span></span>

<span data-ttu-id="47f1f-110">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="47f1f-110">The index position.</span></span> <span data-ttu-id="47f1f-111">Enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="47f1f-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f1f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47f1f-112">Return value</span></span>

<span data-ttu-id="47f1f-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="47f1f-113">Type: **R**</span></span>

<span data-ttu-id="47f1f-114">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="47f1f-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="47f1f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47f1f-115">Remarks</span></span>

<span data-ttu-id="47f1f-116">Diese Methode greift immer auf die erste MIP-Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="47f1f-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="47f1f-117">Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen den [**\[ \] \[ \] MIP.-Operator**](sm5-object-texture1d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="47f1f-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="47f1f-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="47f1f-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="47f1f-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="47f1f-119">Vertex</span></span> | <span data-ttu-id="47f1f-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="47f1f-120">Hull</span></span> | <span data-ttu-id="47f1f-121">Domain</span><span class="sxs-lookup"><span data-stu-id="47f1f-121">Domain</span></span> | <span data-ttu-id="47f1f-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="47f1f-122">Geometry</span></span> | <span data-ttu-id="47f1f-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="47f1f-123">Pixel</span></span> | <span data-ttu-id="47f1f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="47f1f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="47f1f-125">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-125">x</span></span>      | <span data-ttu-id="47f1f-126">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-126">x</span></span>    | <span data-ttu-id="47f1f-127">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-127">x</span></span>      | <span data-ttu-id="47f1f-128">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-128">x</span></span>        | <span data-ttu-id="47f1f-129">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-129">x</span></span>     | <span data-ttu-id="47f1f-130">x</span><span class="sxs-lookup"><span data-stu-id="47f1f-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="47f1f-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47f1f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f1f-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="47f1f-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="47f1f-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="47f1f-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




