---
description: Führt eine aufgenommene Spline-interpolung mithilfe der angegebenen 4D-Vektoren aus.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: D3DXVec4Hermite-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219551"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a><span data-ttu-id="10fe1-103">D3DXVec4Hermite-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="10fe1-103">D3DXVec4Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="10fe1-104">Führt eine aufgenommene Spline-interpolung mithilfe der angegebenen 4D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="10fe1-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="10fe1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10fe1-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="10fe1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10fe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fe1-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="10fe1-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="10fe1-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="10fe1-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="10fe1-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="10fe1-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="10fe1-113">*pT1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="10fe1-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-115">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Quell Struktur, ein Tangens Vektor.</span><span class="sxs-lookup"><span data-stu-id="10fe1-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="10fe1-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-117">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="10fe1-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-118">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="10fe1-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="10fe1-119">*PT2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-120">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="10fe1-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-121">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Quell Struktur, ein Tangens Vektor.</span><span class="sxs-lookup"><span data-stu-id="10fe1-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="10fe1-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fe1-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fe1-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10fe1-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10fe1-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="10fe1-124">Weighting factor.</span></span> <span data-ttu-id="10fe1-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="10fe1-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fe1-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10fe1-126">Return value</span></span>

<span data-ttu-id="10fe1-127">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="10fe1-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="10fe1-128">Ein Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis der Hermite-Spline-interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="10fe1-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="10fe1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10fe1-129">Remarks</span></span>

<span data-ttu-id="10fe1-130">Die **D3DXVec4Hermite** -Funktion interpoliert von (positiona, tangenta) bis (positionb, tangentb) mithilfe der herdie Spline-Interpolation.</span><span class="sxs-lookup"><span data-stu-id="10fe1-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="10fe1-131">Die Spline-interpolung ist eine Generalisierung der Easy-in-Easy-out-Spline.</span><span class="sxs-lookup"><span data-stu-id="10fe1-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="10fe1-132">Die-Rampe ist eine Funktion von Q (s) mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10fe1-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="10fe1-133">Q (s) = As ³ + b ² + CS + D (und somit q ' (s) = 3AS ² + 2B + C)</span><span class="sxs-lookup"><span data-stu-id="10fe1-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="10fe1-134">a) q (0) = v1, also q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="10fe1-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="10fe1-135">b) q (1) = v2, also q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="10fe1-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="10fe1-136">v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, T1 ist der Inhalt von pT1, und T2 ist der Inhalt von PT2.</span><span class="sxs-lookup"><span data-stu-id="10fe1-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="10fe1-137">Diese Eigenschaften werden verwendet, um für A, B, C, D zu lösen.</span><span class="sxs-lookup"><span data-stu-id="10fe1-137">These properties are used to solve for A, B, C, D.</span></span>

<span data-ttu-id="10fe1-138">Binden Sie die Lösungen für A, B, C und D ein, um Q (s) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="10fe1-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="10fe1-139">Dies ergibt:</span><span class="sxs-lookup"><span data-stu-id="10fe1-139">This yields:</span></span>

<span data-ttu-id="10fe1-140">Q (s) = (2v1-2v2 + T2 + T1) s ³ + (3v2-3v1-2t1-T2) s ² + T1S + v1</span><span class="sxs-lookup"><span data-stu-id="10fe1-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="10fe1-141">Diese können wie folgt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="10fe1-141">Which can be rearranged as:</span></span>

<span data-ttu-id="10fe1-142">Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="10fe1-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="10fe1-143">Hermite-Splines sind zum Steuern der Animation nützlich, da die Kurve alle Steuerungs Punkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="10fe1-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="10fe1-144">Da die Position und der Tangens an den Enden der einzelnen Segmente explizit angegeben werden, ist es einfach, eine C2-kontinuierliche Kurve zu erstellen, solange Sie sicherstellen, dass die Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="10fe1-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="10fe1-145">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10fe1-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="10fe1-146">Auf diese Weise kann die **D3DXVec4Hermite** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10fe1-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fe1-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10fe1-147">Requirements</span></span>



| <span data-ttu-id="10fe1-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10fe1-148">Requirement</span></span> | <span data-ttu-id="10fe1-149">Wert</span><span class="sxs-lookup"><span data-stu-id="10fe1-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10fe1-150">Header</span><span class="sxs-lookup"><span data-stu-id="10fe1-150">Header</span></span><br/>  | <dl> <span data-ttu-id="10fe1-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fe1-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="10fe1-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10fe1-152">Library</span></span><br/> | <dl> <span data-ttu-id="10fe1-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10fe1-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10fe1-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10fe1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fe1-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="10fe1-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
