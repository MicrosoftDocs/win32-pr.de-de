---
description: 'Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .'
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: D3DXSHAdd-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219651"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="ad3f3-103">D3DXSHAdd-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="ad3f3-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="ad3f3-104">Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="ad3f3-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad3f3-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="ad3f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad3f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad3f3-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad3f3-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3f3-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad3f3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad3f3-109">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="ad3f3-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ad3f3-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad3f3-112">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad3f3-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3f3-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad3f3-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad3f3-114">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-114">Order of the SH evaluation.</span></span> <span data-ttu-id="ad3f3-115">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ad3f3-116">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ad3f3-117">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ad3f3-118">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad3f3-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3f3-119">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad3f3-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad3f3-120">Zeiger zum ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="ad3f3-121">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad3f3-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3f3-122">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad3f3-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad3f3-123">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad3f3-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad3f3-124">Return value</span></span>

<span data-ttu-id="ad3f3-125">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad3f3-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad3f3-126">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad3f3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad3f3-127">Remarks</span></span>

<span data-ttu-id="ad3f3-128">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="ad3f3-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="ad3f3-129">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad3f3-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="ad3f3-130">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="ad3f3-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3f3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad3f3-131">Requirements</span></span>



| <span data-ttu-id="ad3f3-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad3f3-132">Requirement</span></span> | <span data-ttu-id="ad3f3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ad3f3-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3f3-134">Header</span><span class="sxs-lookup"><span data-stu-id="ad3f3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ad3f3-135"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad3f3-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad3f3-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad3f3-136">Library</span></span><br/> | <dl> <span data-ttu-id="ad3f3-137"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad3f3-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad3f3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad3f3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3f3-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad3f3-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
