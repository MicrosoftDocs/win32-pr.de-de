---
title: 'Appendstructuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Appendstructuredbuffer:: GetDimensions-Funktion'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions-Funktion HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981096"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="a746b-105">Appendstructuredbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="a746b-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="a746b-106">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="a746b-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a746b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a746b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="a746b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a746b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a746b-109">*numstructs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a746b-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a746b-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a746b-110">Type: **uint**</span></span>

<span data-ttu-id="a746b-111">Die Anzahl der Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a746b-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="a746b-112">*Stride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a746b-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a746b-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a746b-113">Type: **uint**</span></span>

<span data-ttu-id="a746b-114">Die Anzahl der Bytes in jedem Element.</span><span class="sxs-lookup"><span data-stu-id="a746b-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a746b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a746b-115">Return value</span></span>

<span data-ttu-id="a746b-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a746b-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a746b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a746b-117">Remarks</span></span>

<span data-ttu-id="a746b-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a746b-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a746b-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="a746b-119">Vertex</span></span> | <span data-ttu-id="a746b-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="a746b-120">Hull</span></span> | <span data-ttu-id="a746b-121">Domain</span><span class="sxs-lookup"><span data-stu-id="a746b-121">Domain</span></span> | <span data-ttu-id="a746b-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="a746b-122">Geometry</span></span> | <span data-ttu-id="a746b-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="a746b-123">Pixel</span></span> | <span data-ttu-id="a746b-124">Compute</span><span class="sxs-lookup"><span data-stu-id="a746b-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a746b-125">x</span><span class="sxs-lookup"><span data-stu-id="a746b-125">x</span></span>      | <span data-ttu-id="a746b-126">x</span><span class="sxs-lookup"><span data-stu-id="a746b-126">x</span></span>    | <span data-ttu-id="a746b-127">x</span><span class="sxs-lookup"><span data-stu-id="a746b-127">x</span></span>      | <span data-ttu-id="a746b-128">x</span><span class="sxs-lookup"><span data-stu-id="a746b-128">x</span></span>        | <span data-ttu-id="a746b-129">x</span><span class="sxs-lookup"><span data-stu-id="a746b-129">x</span></span>     | <span data-ttu-id="a746b-130">x</span><span class="sxs-lookup"><span data-stu-id="a746b-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a746b-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a746b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a746b-132">Appendstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="a746b-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="a746b-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="a746b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




