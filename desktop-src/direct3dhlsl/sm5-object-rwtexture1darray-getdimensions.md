---
title: 'RWTexture1DArray:: GetDimensions-Funktion'
description: 'Gibt die Dimensionen der Ressource zurück. | RWTexture1DArray:: GetDimensions-Funktion'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219274"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="7cfea-105">RWTexture1DArray:: GetDimensions-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cfea-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="7cfea-106">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="7cfea-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cfea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cfea-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="7cfea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cfea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cfea-109">*Breite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7cfea-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfea-110">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7cfea-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7cfea-111">Die Ressourcen Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="7cfea-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7cfea-112">*Elemente* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7cfea-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfea-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7cfea-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7cfea-114">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="7cfea-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cfea-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cfea-115">Return value</span></span>

<span data-ttu-id="7cfea-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7cfea-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cfea-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cfea-117">Remarks</span></span>

<span data-ttu-id="7cfea-118">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="7cfea-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="7cfea-119">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7cfea-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7cfea-120">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7cfea-120">Vertex</span></span> | <span data-ttu-id="7cfea-121">Hülle</span><span class="sxs-lookup"><span data-stu-id="7cfea-121">Hull</span></span> | <span data-ttu-id="7cfea-122">Domain</span><span class="sxs-lookup"><span data-stu-id="7cfea-122">Domain</span></span> | <span data-ttu-id="7cfea-123">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7cfea-123">Geometry</span></span> | <span data-ttu-id="7cfea-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="7cfea-124">Pixel</span></span> | <span data-ttu-id="7cfea-125">Compute</span><span class="sxs-lookup"><span data-stu-id="7cfea-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7cfea-126">x</span><span class="sxs-lookup"><span data-stu-id="7cfea-126">x</span></span>     | <span data-ttu-id="7cfea-127">x</span><span class="sxs-lookup"><span data-stu-id="7cfea-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7cfea-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7cfea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cfea-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="7cfea-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="7cfea-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7cfea-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
