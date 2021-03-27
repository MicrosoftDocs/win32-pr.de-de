---
title: 'Rwbyteaddressbuffer:: Load3 (uint)-Funktion'
description: 'Ruft drei Werte ab. | Rwbyteaddressbuffer:: Load3 (uint)-Funktion'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
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
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982059"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="d7699-105">Rwbyteaddressbuffer:: Load3 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7699-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="d7699-106">Ruft drei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="d7699-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7699-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7699-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="d7699-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7699-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7699-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7699-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7699-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d7699-110">Type: **uint**</span></span>

<span data-ttu-id="d7699-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="d7699-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7699-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7699-112">Return value</span></span>

<span data-ttu-id="d7699-113">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="d7699-113">Type: **uint3**</span></span>

<span data-ttu-id="d7699-114">Drei Werte.</span><span class="sxs-lookup"><span data-stu-id="d7699-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7699-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7699-115">Remarks</span></span>

<span data-ttu-id="d7699-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d7699-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d7699-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d7699-117">Vertex</span></span> | <span data-ttu-id="d7699-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="d7699-118">Hull</span></span> | <span data-ttu-id="d7699-119">Domain</span><span class="sxs-lookup"><span data-stu-id="d7699-119">Domain</span></span> | <span data-ttu-id="d7699-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d7699-120">Geometry</span></span> | <span data-ttu-id="d7699-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="d7699-121">Pixel</span></span> | <span data-ttu-id="d7699-122">Compute</span><span class="sxs-lookup"><span data-stu-id="d7699-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d7699-123">x</span><span class="sxs-lookup"><span data-stu-id="d7699-123">x</span></span>     | <span data-ttu-id="d7699-124">x</span><span class="sxs-lookup"><span data-stu-id="d7699-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d7699-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7699-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7699-126">Load3-Methoden</span><span class="sxs-lookup"><span data-stu-id="d7699-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="d7699-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d7699-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




