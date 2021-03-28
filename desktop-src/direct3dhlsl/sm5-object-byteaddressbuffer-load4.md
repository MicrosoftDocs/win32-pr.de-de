---
title: 'Byteaddressbuffer:: Load4 (uint)-Funktion'
description: 'Ruft vier Werte ab. | Byteaddressbuffer:: Load4 (uint)-Funktion'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981928"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="eec2e-105">Byteaddressbuffer:: Load4 (uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="eec2e-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="eec2e-106">Ruft vier Werte ab.</span><span class="sxs-lookup"><span data-stu-id="eec2e-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eec2e-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="eec2e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec2e-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eec2e-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2e-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="eec2e-110">Type: **uint**</span></span>

<span data-ttu-id="eec2e-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="eec2e-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec2e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eec2e-112">Return value</span></span>

<span data-ttu-id="eec2e-113">Typ: **uint4**</span><span class="sxs-lookup"><span data-stu-id="eec2e-113">Type: **uint4**</span></span>

<span data-ttu-id="eec2e-114">Vier Werte.</span><span class="sxs-lookup"><span data-stu-id="eec2e-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec2e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eec2e-115">Remarks</span></span>

<span data-ttu-id="eec2e-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eec2e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eec2e-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="eec2e-117">Vertex</span></span> | <span data-ttu-id="eec2e-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="eec2e-118">Hull</span></span> | <span data-ttu-id="eec2e-119">Domain</span><span class="sxs-lookup"><span data-stu-id="eec2e-119">Domain</span></span> | <span data-ttu-id="eec2e-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="eec2e-120">Geometry</span></span> | <span data-ttu-id="eec2e-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="eec2e-121">Pixel</span></span> | <span data-ttu-id="eec2e-122">Compute</span><span class="sxs-lookup"><span data-stu-id="eec2e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eec2e-123">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-123">x</span></span>      | <span data-ttu-id="eec2e-124">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-124">x</span></span>    | <span data-ttu-id="eec2e-125">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-125">x</span></span>      | <span data-ttu-id="eec2e-126">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-126">x</span></span>        | <span data-ttu-id="eec2e-127">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-127">x</span></span>     | <span data-ttu-id="eec2e-128">x</span><span class="sxs-lookup"><span data-stu-id="eec2e-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eec2e-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eec2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec2e-130">Load4-Methoden</span><span class="sxs-lookup"><span data-stu-id="eec2e-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="eec2e-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eec2e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




