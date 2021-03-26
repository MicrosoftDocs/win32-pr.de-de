---
title: 'Rwstructuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Rwstructuredbuffer:: GetDimensions-Funktion'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981081"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="de8b7-105">Rwstructuredbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="de8b7-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="de8b7-106">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="de8b7-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de8b7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="de8b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de8b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8b7-109">*numstructs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de8b7-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de8b7-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="de8b7-110">Type: **uint**</span></span>

<span data-ttu-id="de8b7-111">Die Anzahl der Strukturen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="de8b7-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="de8b7-112">*Stride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de8b7-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de8b7-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="de8b7-113">Type: **uint**</span></span>

<span data-ttu-id="de8b7-114">Der Schritt (in Byte) der einzelnen Strukturelemente.</span><span class="sxs-lookup"><span data-stu-id="de8b7-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8b7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de8b7-115">Return value</span></span>

<span data-ttu-id="de8b7-116">Nichts</span><span class="sxs-lookup"><span data-stu-id="de8b7-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="de8b7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de8b7-117">Remarks</span></span>

<span data-ttu-id="de8b7-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="de8b7-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="de8b7-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="de8b7-119">Vertex</span></span> | <span data-ttu-id="de8b7-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="de8b7-120">Hull</span></span> | <span data-ttu-id="de8b7-121">Domain</span><span class="sxs-lookup"><span data-stu-id="de8b7-121">Domain</span></span> | <span data-ttu-id="de8b7-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="de8b7-122">Geometry</span></span> | <span data-ttu-id="de8b7-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="de8b7-123">Pixel</span></span> | <span data-ttu-id="de8b7-124">Compute</span><span class="sxs-lookup"><span data-stu-id="de8b7-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="de8b7-125">x</span><span class="sxs-lookup"><span data-stu-id="de8b7-125">x</span></span>     | <span data-ttu-id="de8b7-126">x</span><span class="sxs-lookup"><span data-stu-id="de8b7-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="de8b7-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de8b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8b7-128">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="de8b7-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="de8b7-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="de8b7-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




