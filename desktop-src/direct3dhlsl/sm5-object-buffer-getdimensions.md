---
title: 'Buffer:: GetDimensions-Funktion'
description: 'Ruft die Länge des Puffers ab. | Buffer:: GetDimensions-Funktion'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981089"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="d8a3b-105">Buffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8a3b-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="d8a3b-106">Ruft die Länge des Puffers ab.</span><span class="sxs-lookup"><span data-stu-id="d8a3b-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8a3b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="d8a3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8a3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a3b-109"> \[ Abblenden\]</span><span class="sxs-lookup"><span data-stu-id="d8a3b-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a3b-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d8a3b-110">Type: **uint**</span></span>

<span data-ttu-id="d8a3b-111">Die Länge des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d8a3b-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a3b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8a3b-112">Return value</span></span>

<span data-ttu-id="d8a3b-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d8a3b-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a3b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8a3b-114">Remarks</span></span>

<span data-ttu-id="d8a3b-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d8a3b-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d8a3b-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d8a3b-116">Vertex</span></span> | <span data-ttu-id="d8a3b-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="d8a3b-117">Hull</span></span> | <span data-ttu-id="d8a3b-118">Domain</span><span class="sxs-lookup"><span data-stu-id="d8a3b-118">Domain</span></span> | <span data-ttu-id="d8a3b-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d8a3b-119">Geometry</span></span> | <span data-ttu-id="d8a3b-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="d8a3b-120">Pixel</span></span> | <span data-ttu-id="d8a3b-121">Compute</span><span class="sxs-lookup"><span data-stu-id="d8a3b-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d8a3b-122">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-122">x</span></span>      | <span data-ttu-id="d8a3b-123">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-123">x</span></span>    | <span data-ttu-id="d8a3b-124">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-124">x</span></span>      | <span data-ttu-id="d8a3b-125">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-125">x</span></span>        | <span data-ttu-id="d8a3b-126">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-126">x</span></span>     | <span data-ttu-id="d8a3b-127">x</span><span class="sxs-lookup"><span data-stu-id="d8a3b-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d8a3b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8a3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a3b-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="d8a3b-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="d8a3b-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d8a3b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




