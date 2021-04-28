---
description: 'D3DXFresnelTerm-Funktion (D3dx9math.h): Berechnet den Fresnel-Begriff.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114478"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="42b1d-103">D3DXFresnelTerm-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="42b1d-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="42b1d-104">Berechnen Sie den Fresnel-Begriff.</span><span class="sxs-lookup"><span data-stu-id="42b1d-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b1d-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="42b1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42b1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b1d-107">*CosTheta* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42b1d-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b1d-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42b1d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42b1d-109">Der Wert muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="42b1d-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="42b1d-110">*RefractionIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42b1d-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b1d-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42b1d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42b1d-112">Der Refraktionsindex eines Materials.</span><span class="sxs-lookup"><span data-stu-id="42b1d-112">The refraction index of a material.</span></span> <span data-ttu-id="42b1d-113">Der Wert muss größer als 1 sein.</span><span class="sxs-lookup"><span data-stu-id="42b1d-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b1d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42b1d-114">Return value</span></span>

<span data-ttu-id="42b1d-115">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42b1d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42b1d-116">Diese Funktion gibt den Fresnel-Begriff für unisiertes Licht zurück.</span><span class="sxs-lookup"><span data-stu-id="42b1d-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="42b1d-117">CosTheta ist der Kosinus des Incidentwinkels.</span><span class="sxs-lookup"><span data-stu-id="42b1d-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b1d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42b1d-118">Remarks</span></span>

<span data-ttu-id="42b1d-119">So finden Sie den Fresnel-Begriff (F):</span><span class="sxs-lookup"><span data-stu-id="42b1d-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="42b1d-120">Wenn A ein Winkel von 1 und B der Winkel der Refraktion ist, dann</span><span class="sxs-lookup"><span data-stu-id="42b1d-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="42b1d-121">Wenn Sie dann mithilfe der Trig-Identitäten erweitern und vereinfachen, erhalten Sie:</span><span class="sxs-lookup"><span data-stu-id="42b1d-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="42b1d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42b1d-122">Requirements</span></span>



| <span data-ttu-id="42b1d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42b1d-123">Requirement</span></span> | <span data-ttu-id="42b1d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="42b1d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42b1d-125">Header</span><span class="sxs-lookup"><span data-stu-id="42b1d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="42b1d-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="42b1d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="42b1d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="42b1d-127">Library</span></span><br/> | <dl> <span data-ttu-id="42b1d-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="42b1d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42b1d-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42b1d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b1d-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="42b1d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
