---
title: 'Texture2DMSArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2DMSArray:: GetDimensions-Funktion'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353719"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="2e323-105">Texture2DMSArray:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e323-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="2e323-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="2e323-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e323-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e323-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="2e323-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e323-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e323-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e323-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e323-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e323-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2e323-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="2e323-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2e323-112">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e323-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e323-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e323-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2e323-114">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="2e323-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2e323-115">*Elemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e323-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e323-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e323-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2e323-117">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="2e323-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="2e323-118">*Anzahl von Beispielen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e323-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e323-119">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e323-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2e323-120">Die Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="2e323-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e323-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e323-121">Return value</span></span>

<span data-ttu-id="2e323-122">Nichts</span><span class="sxs-lookup"><span data-stu-id="2e323-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="2e323-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e323-123">Remarks</span></span>

<span data-ttu-id="2e323-124">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="2e323-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="2e323-125">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2e323-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2e323-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2e323-126">Vertex</span></span> | <span data-ttu-id="2e323-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="2e323-127">Hull</span></span> | <span data-ttu-id="2e323-128">Domain</span><span class="sxs-lookup"><span data-stu-id="2e323-128">Domain</span></span> | <span data-ttu-id="2e323-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2e323-129">Geometry</span></span> | <span data-ttu-id="2e323-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="2e323-130">Pixel</span></span> | <span data-ttu-id="2e323-131">Compute</span><span class="sxs-lookup"><span data-stu-id="2e323-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2e323-132">x</span><span class="sxs-lookup"><span data-stu-id="2e323-132">x</span></span>     | <span data-ttu-id="2e323-133">x</span><span class="sxs-lookup"><span data-stu-id="2e323-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2e323-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e323-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e323-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2e323-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="2e323-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2e323-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
