---
title: 'Rwbuffer:: GetDimensions-Funktion'
description: 'Ruft die Länge des Puffers ab. | Rwbuffer:: GetDimensions-Funktion'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995686"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="35b29-105">Rwbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="35b29-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="35b29-106">Ruft die Länge des Puffers ab.</span><span class="sxs-lookup"><span data-stu-id="35b29-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b29-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="35b29-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35b29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b29-109"> \[ Abblenden\]</span><span class="sxs-lookup"><span data-stu-id="35b29-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35b29-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="35b29-110">Type: **uint**</span></span>

<span data-ttu-id="35b29-111">Die Länge des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="35b29-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b29-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35b29-112">Return value</span></span>

<span data-ttu-id="35b29-113">Nichts</span><span class="sxs-lookup"><span data-stu-id="35b29-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="35b29-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35b29-114">Remarks</span></span>

<span data-ttu-id="35b29-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="35b29-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="35b29-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="35b29-116">Vertex</span></span> | <span data-ttu-id="35b29-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="35b29-117">Hull</span></span> | <span data-ttu-id="35b29-118">Domain</span><span class="sxs-lookup"><span data-stu-id="35b29-118">Domain</span></span> | <span data-ttu-id="35b29-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="35b29-119">Geometry</span></span> | <span data-ttu-id="35b29-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="35b29-120">Pixel</span></span> | <span data-ttu-id="35b29-121">Compute</span><span class="sxs-lookup"><span data-stu-id="35b29-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="35b29-122">x</span><span class="sxs-lookup"><span data-stu-id="35b29-122">x</span></span>     | <span data-ttu-id="35b29-123">x</span><span class="sxs-lookup"><span data-stu-id="35b29-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="35b29-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35b29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b29-125">Rwbuffer</span><span class="sxs-lookup"><span data-stu-id="35b29-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="35b29-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="35b29-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




