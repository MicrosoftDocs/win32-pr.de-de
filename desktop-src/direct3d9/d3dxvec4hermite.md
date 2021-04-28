---
description: 'D3DXVec4Hermite-Funktion (D3dx9math.h): Führt eine Hermite-Splineinterpolation mithilfe der angegebenen 4D-Vektoren aus.'
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: D3DXVec4Hermite-Funktion (D3dx9math.h)
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
ms.openlocfilehash: b08ed785c24ba9580be0fc7f620a471ea96184a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097698"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a><span data-ttu-id="c3e5b-103">D3DXVec4Hermite-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c3e5b-103">D3DXVec4Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="c3e5b-104">Führt eine Hermite-Splineinterpolation mithilfe der angegebenen 4D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e5b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c3e5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3e5b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c3e5b-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-112">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="c3e5b-113">*pT1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-114">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-115">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Tangensvektor.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="c3e5b-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-117">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-118">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="c3e5b-119">*pT2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-120">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-121">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Tangensvektor.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="c3e5b-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3e5b-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e5b-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3e5b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3e5b-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-124">Weighting factor.</span></span> <span data-ttu-id="c3e5b-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3e5b-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3e5b-126">Return value</span></span>

<span data-ttu-id="c3e5b-127">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3e5b-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3e5b-128">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis der Hermite-Splineinterpolation ist.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3e5b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3e5b-129">Remarks</span></span>

<span data-ttu-id="c3e5b-130">Die **D3DXVec4Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) nach (positionB, tangentB).</span><span class="sxs-lookup"><span data-stu-id="c3e5b-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="c3e5b-131">Die Splineinterpolation ist eine Verallgemeinerung des Splines mit einfacherEntschärfung.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="c3e5b-132">Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="c3e5b-133">Q(s) = Assstelle + Bssstelle + Cs + D (und daher Q(s) = 3Aszept + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="c3e5b-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="c3e5b-134">a) Q(0) = v1, also Q'(0) = t1</span><span class="sxs-lookup"><span data-stu-id="c3e5b-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="c3e5b-135">b) Q(1) = v2, also Q'(1) = t2</span><span class="sxs-lookup"><span data-stu-id="c3e5b-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="c3e5b-136">v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 ist der Inhalt von pT2.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="c3e5b-137">Diese Eigenschaften werden für A, B, C, D verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-137">These properties are used to solve for A, B, C, D.</span></span>

<span data-ttu-id="c3e5b-138">Schließen Sie die Lösungen für A, B, C und D ein, um Q(s) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="c3e5b-139">Dies ergibt:</span><span class="sxs-lookup"><span data-stu-id="c3e5b-139">This yields:</span></span>

<span data-ttu-id="c3e5b-140">Q(s) = (2v1 - 2v2 + t2 + t1)ssstelle + (3v2 - 3v1 - 2t1 - t2)stif + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="c3e5b-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="c3e5b-141">Dies kann wie hier angezeigt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="c3e5b-141">Which can be rearranged as:</span></span>

<span data-ttu-id="c3e5b-142">Q(s) = (2ssstelle – 3ssstelle + 1)v1 + (-2ssstelle + 3ssstelle)v2 + (ssstelle – 2ssstelle + s)t1 + (ssstelle – ssstelle)t2</span><span class="sxs-lookup"><span data-stu-id="c3e5b-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="c3e5b-143">Hermite-Splines sind nützlich zum Steuern der Animation, da die Kurve alle Kontrollpunkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="c3e5b-144">Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="c3e5b-145">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c3e5b-146">Auf diese Weise kann die **D3DXVec4Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3e5b-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3e5b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e5b-147">Requirements</span></span>



| <span data-ttu-id="c3e5b-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e5b-148">Requirement</span></span> | <span data-ttu-id="c3e5b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="c3e5b-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e5b-150">Header</span><span class="sxs-lookup"><span data-stu-id="c3e5b-150">Header</span></span><br/>  | <dl> <span data-ttu-id="c3e5b-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c3e5b-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c3e5b-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3e5b-152">Library</span></span><br/> | <dl> <span data-ttu-id="c3e5b-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3e5b-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3e5b-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3e5b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e5b-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c3e5b-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
