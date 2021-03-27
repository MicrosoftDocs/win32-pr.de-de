---
title: 'RWTexture2D:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | RWTexture2D:: GetDimensions-Funktion'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132264"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="3b508-105">RWTexture2D:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b508-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="3b508-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="3b508-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b508-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b508-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="3b508-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b508-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b508-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3b508-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b508-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b508-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b508-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="3b508-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3b508-112">*Höhe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3b508-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b508-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b508-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b508-114">Die Ressourcen Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="3b508-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b508-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b508-115">Return value</span></span>

<span data-ttu-id="3b508-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3b508-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b508-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b508-117">Remarks</span></span>

<span data-ttu-id="3b508-118">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="3b508-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="3b508-119">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3b508-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3b508-120">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3b508-120">Vertex</span></span> | <span data-ttu-id="3b508-121">Hülle</span><span class="sxs-lookup"><span data-stu-id="3b508-121">Hull</span></span> | <span data-ttu-id="3b508-122">Domain</span><span class="sxs-lookup"><span data-stu-id="3b508-122">Domain</span></span> | <span data-ttu-id="3b508-123">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3b508-123">Geometry</span></span> | <span data-ttu-id="3b508-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="3b508-124">Pixel</span></span> | <span data-ttu-id="3b508-125">Compute</span><span class="sxs-lookup"><span data-stu-id="3b508-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3b508-126">x</span><span class="sxs-lookup"><span data-stu-id="3b508-126">x</span></span>     | <span data-ttu-id="3b508-127">x</span><span class="sxs-lookup"><span data-stu-id="3b508-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3b508-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b508-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b508-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="3b508-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="3b508-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3b508-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
