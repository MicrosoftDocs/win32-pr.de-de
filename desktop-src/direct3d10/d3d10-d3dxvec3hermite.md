---
description: 'D3DXVec3Hermite-Funktion (D3DX10Math.h): Führt eine Hermite-Splineinterpolation mit den angegebenen 3D-Vektoren aus.'
ms.assetid: d2212299-0478-48a6-b303-60c212528058
title: D3DXVec3Hermite-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cbed5ceaca1e4e404c47766fa41b8b095216b277
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108188"
---
# <a name="d3dxvec3hermite-function-d3dx10mathh"></a><span data-ttu-id="7d46a-103">D3DXVec3Hermite-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7d46a-103">D3DXVec3Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="7d46a-104">Führt eine Hermite-Splineinterpolation unter Verwendung der angegebenen 3D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="7d46a-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d46a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d46a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="7d46a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d46a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d46a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d46a-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7d46a-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d46a-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d46a-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-112">Zeiger auf eine D3DXVECTOR3-Quellstruktur, einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="7d46a-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="7d46a-113">*pT1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d46a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-115">Zeiger auf eine D3DXVECTOR3-Quellstruktur, einen Tangensvektor.</span><span class="sxs-lookup"><span data-stu-id="7d46a-115">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="7d46a-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d46a-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-118">Zeiger auf eine D3DXVECTOR3-Quellstruktur, einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="7d46a-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="7d46a-119">*pT2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-120">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d46a-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-121">Zeiger auf eine D3DXVECTOR3-Quellstruktur, einen Tangensvektor.</span><span class="sxs-lookup"><span data-stu-id="7d46a-121">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="7d46a-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d46a-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d46a-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d46a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d46a-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="7d46a-124">Weighting factor.</span></span> <span data-ttu-id="7d46a-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7d46a-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d46a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d46a-126">Return value</span></span>

<span data-ttu-id="7d46a-127">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d46a-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7d46a-128">Zeiger auf eine D3DXVECTOR3-Struktur, die das Ergebnis der Hermite-Splineinterpolation ist.</span><span class="sxs-lookup"><span data-stu-id="7d46a-128">Pointer to a D3DXVECTOR3 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d46a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d46a-129">Remarks</span></span>

<span data-ttu-id="7d46a-130">Die **D3DXVec3Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) in (positionB, tangentB).</span><span class="sxs-lookup"><span data-stu-id="7d46a-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="7d46a-131">Die Splineinterpolation ist eine Generalisierung der einfachen, einfachen Spline.</span><span class="sxs-lookup"><span data-stu-id="7d46a-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="7d46a-132">Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d46a-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="7d46a-133">Q(s) = As( + Bs) + Cs + D (und daher Q'(s) = 3As× + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="7d46a-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="7d46a-134">a) Q(0) = v1, also Q'(0) = t1</span><span class="sxs-lookup"><span data-stu-id="7d46a-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="7d46a-135">b) Q(1) = v2, also Q'(1) = t2</span><span class="sxs-lookup"><span data-stu-id="7d46a-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="7d46a-136">v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 der Inhalt von pT2.</span><span class="sxs-lookup"><span data-stu-id="7d46a-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="7d46a-137">Diese Eigenschaften werden zur Lösung für A, B, C, D verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d46a-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="7d46a-138">Schließen Sie die Lösungen für A, B, C und D ein, um Fragen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7d46a-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="7d46a-139">Dies ergibt:</span><span class="sxs-lookup"><span data-stu-id="7d46a-139">This yields:</span></span>

<span data-ttu-id="7d46a-140">Q(s) = (2v1 - 2v2 + t2 + t1)s) + (3v2 - 3v1 - 2t1 - t2)s× t1s + v1</span><span class="sxs-lookup"><span data-stu-id="7d46a-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="7d46a-141">Dies kann neu angeordnet werden wie:</span><span class="sxs-lookup"><span data-stu-id="7d46a-141">Which can be rearranged as:</span></span>

<span data-ttu-id="7d46a-142">Q(s) = (2s, 3s) + 1)v1 + (-2s, + 3s) v2 + (s= - 2s): + s)t1 + (s) - s2)t2</span><span class="sxs-lookup"><span data-stu-id="7d46a-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="7d46a-143">Einsemit-Splines sind nützlich, um Animationen zu steuern, da die Kurve alle Kontrollpunkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="7d46a-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="7d46a-144">Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7d46a-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="7d46a-145">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d46a-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7d46a-146">Auf diese Weise kann die **D3DXVec3Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d46a-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d46a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d46a-147">Requirements</span></span>



| <span data-ttu-id="7d46a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d46a-148">Requirement</span></span> | <span data-ttu-id="7d46a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="7d46a-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d46a-150">Header</span><span class="sxs-lookup"><span data-stu-id="7d46a-150">Header</span></span><br/> | <dl> <span data-ttu-id="7d46a-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7d46a-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d46a-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d46a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d46a-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7d46a-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
