---
title: 'Texture1D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | Texture1D:: GetDimensions-Funktion'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530707"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="856f0-105">Texture1D:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="856f0-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="856f0-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="856f0-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="856f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="856f0-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="856f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="856f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856f0-109">*Miplevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="856f0-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="856f0-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="856f0-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="856f0-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="856f0-111">Optional.</span></span> <span data-ttu-id="856f0-112">MipMap-Ebene (muss angegeben werden, wenn " *numoflevels* " verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="856f0-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="856f0-113">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="856f0-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="856f0-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="856f0-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="856f0-115">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="856f0-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="856f0-116">*Nummerige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="856f0-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="856f0-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="856f0-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="856f0-118">Die Anzahl von MipMap-Ebenen (erfordert auch *miplevel* ).</span><span class="sxs-lookup"><span data-stu-id="856f0-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856f0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="856f0-119">Return value</span></span>

<span data-ttu-id="856f0-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="856f0-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="856f0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="856f0-121">Remarks</span></span>

<span data-ttu-id="856f0-122">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="856f0-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="856f0-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="856f0-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="856f0-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="856f0-124">Vertex</span></span> | <span data-ttu-id="856f0-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="856f0-125">Hull</span></span> | <span data-ttu-id="856f0-126">Domain</span><span class="sxs-lookup"><span data-stu-id="856f0-126">Domain</span></span> | <span data-ttu-id="856f0-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="856f0-127">Geometry</span></span> | <span data-ttu-id="856f0-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="856f0-128">Pixel</span></span> | <span data-ttu-id="856f0-129">Compute</span><span class="sxs-lookup"><span data-stu-id="856f0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="856f0-130">x</span><span class="sxs-lookup"><span data-stu-id="856f0-130">x</span></span>     | <span data-ttu-id="856f0-131">x</span><span class="sxs-lookup"><span data-stu-id="856f0-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="856f0-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="856f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856f0-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="856f0-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="856f0-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="856f0-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
