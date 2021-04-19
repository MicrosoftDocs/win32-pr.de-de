---
description: Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden.
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: D3DXSHMultiply2-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355800"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="a809f-103">D3DXSHMultiply2-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a809f-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="a809f-104">Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a809f-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="a809f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a809f-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="a809f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a809f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a809f-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a809f-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a809f-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a809f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a809f-109">Ein Zeiger auf die Ausgabe-SH-Basis Funktion "ylm" wird in l \* l + m + l gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a809f-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="a809f-110">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a809f-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a809f-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a809f-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a809f-112">Geben Sie sh coeffs als erste Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="a809f-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="a809f-113">*PG* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a809f-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a809f-114">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a809f-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a809f-115">Der zweite Satz von Eingabe-SH-coeffs.</span><span class="sxs-lookup"><span data-stu-id="a809f-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a809f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a809f-116">Return value</span></span>

<span data-ttu-id="a809f-117">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a809f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a809f-118">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="a809f-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="a809f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a809f-119">Remarks</span></span>

<span data-ttu-id="a809f-120">Die Reihenfolge ist eine Zahl zwischen 2 und einschließlich 6.</span><span class="sxs-lookup"><span data-stu-id="a809f-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="a809f-121">Auf dieser Seite werden also mehrere Funktionen dokumentiert: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="a809f-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="a809f-122">Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden, wobei *Pout* \[ i \] = int (y i (s) f (s) \_ g (s)) ist \* \* , wobei y \_ i (s) die ITH-Basis Funktion ist, f (s) und g (s) SH Functions (Sum \_ i (y \_ i (s) \* c \_ i)).</span><span class="sxs-lookup"><span data-stu-id="a809f-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="a809f-123">Die Reihenfolge o bestimmt die Längen der Arrays, bei denen immer O ^ 2-Koeffizienten vorhanden sein sollten.</span><span class="sxs-lookup"><span data-stu-id="a809f-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="a809f-124">Im allgemeinen generiert das Produkt von zwei SH-Funktionen von Order O eine sh-Funktion von Order 2 \* O-1, aber die Ergebnisse werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a809f-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="a809f-125">Dies bedeutet, dass das Produkt sich (f \* g = = g \* f), aber nicht zuordnen lässt (f \* (g \* h)! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="a809f-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="a809f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a809f-126">Requirements</span></span>



| <span data-ttu-id="a809f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a809f-127">Requirement</span></span> | <span data-ttu-id="a809f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a809f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a809f-129">Header</span><span class="sxs-lookup"><span data-stu-id="a809f-129">Header</span></span><br/> | <dl> <span data-ttu-id="a809f-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a809f-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a809f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a809f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a809f-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a809f-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
