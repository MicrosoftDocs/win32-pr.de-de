---
title: 'Structuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Structuredbuffer:: GetDimensions-Funktion'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352959"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="80eef-105">Structuredbuffer:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="80eef-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="80eef-106">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="80eef-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="80eef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80eef-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="80eef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="80eef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80eef-109">*numstructs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80eef-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80eef-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="80eef-110">Type: **uint**</span></span>

<span data-ttu-id="80eef-111">Die Anzahl der Strukturen in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="80eef-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="80eef-112">*Stride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80eef-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80eef-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="80eef-113">Type: **uint**</span></span>

<span data-ttu-id="80eef-114">Der Schritt (in Byte) der einzelnen Strukturelemente.</span><span class="sxs-lookup"><span data-stu-id="80eef-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80eef-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80eef-115">Return value</span></span>

<span data-ttu-id="80eef-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="80eef-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80eef-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80eef-117">Remarks</span></span>

<span data-ttu-id="80eef-118">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="80eef-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="80eef-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="80eef-119">Vertex</span></span> | <span data-ttu-id="80eef-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="80eef-120">Hull</span></span> | <span data-ttu-id="80eef-121">Domain</span><span class="sxs-lookup"><span data-stu-id="80eef-121">Domain</span></span> | <span data-ttu-id="80eef-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="80eef-122">Geometry</span></span> | <span data-ttu-id="80eef-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="80eef-123">Pixel</span></span> | <span data-ttu-id="80eef-124">Compute</span><span class="sxs-lookup"><span data-stu-id="80eef-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="80eef-125">x</span><span class="sxs-lookup"><span data-stu-id="80eef-125">x</span></span>      | <span data-ttu-id="80eef-126">x</span><span class="sxs-lookup"><span data-stu-id="80eef-126">x</span></span>    | <span data-ttu-id="80eef-127">x</span><span class="sxs-lookup"><span data-stu-id="80eef-127">x</span></span>      | <span data-ttu-id="80eef-128">x</span><span class="sxs-lookup"><span data-stu-id="80eef-128">x</span></span>        | <span data-ttu-id="80eef-129">x</span><span class="sxs-lookup"><span data-stu-id="80eef-129">x</span></span>     | <span data-ttu-id="80eef-130">x</span><span class="sxs-lookup"><span data-stu-id="80eef-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="80eef-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="80eef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80eef-132">Structuredbuffer</span><span class="sxs-lookup"><span data-stu-id="80eef-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="80eef-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="80eef-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




