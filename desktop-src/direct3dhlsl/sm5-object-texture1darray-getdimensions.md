---
title: 'Texture1DArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture1DArray:: GetDimensions-Funktion'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761763"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="cc786-105">Texture1DArray:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc786-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="cc786-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="cc786-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc786-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc786-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="cc786-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc786-109">*Miplevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc786-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc786-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc786-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc786-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="cc786-111">Optional.</span></span> <span data-ttu-id="cc786-112">MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="cc786-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="cc786-113">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cc786-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc786-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc786-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc786-115">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="cc786-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="cc786-116">*Elemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cc786-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc786-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc786-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc786-118">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="cc786-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="cc786-119">*Nummerige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cc786-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc786-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc786-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc786-121">Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).</span><span class="sxs-lookup"><span data-stu-id="cc786-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc786-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc786-122">Return value</span></span>

<span data-ttu-id="cc786-123">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cc786-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc786-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc786-124">Remarks</span></span>

<span data-ttu-id="cc786-125">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="cc786-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="cc786-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cc786-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cc786-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cc786-127">Vertex</span></span> | <span data-ttu-id="cc786-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="cc786-128">Hull</span></span> | <span data-ttu-id="cc786-129">Domain</span><span class="sxs-lookup"><span data-stu-id="cc786-129">Domain</span></span> | <span data-ttu-id="cc786-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cc786-130">Geometry</span></span> | <span data-ttu-id="cc786-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="cc786-131">Pixel</span></span> | <span data-ttu-id="cc786-132">Compute</span><span class="sxs-lookup"><span data-stu-id="cc786-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cc786-133">x</span><span class="sxs-lookup"><span data-stu-id="cc786-133">x</span></span>     | <span data-ttu-id="cc786-134">x</span><span class="sxs-lookup"><span data-stu-id="cc786-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cc786-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc786-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc786-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="cc786-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="cc786-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="cc786-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
