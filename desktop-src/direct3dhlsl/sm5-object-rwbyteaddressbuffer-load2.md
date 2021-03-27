---
title: 'Rwbyteaddressbuffer:: Load2 (uint)-Funktion'
description: 'Ruft zwei Werte ab. | Rwbyteaddressbuffer:: Load2 (uint)-Funktion'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982029"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="5dd9b-105">Rwbyteaddressbuffer:: Load2 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="5dd9b-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="5dd9b-106">Ruft zwei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="5dd9b-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd9b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dd9b-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="5dd9b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dd9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd9b-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dd9b-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd9b-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5dd9b-110">Type: **uint**</span></span>

<span data-ttu-id="5dd9b-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="5dd9b-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd9b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dd9b-112">Return value</span></span>

<span data-ttu-id="5dd9b-113">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="5dd9b-113">Type: **uint2**</span></span>

<span data-ttu-id="5dd9b-114">Zwei-Werte.</span><span class="sxs-lookup"><span data-stu-id="5dd9b-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd9b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dd9b-115">Remarks</span></span>

<span data-ttu-id="5dd9b-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5dd9b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5dd9b-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5dd9b-117">Vertex</span></span> | <span data-ttu-id="5dd9b-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="5dd9b-118">Hull</span></span> | <span data-ttu-id="5dd9b-119">Domain</span><span class="sxs-lookup"><span data-stu-id="5dd9b-119">Domain</span></span> | <span data-ttu-id="5dd9b-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5dd9b-120">Geometry</span></span> | <span data-ttu-id="5dd9b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="5dd9b-121">Pixel</span></span> | <span data-ttu-id="5dd9b-122">Compute</span><span class="sxs-lookup"><span data-stu-id="5dd9b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5dd9b-123">x</span><span class="sxs-lookup"><span data-stu-id="5dd9b-123">x</span></span>     | <span data-ttu-id="5dd9b-124">x</span><span class="sxs-lookup"><span data-stu-id="5dd9b-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5dd9b-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5dd9b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd9b-126">Load2-Methoden</span><span class="sxs-lookup"><span data-stu-id="5dd9b-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="5dd9b-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5dd9b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




