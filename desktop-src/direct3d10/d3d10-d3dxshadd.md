---
description: 'D3DXSHAdd-Funktion (D3DX10.h): Fügt zwei SH-Vektoren (PhericalIcalIcal, Förmige Förmiges) hinzu; anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: D3DXSHAdd-Funktion (D3DX10.h)
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
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108658"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="42ade-103">D3DXSHAdd-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="42ade-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="42ade-104">Fügt zwei SH-Vektoren (PhericalIcal) hinzu. anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="42ade-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="42ade-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ade-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="42ade-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ade-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42ade-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42ade-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="42ade-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42ade-109">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="42ade-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="42ade-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="42ade-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="42ade-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="42ade-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42ade-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42ade-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42ade-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42ade-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42ade-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="42ade-114">Order of the SH evaluation.</span></span> <span data-ttu-id="42ade-115">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="42ade-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="42ade-116">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="42ade-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="42ade-117">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="42ade-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="42ade-118">*pA* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42ade-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42ade-119">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="42ade-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42ade-120">Zeiger auf den ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="42ade-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="42ade-121">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="42ade-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42ade-122">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="42ade-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42ade-123">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="42ade-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42ade-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42ade-124">Return value</span></span>

<span data-ttu-id="42ade-125">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="42ade-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42ade-126">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="42ade-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ade-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42ade-127">Remarks</span></span>

<span data-ttu-id="42ade-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="42ade-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="42ade-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="42ade-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="42ade-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="42ade-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ade-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42ade-131">Requirements</span></span>



| <span data-ttu-id="42ade-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42ade-132">Requirement</span></span> | <span data-ttu-id="42ade-133">Wert</span><span class="sxs-lookup"><span data-stu-id="42ade-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42ade-134">Header</span><span class="sxs-lookup"><span data-stu-id="42ade-134">Header</span></span><br/>  | <dl> <span data-ttu-id="42ade-135"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="42ade-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="42ade-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="42ade-136">Library</span></span><br/> | <dl> <span data-ttu-id="42ade-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="42ade-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ade-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42ade-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ade-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="42ade-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
