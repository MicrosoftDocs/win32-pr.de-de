---
description: Berechnet das Produkt von zwei sphärischen Oberschwingungen-Funktionen (f und g). Beide Funktionen sind in der Reihenfolge N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: D3DXSHMultiply5-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b43fb89bdd5d6f75a4adca86323786d4a2bddac1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355576"
---
# <a name="d3dxshmultiply5-function"></a><span data-ttu-id="c33b0-104">D3DXSHMultiply5-Funktion</span><span class="sxs-lookup"><span data-stu-id="c33b0-104">D3DXSHMultiply5 function</span></span>

<span data-ttu-id="c33b0-105">Berechnet das Produkt von zwei sphärischen Oberschwingungen-Funktionen (f und g).</span><span class="sxs-lookup"><span data-stu-id="c33b0-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="c33b0-106">Beide Funktionen sind in der Reihenfolge N = 5.</span><span class="sxs-lookup"><span data-stu-id="c33b0-106">Both functions are of order N = 5.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c33b0-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply5(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="c33b0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c33b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33b0-109">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33b0-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33b0-110">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c33b0-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33b0-111">Zeiger auf die Ausgabe-SH-Koeffizienten – die Basis Funktion *Y* LM wird in *l*² + *m* + l gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c33b0-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at *l*² + *m* + l.</span></span> <span data-ttu-id="c33b0-112">Die Reihenfolge n bestimmt die Länge des Arrays, bei der immer *N*² Koeffizienten vorhanden sein sollten.</span><span class="sxs-lookup"><span data-stu-id="c33b0-112">The order N determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="c33b0-113">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33b0-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33b0-114">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c33b0-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33b0-115">Geben Sie SH Koeffizienten für die erste Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="c33b0-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="c33b0-116">*PG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33b0-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33b0-117">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c33b0-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33b0-118">Zweiter Satz von Eingabe-SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="c33b0-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33b0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c33b0-119">Return value</span></span>

<span data-ttu-id="c33b0-120">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c33b0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33b0-121">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="c33b0-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33b0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c33b0-122">Remarks</span></span>

<span data-ttu-id="c33b0-123">Das Produkt der beiden SH-Funktionen von Order N = 5 generiert eine sh-Funktion der Reihenfolge 2 × *N* -1 = 9, die Ergebnisse werden jedoch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="c33b0-123">The product of two SH functions of order N = 5 generates an SH function of order 2 × *N* - 1 = 9, but the results are truncated.</span></span> <span data-ttu-id="c33b0-124">Dies bedeutet, dass das Produkt sich ( *f* × *g*  =   × × *f* ), aber nicht zuordnen lässt ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="c33b0-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="c33b0-125">Diese Funktion verwendet die folgende Gleichung:</span><span class="sxs-lookup"><span data-stu-id="c33b0-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="c33b0-126">dabei \_ ist y i (s) die Funktion "ITH sh", und f (s) und g (s) verwenden die folgende sh-Funktion:</span><span class="sxs-lookup"><span data-stu-id="c33b0-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="c33b0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c33b0-127">Requirements</span></span>



| <span data-ttu-id="c33b0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c33b0-128">Requirement</span></span> | <span data-ttu-id="c33b0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c33b0-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33b0-130">Header</span><span class="sxs-lookup"><span data-stu-id="c33b0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c33b0-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33b0-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c33b0-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c33b0-132">Library</span></span><br/> | <dl> <span data-ttu-id="c33b0-133"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c33b0-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c33b0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c33b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33b0-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c33b0-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
