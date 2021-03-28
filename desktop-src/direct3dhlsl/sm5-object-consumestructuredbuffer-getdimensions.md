---
title: 'Consumestructuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Consumestructuredbuffer:: GetDimensions-Funktion'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995318"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="1f47c-105">Consumestructuredbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f47c-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="1f47c-106">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="1f47c-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f47c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f47c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="1f47c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f47c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f47c-109">*numstructs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f47c-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f47c-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f47c-110">Type: **uint**</span></span>

<span data-ttu-id="1f47c-111">Die Anzahl der Strukturen.</span><span class="sxs-lookup"><span data-stu-id="1f47c-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="1f47c-112">*Stride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f47c-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f47c-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f47c-113">Type: **uint**</span></span>

<span data-ttu-id="1f47c-114">Der Schritt (in Byte) der einzelnen Elemente.</span><span class="sxs-lookup"><span data-stu-id="1f47c-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f47c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f47c-115">Return value</span></span>

<span data-ttu-id="1f47c-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1f47c-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f47c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f47c-117">Remarks</span></span>

<span data-ttu-id="1f47c-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1f47c-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1f47c-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1f47c-119">Vertex</span></span> | <span data-ttu-id="1f47c-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="1f47c-120">Hull</span></span> | <span data-ttu-id="1f47c-121">Domain</span><span class="sxs-lookup"><span data-stu-id="1f47c-121">Domain</span></span> | <span data-ttu-id="1f47c-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1f47c-122">Geometry</span></span> | <span data-ttu-id="1f47c-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="1f47c-123">Pixel</span></span> | <span data-ttu-id="1f47c-124">Compute</span><span class="sxs-lookup"><span data-stu-id="1f47c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1f47c-125">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-125">x</span></span>      | <span data-ttu-id="1f47c-126">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-126">x</span></span>    | <span data-ttu-id="1f47c-127">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-127">x</span></span>      | <span data-ttu-id="1f47c-128">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-128">x</span></span>        | <span data-ttu-id="1f47c-129">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-129">x</span></span>     | <span data-ttu-id="1f47c-130">x</span><span class="sxs-lookup"><span data-stu-id="1f47c-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1f47c-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f47c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f47c-132">Consumestructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="1f47c-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1f47c-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1f47c-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




