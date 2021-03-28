---
title: 'Texture2DMS:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2DMS:: GetDimensions-Funktion'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961383"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="f0ce2-105">Texture2DMS:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0ce2-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="f0ce2-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ce2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ce2-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="f0ce2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0ce2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ce2-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0ce2-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ce2-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f0ce2-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f0ce2-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="f0ce2-112">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0ce2-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ce2-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f0ce2-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f0ce2-114">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="f0ce2-115">*Anzahl von Beispielen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0ce2-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ce2-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f0ce2-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f0ce2-117">Die Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ce2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0ce2-118">Return value</span></span>

<span data-ttu-id="f0ce2-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ce2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0ce2-120">Remarks</span></span>

<span data-ttu-id="f0ce2-121">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="f0ce2-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="f0ce2-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f0ce2-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f0ce2-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f0ce2-123">Vertex</span></span> | <span data-ttu-id="f0ce2-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="f0ce2-124">Hull</span></span> | <span data-ttu-id="f0ce2-125">Domain</span><span class="sxs-lookup"><span data-stu-id="f0ce2-125">Domain</span></span> | <span data-ttu-id="f0ce2-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f0ce2-126">Geometry</span></span> | <span data-ttu-id="f0ce2-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="f0ce2-127">Pixel</span></span> | <span data-ttu-id="f0ce2-128">Compute</span><span class="sxs-lookup"><span data-stu-id="f0ce2-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f0ce2-129">x</span><span class="sxs-lookup"><span data-stu-id="f0ce2-129">x</span></span>     | <span data-ttu-id="f0ce2-130">x</span><span class="sxs-lookup"><span data-stu-id="f0ce2-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f0ce2-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0ce2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ce2-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="f0ce2-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="f0ce2-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f0ce2-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
