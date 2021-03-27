---
title: 'Byteaddressbuffer:: Load (int)-Funktion'
description: 'Ruft einen Wert ab. | Byteaddressbuffer:: Load (int)-Funktion'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995383"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="e0b93-105">Byteaddressbuffer:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0b93-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="e0b93-106">Ruft einen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="e0b93-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b93-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b93-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="e0b93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b93-109">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0b93-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b93-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="e0b93-110">Type: **int**</span></span>

<span data-ttu-id="e0b93-111">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="e0b93-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b93-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0b93-112">Return value</span></span>

<span data-ttu-id="e0b93-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e0b93-113">Type: **uint**</span></span>

<span data-ttu-id="e0b93-114">Ein-Wert.</span><span class="sxs-lookup"><span data-stu-id="e0b93-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0b93-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0b93-115">Remarks</span></span>

<span data-ttu-id="e0b93-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e0b93-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e0b93-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e0b93-117">Vertex</span></span> | <span data-ttu-id="e0b93-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="e0b93-118">Hull</span></span> | <span data-ttu-id="e0b93-119">Domain</span><span class="sxs-lookup"><span data-stu-id="e0b93-119">Domain</span></span> | <span data-ttu-id="e0b93-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e0b93-120">Geometry</span></span> | <span data-ttu-id="e0b93-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="e0b93-121">Pixel</span></span> | <span data-ttu-id="e0b93-122">Compute</span><span class="sxs-lookup"><span data-stu-id="e0b93-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e0b93-123">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-123">x</span></span>      | <span data-ttu-id="e0b93-124">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-124">x</span></span>    | <span data-ttu-id="e0b93-125">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-125">x</span></span>      | <span data-ttu-id="e0b93-126">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-126">x</span></span>        | <span data-ttu-id="e0b93-127">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-127">x</span></span>     | <span data-ttu-id="e0b93-128">x</span><span class="sxs-lookup"><span data-stu-id="e0b93-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e0b93-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0b93-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b93-130">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="e0b93-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="e0b93-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e0b93-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




