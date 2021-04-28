---
description: 'D3DXQuaternionBaryCentric-Funktion (D3dx9math.h): Gibt eine Quaternion in barycentric-Koordinaten zurück.'
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: D3DXQuaternionBaryCentric-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ce0cfc7b3a59dc2a3cae6fa240015e70a035695
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094108"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="22abc-103">D3DXQuaternionBaryCentric-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="22abc-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="22abc-104">Gibt eine Quaternion in baryzentrischen Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="22abc-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="22abc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22abc-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="22abc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22abc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22abc-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="22abc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="22abc-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="22abc-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="22abc-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="22abc-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22abc-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="22abc-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="22abc-112">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="22abc-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="22abc-113">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22abc-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-114">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="22abc-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="22abc-115">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="22abc-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="22abc-116">*pQ3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22abc-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-117">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="22abc-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="22abc-118">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="22abc-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="22abc-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22abc-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22abc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22abc-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="22abc-121">Weighting factor.</span></span> <span data-ttu-id="22abc-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22abc-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="22abc-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22abc-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22abc-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22abc-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22abc-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="22abc-125">Weighting factor.</span></span> <span data-ttu-id="22abc-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="22abc-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22abc-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22abc-127">Return value</span></span>

<span data-ttu-id="22abc-128">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="22abc-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="22abc-129">Zeiger auf eine [**D3DXQUATERNION-Struktur**](d3dxquaternion.md) in baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="22abc-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="22abc-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22abc-130">Remarks</span></span>

<span data-ttu-id="22abc-131">Um die barytischen Koordinaten zu berechnen, implementiert die **D3DXQuaternionBaryCentric-Funktion** die folgende Reihe von pherischen linearen Interpolationsvorgängen:</span><span class="sxs-lookup"><span data-stu-id="22abc-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="22abc-132">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="22abc-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="22abc-133">Auf diese Weise kann die **D3DXQuaternionBaryCentric-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22abc-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="22abc-134">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="22abc-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="22abc-135">Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="22abc-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="22abc-136">Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="22abc-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="22abc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22abc-137">Requirements</span></span>



| <span data-ttu-id="22abc-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22abc-138">Requirement</span></span> | <span data-ttu-id="22abc-139">Wert</span><span class="sxs-lookup"><span data-stu-id="22abc-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22abc-140">Header</span><span class="sxs-lookup"><span data-stu-id="22abc-140">Header</span></span><br/>  | <dl> <span data-ttu-id="22abc-141"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="22abc-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="22abc-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22abc-142">Library</span></span><br/> | <dl> <span data-ttu-id="22abc-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="22abc-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22abc-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22abc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22abc-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="22abc-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
