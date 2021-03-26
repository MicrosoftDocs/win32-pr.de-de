---
title: 'RWTexture2DArray:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | RWTexture2DArray:: Operator-Funktion'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050749"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="c938e-105">RWTexture2DArray:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="c938e-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="c938e-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="c938e-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c938e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c938e-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="c938e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c938e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c938e-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c938e-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c938e-110">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="c938e-110">Type: **uint3**</span></span>

<span data-ttu-id="c938e-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="c938e-111">The index position.</span></span> <span data-ttu-id="c938e-112">Die erste und die zweite Komponente enthalten die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="c938e-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="c938e-113">Die dritte Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="c938e-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c938e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c938e-114">Return value</span></span>

<span data-ttu-id="c938e-115">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="c938e-115">Type: **R**</span></span>

<span data-ttu-id="c938e-116">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="c938e-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="c938e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c938e-117">Remarks</span></span>

<span data-ttu-id="c938e-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c938e-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c938e-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c938e-119">Vertex</span></span> | <span data-ttu-id="c938e-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="c938e-120">Hull</span></span> | <span data-ttu-id="c938e-121">Domain</span><span class="sxs-lookup"><span data-stu-id="c938e-121">Domain</span></span> | <span data-ttu-id="c938e-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c938e-122">Geometry</span></span> | <span data-ttu-id="c938e-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="c938e-123">Pixel</span></span> | <span data-ttu-id="c938e-124">Compute</span><span class="sxs-lookup"><span data-stu-id="c938e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c938e-125">x</span><span class="sxs-lookup"><span data-stu-id="c938e-125">x</span></span>     | <span data-ttu-id="c938e-126">x</span><span class="sxs-lookup"><span data-stu-id="c938e-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c938e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c938e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c938e-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="c938e-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="c938e-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c938e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




