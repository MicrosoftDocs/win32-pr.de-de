---
title: 'Texture2D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture2D:: GetDimensions-Funktion'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995630"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="cee6b-105">Texture2D:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="cee6b-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="cee6b-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="cee6b-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee6b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cee6b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="cee6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cee6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cee6b-109">*Miplevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cee6b-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cee6b-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="cee6b-110">Type: **uint**</span></span>

<span data-ttu-id="cee6b-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="cee6b-111">Optional.</span></span> <span data-ttu-id="cee6b-112">Die MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="cee6b-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="cee6b-113">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cee6b-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cee6b-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="cee6b-114">Type: **uint**</span></span>

<span data-ttu-id="cee6b-115">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="cee6b-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="cee6b-116">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cee6b-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cee6b-117">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="cee6b-117">Type: **uint**</span></span>

<span data-ttu-id="cee6b-118">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="cee6b-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="cee6b-119">*Nummerige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cee6b-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cee6b-120">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="cee6b-120">Type: **uint**</span></span>

<span data-ttu-id="cee6b-121">Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).</span><span class="sxs-lookup"><span data-stu-id="cee6b-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cee6b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cee6b-122">Return value</span></span>

<span data-ttu-id="cee6b-123">Nichts</span><span class="sxs-lookup"><span data-stu-id="cee6b-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="cee6b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cee6b-124">Remarks</span></span>

<span data-ttu-id="cee6b-125">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="cee6b-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="cee6b-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cee6b-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cee6b-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cee6b-127">Vertex</span></span> | <span data-ttu-id="cee6b-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="cee6b-128">Hull</span></span> | <span data-ttu-id="cee6b-129">Domain</span><span class="sxs-lookup"><span data-stu-id="cee6b-129">Domain</span></span> | <span data-ttu-id="cee6b-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cee6b-130">Geometry</span></span> | <span data-ttu-id="cee6b-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="cee6b-131">Pixel</span></span> | <span data-ttu-id="cee6b-132">Compute</span><span class="sxs-lookup"><span data-stu-id="cee6b-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cee6b-133">x</span><span class="sxs-lookup"><span data-stu-id="cee6b-133">x</span></span>     | <span data-ttu-id="cee6b-134">x</span><span class="sxs-lookup"><span data-stu-id="cee6b-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cee6b-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cee6b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee6b-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="cee6b-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="cee6b-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="cee6b-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




