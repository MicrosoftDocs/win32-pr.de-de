---
description: Berechnen Sie den Fresnel-Begriff.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: D3DXFresnelTerm-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531052"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="cfb3e-103">D3DXFresnelTerm-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cfb3e-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="cfb3e-104">Berechnen Sie den Fresnel-Begriff.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb3e-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="cfb3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb3e-107">*Kostheta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb3e-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb3e-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfb3e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfb3e-109">Der Wert muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="cfb3e-110">" *Refractionindex* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="cfb3e-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb3e-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfb3e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfb3e-112">Der abbrechungs Index eines Materials.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-112">The refraction index of a material.</span></span> <span data-ttu-id="cfb3e-113">Der Wert muss größer als 1 sein.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb3e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfb3e-114">Return value</span></span>

<span data-ttu-id="cfb3e-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfb3e-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfb3e-116">Diese Funktion gibt den Fresnel-Begriff für nicht polarisiertes Licht zurück.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="cfb3e-117">Costheta ist der Kosinus des Vorfall Winkels.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb3e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb3e-118">Remarks</span></span>

<span data-ttu-id="cfb3e-119">So finden Sie den Fresnel-Begriff (F):</span><span class="sxs-lookup"><span data-stu-id="cfb3e-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="cfb3e-120">Wenn ein der Winkel des Auftretens und B der Winkel der abbrechungs Angabe ist, dann</span><span class="sxs-lookup"><span data-stu-id="cfb3e-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="cfb3e-121">Wenn Sie die drei-und Vereinfachung verwenden, erhalten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cfb3e-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="cfb3e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb3e-122">Requirements</span></span>



| <span data-ttu-id="cfb3e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb3e-123">Requirement</span></span> | <span data-ttu-id="cfb3e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb3e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb3e-125">Header</span><span class="sxs-lookup"><span data-stu-id="cfb3e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cfb3e-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb3e-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cfb3e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfb3e-127">Library</span></span><br/> | <dl> <span data-ttu-id="cfb3e-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfb3e-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cfb3e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb3e-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cfb3e-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
