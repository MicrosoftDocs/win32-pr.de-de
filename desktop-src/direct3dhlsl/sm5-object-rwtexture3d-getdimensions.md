---
title: 'RWTexture3D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | RWTexture3D:: GetDimensions-Funktion'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352968"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="4f41e-105">RWTexture3D:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f41e-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="4f41e-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="4f41e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f41e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f41e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="4f41e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f41e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f41e-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f41e-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f41e-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4f41e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4f41e-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="4f41e-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="4f41e-112">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f41e-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f41e-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4f41e-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4f41e-114">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="4f41e-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="4f41e-115">*Tiefe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f41e-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f41e-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4f41e-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4f41e-117">Die Ressourcen Tiefe in Texels.</span><span class="sxs-lookup"><span data-stu-id="4f41e-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f41e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f41e-118">Return value</span></span>

<span data-ttu-id="4f41e-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4f41e-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f41e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f41e-120">Remarks</span></span>

<span data-ttu-id="4f41e-121">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="4f41e-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="4f41e-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4f41e-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4f41e-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4f41e-123">Vertex</span></span> | <span data-ttu-id="4f41e-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="4f41e-124">Hull</span></span> | <span data-ttu-id="4f41e-125">Domain</span><span class="sxs-lookup"><span data-stu-id="4f41e-125">Domain</span></span> | <span data-ttu-id="4f41e-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4f41e-126">Geometry</span></span> | <span data-ttu-id="4f41e-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="4f41e-127">Pixel</span></span> | <span data-ttu-id="4f41e-128">Compute</span><span class="sxs-lookup"><span data-stu-id="4f41e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4f41e-129">x</span><span class="sxs-lookup"><span data-stu-id="4f41e-129">x</span></span>     | <span data-ttu-id="4f41e-130">x</span><span class="sxs-lookup"><span data-stu-id="4f41e-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4f41e-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f41e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f41e-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="4f41e-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="4f41e-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4f41e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
