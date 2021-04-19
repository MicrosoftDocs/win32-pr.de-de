---
description: Gibt eine Quaternion in baryzentrierten Koordinaten zurück.
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: D3DXQuaternionBaryCentric-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 002d235ab9957784c19b5e5a699dd87dfed74d4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373507"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="037de-103">D3DXQuaternionBaryCentric-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="037de-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="037de-104">Gibt eine Quaternion in baryzentrierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="037de-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="037de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="037de-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="037de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="037de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="037de-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="037de-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="037de-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="037de-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="037de-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="037de-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037de-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="037de-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="037de-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="037de-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="037de-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037de-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-114">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="037de-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="037de-115">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="037de-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="037de-116">*pQ3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037de-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-117">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="037de-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="037de-118">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="037de-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="037de-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037de-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="037de-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="037de-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="037de-121">Weighting factor.</span></span> <span data-ttu-id="037de-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="037de-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="037de-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037de-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037de-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="037de-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="037de-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="037de-125">Weighting factor.</span></span> <span data-ttu-id="037de-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="037de-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="037de-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="037de-127">Return value</span></span>

<span data-ttu-id="037de-128">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="037de-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="037de-129">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur in den baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="037de-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="037de-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="037de-130">Remarks</span></span>

<span data-ttu-id="037de-131">Zum Berechnen der barzentrischen Koordinaten implementiert die **D3DXQuaternionBaryCentric** -Funktion die folgende Reihe von sphärischen linearen Interpolations Vorgängen:</span><span class="sxs-lookup"><span data-stu-id="037de-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="037de-132">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="037de-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="037de-133">Auf diese Weise kann die **D3DXQuaternionBaryCentric** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="037de-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="037de-134">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="037de-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="037de-135">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="037de-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="037de-136">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="037de-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="037de-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037de-137">Requirements</span></span>



| <span data-ttu-id="037de-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037de-138">Requirement</span></span> | <span data-ttu-id="037de-139">Wert</span><span class="sxs-lookup"><span data-stu-id="037de-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="037de-140">Header</span><span class="sxs-lookup"><span data-stu-id="037de-140">Header</span></span><br/>  | <dl> <span data-ttu-id="037de-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="037de-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="037de-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="037de-142">Library</span></span><br/> | <dl> <span data-ttu-id="037de-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="037de-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="037de-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037de-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037de-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="037de-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
