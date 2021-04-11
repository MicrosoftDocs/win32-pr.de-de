---
description: Berechnen Sie den Fresnel-Begriff.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm-Funktion (D3dx9math. h)
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
ms.openlocfilehash: ed6c6dd19dd6b7b70c5eeb08051f9799756b0782
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354846"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="9067c-103">D3DXFresnelTerm-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9067c-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="9067c-104">Berechnen Sie den Fresnel-Begriff.</span><span class="sxs-lookup"><span data-stu-id="9067c-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="9067c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9067c-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="9067c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9067c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9067c-107">*Kostheta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9067c-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9067c-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9067c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9067c-109">Der Wert muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="9067c-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="9067c-110">" *Refractionindex* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="9067c-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9067c-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9067c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9067c-112">Der abbrechungs Index eines Materials.</span><span class="sxs-lookup"><span data-stu-id="9067c-112">The refraction index of a material.</span></span> <span data-ttu-id="9067c-113">Der Wert muss größer als 1 sein.</span><span class="sxs-lookup"><span data-stu-id="9067c-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9067c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9067c-114">Return value</span></span>

<span data-ttu-id="9067c-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9067c-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9067c-116">Diese Funktion gibt den Fresnel-Begriff für nicht polarisiertes Licht zurück.</span><span class="sxs-lookup"><span data-stu-id="9067c-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="9067c-117">Costheta ist der Kosinus des Vorfall Winkels.</span><span class="sxs-lookup"><span data-stu-id="9067c-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="9067c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9067c-118">Remarks</span></span>

<span data-ttu-id="9067c-119">So finden Sie den Fresnel-Begriff (F):</span><span class="sxs-lookup"><span data-stu-id="9067c-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="9067c-120">Wenn ein der Winkel des Auftretens und B der Winkel der abbrechungs Angabe ist, dann</span><span class="sxs-lookup"><span data-stu-id="9067c-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="9067c-121">Wenn Sie die drei-und Vereinfachung verwenden, erhalten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9067c-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="9067c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9067c-122">Requirements</span></span>



| <span data-ttu-id="9067c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9067c-123">Requirement</span></span> | <span data-ttu-id="9067c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9067c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9067c-125">Header</span><span class="sxs-lookup"><span data-stu-id="9067c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9067c-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9067c-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9067c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9067c-127">Library</span></span><br/> | <dl> <span data-ttu-id="9067c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9067c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9067c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9067c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9067c-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9067c-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
