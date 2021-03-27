---
title: 'Texture3D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture3D:: GetDimensions-Funktion'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995752"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="2f34a-105">Texture3D:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f34a-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="2f34a-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="2f34a-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f34a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f34a-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="2f34a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f34a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f34a-109">*Miplevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f34a-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f34a-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f34a-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f34a-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="2f34a-111">Optional.</span></span> <span data-ttu-id="2f34a-112">MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="2f34a-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="2f34a-113">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f34a-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f34a-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f34a-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f34a-115">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="2f34a-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2f34a-116">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f34a-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f34a-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f34a-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f34a-118">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="2f34a-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2f34a-119">*Tiefe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f34a-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f34a-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f34a-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f34a-121">Die Ressourcen Tiefe in Texels.</span><span class="sxs-lookup"><span data-stu-id="2f34a-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2f34a-122">*Nummerige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f34a-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f34a-123">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f34a-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2f34a-124">Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).</span><span class="sxs-lookup"><span data-stu-id="2f34a-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f34a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f34a-125">Return value</span></span>

<span data-ttu-id="2f34a-126">Nichts</span><span class="sxs-lookup"><span data-stu-id="2f34a-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="2f34a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f34a-127">Remarks</span></span>

<span data-ttu-id="2f34a-128">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="2f34a-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="2f34a-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2f34a-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2f34a-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2f34a-130">Vertex</span></span> | <span data-ttu-id="2f34a-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="2f34a-131">Hull</span></span> | <span data-ttu-id="2f34a-132">Domain</span><span class="sxs-lookup"><span data-stu-id="2f34a-132">Domain</span></span> | <span data-ttu-id="2f34a-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2f34a-133">Geometry</span></span> | <span data-ttu-id="2f34a-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="2f34a-134">Pixel</span></span> | <span data-ttu-id="2f34a-135">Compute</span><span class="sxs-lookup"><span data-stu-id="2f34a-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2f34a-136">x</span><span class="sxs-lookup"><span data-stu-id="2f34a-136">x</span></span>     | <span data-ttu-id="2f34a-137">x</span><span class="sxs-lookup"><span data-stu-id="2f34a-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2f34a-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f34a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f34a-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2f34a-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="2f34a-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2f34a-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
