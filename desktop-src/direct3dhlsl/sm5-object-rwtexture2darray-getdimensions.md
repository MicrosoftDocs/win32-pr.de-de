---
title: 'RWTexture2DArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | RWTexture2DArray:: GetDimensions-Funktion'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
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
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219118"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="60bd7-105">RWTexture2DArray:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="60bd7-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="60bd7-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="60bd7-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bd7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60bd7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="60bd7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60bd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bd7-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="60bd7-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60bd7-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="60bd7-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="60bd7-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="60bd7-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="60bd7-112">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="60bd7-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60bd7-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="60bd7-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="60bd7-114">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="60bd7-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="60bd7-115">*Elemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="60bd7-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60bd7-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="60bd7-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="60bd7-117">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="60bd7-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bd7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60bd7-118">Return value</span></span>

<span data-ttu-id="60bd7-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="60bd7-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60bd7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60bd7-120">Remarks</span></span>

<span data-ttu-id="60bd7-121">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="60bd7-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="60bd7-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="60bd7-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="60bd7-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="60bd7-123">Vertex</span></span> | <span data-ttu-id="60bd7-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="60bd7-124">Hull</span></span> | <span data-ttu-id="60bd7-125">Domain</span><span class="sxs-lookup"><span data-stu-id="60bd7-125">Domain</span></span> | <span data-ttu-id="60bd7-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="60bd7-126">Geometry</span></span> | <span data-ttu-id="60bd7-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="60bd7-127">Pixel</span></span> | <span data-ttu-id="60bd7-128">Compute</span><span class="sxs-lookup"><span data-stu-id="60bd7-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="60bd7-129">x</span><span class="sxs-lookup"><span data-stu-id="60bd7-129">x</span></span>     | <span data-ttu-id="60bd7-130">x</span><span class="sxs-lookup"><span data-stu-id="60bd7-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="60bd7-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60bd7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60bd7-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="60bd7-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="60bd7-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="60bd7-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
