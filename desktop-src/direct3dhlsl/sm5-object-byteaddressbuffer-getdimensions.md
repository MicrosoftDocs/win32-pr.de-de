---
title: 'Byteaddressbuffer:: GetDimensions-Funktion'
description: 'Ruft die Länge des Puffers ab. | Byteaddressbuffer:: GetDimensions-Funktion'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995294"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="ab320-105">Byteaddressbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="ab320-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="ab320-106">Ruft die Länge des Puffers ab.</span><span class="sxs-lookup"><span data-stu-id="ab320-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab320-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab320-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="ab320-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab320-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab320-109"> \[ Abblenden\]</span><span class="sxs-lookup"><span data-stu-id="ab320-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab320-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ab320-110">Type: **uint**</span></span>

<span data-ttu-id="ab320-111">Die Länge des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ab320-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab320-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab320-112">Return value</span></span>

<span data-ttu-id="ab320-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ab320-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab320-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab320-114">Remarks</span></span>

<span data-ttu-id="ab320-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ab320-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ab320-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ab320-116">Vertex</span></span> | <span data-ttu-id="ab320-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="ab320-117">Hull</span></span> | <span data-ttu-id="ab320-118">Domain</span><span class="sxs-lookup"><span data-stu-id="ab320-118">Domain</span></span> | <span data-ttu-id="ab320-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ab320-119">Geometry</span></span> | <span data-ttu-id="ab320-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="ab320-120">Pixel</span></span> | <span data-ttu-id="ab320-121">Compute</span><span class="sxs-lookup"><span data-stu-id="ab320-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ab320-122">x</span><span class="sxs-lookup"><span data-stu-id="ab320-122">x</span></span>      | <span data-ttu-id="ab320-123">x</span><span class="sxs-lookup"><span data-stu-id="ab320-123">x</span></span>    | <span data-ttu-id="ab320-124">x</span><span class="sxs-lookup"><span data-stu-id="ab320-124">x</span></span>      | <span data-ttu-id="ab320-125">x</span><span class="sxs-lookup"><span data-stu-id="ab320-125">x</span></span>        | <span data-ttu-id="ab320-126">x</span><span class="sxs-lookup"><span data-stu-id="ab320-126">x</span></span>     | <span data-ttu-id="ab320-127">x</span><span class="sxs-lookup"><span data-stu-id="ab320-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab320-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab320-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab320-129">Byteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="ab320-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ab320-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="ab320-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




