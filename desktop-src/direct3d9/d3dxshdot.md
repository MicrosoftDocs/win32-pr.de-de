---
description: Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: D3DXSHDot-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a69ee929c889232cb29ff1b556dd08ab65a0d6d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394118"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="e4b3d-103">D3DXSHDot-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e4b3d-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="e4b3d-104">Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4b3d-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="e4b3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4b3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b3d-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4b3d-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b3d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4b3d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4b3d-109">Reihenfolge der Auswertung der sphärischen Harmonika (SH).</span><span class="sxs-lookup"><span data-stu-id="e4b3d-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="e4b3d-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e4b3d-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e4b3d-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e4b3d-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4b3d-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b3d-114">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4b3d-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4b3d-115">Zeiger zum ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="e4b3d-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4b3d-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b3d-117">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4b3d-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4b3d-118">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b3d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4b3d-119">Return value</span></span>

<span data-ttu-id="e4b3d-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4b3d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4b3d-121">SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b3d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4b3d-122">Remarks</span></span>

<span data-ttu-id="e4b3d-123">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="e4b3d-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e4b3d-124">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="e4b3d-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e4b3d-125">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="e4b3d-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b3d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4b3d-126">Requirements</span></span>



| <span data-ttu-id="e4b3d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4b3d-127">Requirement</span></span> | <span data-ttu-id="e4b3d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e4b3d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b3d-129">Header</span><span class="sxs-lookup"><span data-stu-id="e4b3d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b3d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b3d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4b3d-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4b3d-131">Library</span></span><br/> | <dl> <span data-ttu-id="e4b3d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4b3d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4b3d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4b3d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b3d-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4b3d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4b3d-135">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e4b3d-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
