---
title: 'Texture2DArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2DArray:: GetDimensions-Funktion'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981072"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="7ca84-105">Texture2DArray:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ca84-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="7ca84-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="7ca84-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ca84-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="7ca84-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ca84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca84-109">*Miplevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca84-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ca84-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ca84-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="7ca84-111">Optional.</span></span> <span data-ttu-id="7ca84-112">Die MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="7ca84-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="7ca84-113">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca84-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ca84-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ca84-115">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="7ca84-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7ca84-116">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca84-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ca84-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ca84-118">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="7ca84-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7ca84-119">*Elemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca84-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ca84-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ca84-121">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="7ca84-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="7ca84-122">*Nummerige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca84-123">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ca84-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ca84-124">Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).</span><span class="sxs-lookup"><span data-stu-id="7ca84-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca84-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ca84-125">Return value</span></span>

<span data-ttu-id="7ca84-126">Nichts</span><span class="sxs-lookup"><span data-stu-id="7ca84-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca84-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ca84-127">Remarks</span></span>

<span data-ttu-id="7ca84-128">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="7ca84-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="7ca84-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7ca84-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7ca84-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7ca84-130">Vertex</span></span> | <span data-ttu-id="7ca84-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="7ca84-131">Hull</span></span> | <span data-ttu-id="7ca84-132">Domain</span><span class="sxs-lookup"><span data-stu-id="7ca84-132">Domain</span></span> | <span data-ttu-id="7ca84-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7ca84-133">Geometry</span></span> | <span data-ttu-id="7ca84-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="7ca84-134">Pixel</span></span> | <span data-ttu-id="7ca84-135">Compute</span><span class="sxs-lookup"><span data-stu-id="7ca84-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7ca84-136">x</span><span class="sxs-lookup"><span data-stu-id="7ca84-136">x</span></span>     | <span data-ttu-id="7ca84-137">x</span><span class="sxs-lookup"><span data-stu-id="7ca84-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7ca84-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ca84-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca84-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7ca84-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="7ca84-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7ca84-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
