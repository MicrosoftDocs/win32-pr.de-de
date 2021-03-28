---
title: 'RWTexture1D:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | RWTexture1D:: Operator-Funktion'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530614"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="e6c5f-105">RWTexture1D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="e6c5f-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="e6c5f-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="e6c5f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c5f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6c5f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="e6c5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6c5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c5f-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6c5f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c5f-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e6c5f-110">Type: **uint**</span></span>

<span data-ttu-id="e6c5f-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="e6c5f-111">The index position.</span></span> <span data-ttu-id="e6c5f-112">Enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="e6c5f-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c5f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6c5f-113">Return value</span></span>

<span data-ttu-id="e6c5f-114">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="e6c5f-114">Type: **R**</span></span>

<span data-ttu-id="e6c5f-115">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="e6c5f-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c5f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6c5f-116">Remarks</span></span>

<span data-ttu-id="e6c5f-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e6c5f-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e6c5f-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e6c5f-118">Vertex</span></span> | <span data-ttu-id="e6c5f-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="e6c5f-119">Hull</span></span> | <span data-ttu-id="e6c5f-120">Domain</span><span class="sxs-lookup"><span data-stu-id="e6c5f-120">Domain</span></span> | <span data-ttu-id="e6c5f-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e6c5f-121">Geometry</span></span> | <span data-ttu-id="e6c5f-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="e6c5f-122">Pixel</span></span> | <span data-ttu-id="e6c5f-123">Compute</span><span class="sxs-lookup"><span data-stu-id="e6c5f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e6c5f-124">x</span><span class="sxs-lookup"><span data-stu-id="e6c5f-124">x</span></span>     | <span data-ttu-id="e6c5f-125">x</span><span class="sxs-lookup"><span data-stu-id="e6c5f-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e6c5f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e6c5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c5f-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="e6c5f-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="e6c5f-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e6c5f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




