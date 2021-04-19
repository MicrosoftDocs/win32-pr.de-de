---
description: Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: D3DXSHDot-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353750"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="1f582-103">D3DXSHDot-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="1f582-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="1f582-104">Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.</span><span class="sxs-lookup"><span data-stu-id="1f582-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f582-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f582-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="1f582-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f582-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f582-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f582-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f582-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f582-109">Reihenfolge der Auswertung der sphärischen Harmonika (SH).</span><span class="sxs-lookup"><span data-stu-id="1f582-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="1f582-110">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="1f582-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1f582-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="1f582-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1f582-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="1f582-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1f582-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f582-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f582-114">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f582-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1f582-115">Zeiger zum ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f582-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f582-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f582-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f582-117">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f582-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1f582-118">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f582-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f582-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f582-119">Return value</span></span>

<span data-ttu-id="1f582-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f582-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f582-121">SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1f582-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f582-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f582-122">Remarks</span></span>

<span data-ttu-id="1f582-123">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="1f582-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1f582-124">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="1f582-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1f582-125">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="1f582-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f582-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f582-126">Requirements</span></span>



| <span data-ttu-id="1f582-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f582-127">Requirement</span></span> | <span data-ttu-id="1f582-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1f582-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f582-129">Header</span><span class="sxs-lookup"><span data-stu-id="1f582-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1f582-130"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f582-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f582-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f582-131">Library</span></span><br/> | <dl> <span data-ttu-id="1f582-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f582-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f582-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f582-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f582-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1f582-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
