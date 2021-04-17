---
title: 'Rwbyteaddressbuffer:: GetDimensions-Funktion'
description: 'Ruft die Länge des Puffers ab. | Rwbyteaddressbuffer:: GetDimensions-Funktion'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353579"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="c72cf-105">Rwbyteaddressbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="c72cf-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="c72cf-106">Ruft die Länge des Puffers ab.</span><span class="sxs-lookup"><span data-stu-id="c72cf-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c72cf-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="c72cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c72cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72cf-109"> \[ Abblenden\]</span><span class="sxs-lookup"><span data-stu-id="c72cf-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c72cf-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c72cf-110">Type: **uint**</span></span>

<span data-ttu-id="c72cf-111">Die Länge des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c72cf-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72cf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c72cf-112">Return value</span></span>

<span data-ttu-id="c72cf-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c72cf-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72cf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c72cf-114">Remarks</span></span>

<span data-ttu-id="c72cf-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c72cf-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c72cf-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c72cf-116">Vertex</span></span> | <span data-ttu-id="c72cf-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="c72cf-117">Hull</span></span> | <span data-ttu-id="c72cf-118">Domain</span><span class="sxs-lookup"><span data-stu-id="c72cf-118">Domain</span></span> | <span data-ttu-id="c72cf-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c72cf-119">Geometry</span></span> | <span data-ttu-id="c72cf-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="c72cf-120">Pixel</span></span> | <span data-ttu-id="c72cf-121">Compute</span><span class="sxs-lookup"><span data-stu-id="c72cf-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c72cf-122">x</span><span class="sxs-lookup"><span data-stu-id="c72cf-122">x</span></span>     | <span data-ttu-id="c72cf-123">x</span><span class="sxs-lookup"><span data-stu-id="c72cf-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c72cf-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c72cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72cf-125">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="c72cf-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c72cf-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c72cf-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




