---
title: 'Byteaddressbuffer:: Load2 (uint)-Funktion'
description: 'Ruft zwei Werte ab. | Byteaddressbuffer:: Load2 (uint)-Funktion'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
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
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761616"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="0a8bf-105">Byteaddressbuffer:: Load2 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a8bf-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="0a8bf-106">Ruft zwei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a8bf-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="0a8bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a8bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a8bf-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a8bf-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8bf-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="0a8bf-110">Type: **uint**</span></span>

<span data-ttu-id="0a8bf-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a8bf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a8bf-112">Return value</span></span>

<span data-ttu-id="0a8bf-113">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="0a8bf-113">Type: **uint2**</span></span>

<span data-ttu-id="0a8bf-114">Zwei-Werte.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8bf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a8bf-115">Remarks</span></span>

<span data-ttu-id="0a8bf-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0a8bf-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="0a8bf-117">Vertex</span></span> | <span data-ttu-id="0a8bf-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="0a8bf-118">Hull</span></span> | <span data-ttu-id="0a8bf-119">Domain</span><span class="sxs-lookup"><span data-stu-id="0a8bf-119">Domain</span></span> | <span data-ttu-id="0a8bf-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="0a8bf-120">Geometry</span></span> | <span data-ttu-id="0a8bf-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="0a8bf-121">Pixel</span></span> | <span data-ttu-id="0a8bf-122">Compute</span><span class="sxs-lookup"><span data-stu-id="0a8bf-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0a8bf-123">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-123">x</span></span>      | <span data-ttu-id="0a8bf-124">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-124">x</span></span>    | <span data-ttu-id="0a8bf-125">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-125">x</span></span>      | <span data-ttu-id="0a8bf-126">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-126">x</span></span>        | <span data-ttu-id="0a8bf-127">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-127">x</span></span>     | <span data-ttu-id="0a8bf-128">x</span><span class="sxs-lookup"><span data-stu-id="0a8bf-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0a8bf-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a8bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8bf-130">Load2-Methoden</span><span class="sxs-lookup"><span data-stu-id="0a8bf-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="0a8bf-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0a8bf-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




