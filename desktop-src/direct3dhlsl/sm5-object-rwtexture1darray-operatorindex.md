---
title: 'RWTexture1DArray:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | RWTexture1DArray:: Operator-Funktion'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981712"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="78738-105">RWTexture1DArray:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="78738-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="78738-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="78738-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="78738-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78738-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="78738-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78738-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78738-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78738-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78738-110">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="78738-110">Type: **uint2**</span></span>

<span data-ttu-id="78738-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="78738-111">The index position.</span></span> <span data-ttu-id="78738-112">Die erste Komponente enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="78738-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="78738-113">Die zweite Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="78738-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78738-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78738-114">Return value</span></span>

<span data-ttu-id="78738-115">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="78738-115">Type: **R**</span></span>

<span data-ttu-id="78738-116">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="78738-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="78738-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78738-117">Remarks</span></span>

<span data-ttu-id="78738-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="78738-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="78738-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="78738-119">Vertex</span></span> | <span data-ttu-id="78738-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="78738-120">Hull</span></span> | <span data-ttu-id="78738-121">Domain</span><span class="sxs-lookup"><span data-stu-id="78738-121">Domain</span></span> | <span data-ttu-id="78738-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="78738-122">Geometry</span></span> | <span data-ttu-id="78738-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="78738-123">Pixel</span></span> | <span data-ttu-id="78738-124">Compute</span><span class="sxs-lookup"><span data-stu-id="78738-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="78738-125">x</span><span class="sxs-lookup"><span data-stu-id="78738-125">x</span></span>     | <span data-ttu-id="78738-126">x</span><span class="sxs-lookup"><span data-stu-id="78738-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="78738-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="78738-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78738-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="78738-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="78738-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="78738-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




