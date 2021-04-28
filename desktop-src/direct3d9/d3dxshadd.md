---
description: 'D3DXSHAdd-Funktion (D3dx9math.h) – Fügt zwei SH-Vektoren (PhericalIcalIcal, Pherical- Enzyprischen) hinzu; anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117958"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="068e0-103">D3DXSHAdd-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="068e0-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="068e0-104">Fügt zwei SH-Vektoren (PhericalIcal) hinzu. anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="068e0-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="068e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="068e0-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="068e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="068e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068e0-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="068e0-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="068e0-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="068e0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="068e0-109">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="068e0-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="068e0-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="068e0-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="068e0-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="068e0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="068e0-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="068e0-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068e0-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="068e0-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="068e0-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="068e0-114">Order of the SH evaluation.</span></span> <span data-ttu-id="068e0-115">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="068e0-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="068e0-116">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="068e0-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="068e0-117">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="068e0-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="068e0-118">*pA* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="068e0-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068e0-119">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="068e0-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="068e0-120">Zeiger auf den ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="068e0-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="068e0-121">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="068e0-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068e0-122">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="068e0-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="068e0-123">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="068e0-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068e0-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="068e0-124">Return value</span></span>

<span data-ttu-id="068e0-125">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="068e0-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="068e0-126">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="068e0-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="068e0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="068e0-127">Remarks</span></span>

<span data-ttu-id="068e0-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="068e0-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="068e0-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="068e0-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="068e0-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="068e0-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="068e0-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="068e0-131">Requirements</span></span>



| <span data-ttu-id="068e0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="068e0-132">Requirement</span></span> | <span data-ttu-id="068e0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="068e0-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="068e0-134">Header</span><span class="sxs-lookup"><span data-stu-id="068e0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="068e0-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="068e0-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="068e0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="068e0-136">Library</span></span><br/> | <dl> <span data-ttu-id="068e0-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="068e0-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="068e0-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="068e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068e0-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="068e0-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="068e0-140">Vorausberechnen der Übertragungsstärke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="068e0-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
