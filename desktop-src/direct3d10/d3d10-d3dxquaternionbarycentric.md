---
description: 'D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h): Gibt eine Quaternion in baryzentrischen Koordinaten zurück.'
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d8e41a0173b7b26083f38beb82417365ef7067
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108778"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="52b8d-103">D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="52b8d-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="52b8d-104">Gibt eine Quaternion in baryzentrischen Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="52b8d-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52b8d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="52b8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52b8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52b8d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52b8d-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52b8d-109">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="52b8d-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="52b8d-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52b8d-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52b8d-112">Zeiger auf eine D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="52b8d-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="52b8d-113">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-114">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52b8d-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52b8d-115">Zeiger auf eine D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="52b8d-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="52b8d-116">*pQ3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-117">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52b8d-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52b8d-118">Zeiger auf eine D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="52b8d-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="52b8d-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52b8d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52b8d-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="52b8d-121">Weighting factor.</span></span> <span data-ttu-id="52b8d-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="52b8d-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="52b8d-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52b8d-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b8d-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52b8d-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52b8d-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="52b8d-125">Weighting factor.</span></span> <span data-ttu-id="52b8d-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="52b8d-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52b8d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52b8d-127">Return value</span></span>

<span data-ttu-id="52b8d-128">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52b8d-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52b8d-129">Zeiger auf eine D3DXQUATERNION-Struktur in baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="52b8d-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="52b8d-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52b8d-130">Remarks</span></span>

<span data-ttu-id="52b8d-131">Um die barytischen Koordinaten zu berechnen, implementiert die D3DXQuaternionBaryCentric-Funktion die folgende Reihe von pherischen linearen Interpolationsvorgängen:</span><span class="sxs-lookup"><span data-stu-id="52b8d-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="52b8d-132">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="52b8d-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="52b8d-133">Auf diese Weise kann die D3DXQuaternionBaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52b8d-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="52b8d-134">Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="52b8d-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="52b8d-135">Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="52b8d-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="52b8d-136">Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="52b8d-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="52b8d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52b8d-137">Requirements</span></span>



| <span data-ttu-id="52b8d-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52b8d-138">Requirement</span></span> | <span data-ttu-id="52b8d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="52b8d-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52b8d-140">Header</span><span class="sxs-lookup"><span data-stu-id="52b8d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="52b8d-141"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="52b8d-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="52b8d-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52b8d-142">Library</span></span><br/> | <dl> <span data-ttu-id="52b8d-143"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="52b8d-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52b8d-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52b8d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b8d-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="52b8d-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
