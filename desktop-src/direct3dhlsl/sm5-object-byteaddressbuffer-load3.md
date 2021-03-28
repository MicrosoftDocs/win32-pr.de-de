---
title: 'Byteaddressbuffer:: Load3 (uint)-Funktion'
description: 'Ruft drei Werte ab. | Byteaddressbuffer:: Load3 (uint)-Funktion'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981929"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="66120-105">Byteaddressbuffer:: Load3 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="66120-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="66120-106">Ruft drei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="66120-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="66120-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66120-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="66120-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66120-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66120-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66120-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66120-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="66120-110">Type: **uint**</span></span>

<span data-ttu-id="66120-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="66120-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66120-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66120-112">Return value</span></span>

<span data-ttu-id="66120-113">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="66120-113">Type: **uint3**</span></span>

<span data-ttu-id="66120-114">Drei Werte.</span><span class="sxs-lookup"><span data-stu-id="66120-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="66120-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66120-115">Remarks</span></span>

<span data-ttu-id="66120-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="66120-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="66120-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="66120-117">Vertex</span></span> | <span data-ttu-id="66120-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="66120-118">Hull</span></span> | <span data-ttu-id="66120-119">Domain</span><span class="sxs-lookup"><span data-stu-id="66120-119">Domain</span></span> | <span data-ttu-id="66120-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="66120-120">Geometry</span></span> | <span data-ttu-id="66120-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="66120-121">Pixel</span></span> | <span data-ttu-id="66120-122">Compute</span><span class="sxs-lookup"><span data-stu-id="66120-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="66120-123">x</span><span class="sxs-lookup"><span data-stu-id="66120-123">x</span></span>      | <span data-ttu-id="66120-124">x</span><span class="sxs-lookup"><span data-stu-id="66120-124">x</span></span>    | <span data-ttu-id="66120-125">x</span><span class="sxs-lookup"><span data-stu-id="66120-125">x</span></span>      | <span data-ttu-id="66120-126">x</span><span class="sxs-lookup"><span data-stu-id="66120-126">x</span></span>        | <span data-ttu-id="66120-127">x</span><span class="sxs-lookup"><span data-stu-id="66120-127">x</span></span>     | <span data-ttu-id="66120-128">x</span><span class="sxs-lookup"><span data-stu-id="66120-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="66120-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="66120-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66120-130">Load3-Methoden</span><span class="sxs-lookup"><span data-stu-id="66120-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="66120-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="66120-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




