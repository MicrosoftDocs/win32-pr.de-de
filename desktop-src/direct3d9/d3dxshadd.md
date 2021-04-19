---
description: 'Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 6b8f65a14cf745e8b378728d4fa6e0a234284d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361856"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="91c3d-103">D3DXSHAdd-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="91c3d-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="91c3d-104">Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="91c3d-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="91c3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91c3d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="91c3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91c3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c3d-107">*Pout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91c3d-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3d-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91c3d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91c3d-109">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="91c3d-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="91c3d-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="91c3d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="91c3d-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="91c3d-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="91c3d-112">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c3d-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3d-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91c3d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91c3d-114">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="91c3d-114">Order of the SH evaluation.</span></span> <span data-ttu-id="91c3d-115">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="91c3d-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="91c3d-116">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="91c3d-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="91c3d-117">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="91c3d-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="91c3d-118">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c3d-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3d-119">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="91c3d-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91c3d-120">Zeiger zum ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="91c3d-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="91c3d-121">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c3d-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3d-122">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="91c3d-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91c3d-123">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="91c3d-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c3d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91c3d-124">Return value</span></span>

<span data-ttu-id="91c3d-125">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91c3d-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91c3d-126">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="91c3d-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c3d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91c3d-127">Remarks</span></span>

<span data-ttu-id="91c3d-128">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="91c3d-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="91c3d-129">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="91c3d-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="91c3d-130">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="91c3d-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c3d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91c3d-131">Requirements</span></span>



| <span data-ttu-id="91c3d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91c3d-132">Requirement</span></span> | <span data-ttu-id="91c3d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="91c3d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91c3d-134">Header</span><span class="sxs-lookup"><span data-stu-id="91c3d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="91c3d-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c3d-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="91c3d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91c3d-136">Library</span></span><br/> | <dl> <span data-ttu-id="91c3d-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91c3d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91c3d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91c3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c3d-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="91c3d-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="91c3d-140">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="91c3d-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
