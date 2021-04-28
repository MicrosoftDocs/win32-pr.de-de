---
description: D3DXSHDot-Funktion (D3dx9math.h) – Berechnet das Punktprodukt von zwei SH-Vektoren (PhericalIcalIcal, PhericalIcalIcal).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: D3DXSHDot-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093928"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="1f766-103">D3DXSHDot-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1f766-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="1f766-104">Berechnet das Punktprodukt von zwei SH-Vektoren (PhericalIcal).</span><span class="sxs-lookup"><span data-stu-id="1f766-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f766-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f766-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="1f766-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f766-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f766-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1f766-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f766-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f766-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f766-109">Reihenfolge der Sh-Auswertung (PhericalIcalIcal).</span><span class="sxs-lookup"><span data-stu-id="1f766-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="1f766-110">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="1f766-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1f766-111">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1f766-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1f766-112">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="1f766-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1f766-113">*pA* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1f766-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f766-114">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f766-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1f766-115">Zeiger auf den ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f766-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f766-116">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1f766-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f766-117">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f766-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1f766-118">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f766-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f766-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f766-119">Return value</span></span>

<span data-ttu-id="1f766-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f766-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f766-121">SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1f766-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f766-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f766-122">Remarks</span></span>

<span data-ttu-id="1f766-123">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="1f766-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1f766-124">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="1f766-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1f766-125">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="1f766-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f766-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f766-126">Requirements</span></span>



| <span data-ttu-id="1f766-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f766-127">Requirement</span></span> | <span data-ttu-id="1f766-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1f766-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f766-129">Header</span><span class="sxs-lookup"><span data-stu-id="1f766-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1f766-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1f766-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1f766-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f766-131">Library</span></span><br/> | <dl> <span data-ttu-id="1f766-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f766-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f766-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f766-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f766-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1f766-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1f766-135">Vorausberechnen der Übertragungsstärke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1f766-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
