---
title: 'Rwbyteaddressbuffer:: Load4 (uint)-Funktion'
description: 'Ruft vier Werte ab. | Rwbyteaddressbuffer:: Load4 (uint)-Funktion'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982048"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="aa3bc-105">Rwbyteaddressbuffer:: Load4 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa3bc-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="aa3bc-106">Ruft vier Werte ab.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa3bc-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="aa3bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa3bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa3bc-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="aa3bc-110">Type: **uint**</span></span>

<span data-ttu-id="aa3bc-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa3bc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa3bc-112">Return value</span></span>

<span data-ttu-id="aa3bc-113">Typ: **uint4**</span><span class="sxs-lookup"><span data-stu-id="aa3bc-113">Type: **uint4**</span></span>

<span data-ttu-id="aa3bc-114">Vier Werte.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa3bc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa3bc-115">Remarks</span></span>

<span data-ttu-id="aa3bc-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="aa3bc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aa3bc-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="aa3bc-117">Vertex</span></span> | <span data-ttu-id="aa3bc-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="aa3bc-118">Hull</span></span> | <span data-ttu-id="aa3bc-119">Domain</span><span class="sxs-lookup"><span data-stu-id="aa3bc-119">Domain</span></span> | <span data-ttu-id="aa3bc-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="aa3bc-120">Geometry</span></span> | <span data-ttu-id="aa3bc-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="aa3bc-121">Pixel</span></span> | <span data-ttu-id="aa3bc-122">Compute</span><span class="sxs-lookup"><span data-stu-id="aa3bc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aa3bc-123">x</span><span class="sxs-lookup"><span data-stu-id="aa3bc-123">x</span></span>     | <span data-ttu-id="aa3bc-124">x</span><span class="sxs-lookup"><span data-stu-id="aa3bc-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aa3bc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa3bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3bc-126">Load4-Methoden</span><span class="sxs-lookup"><span data-stu-id="aa3bc-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="aa3bc-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="aa3bc-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




