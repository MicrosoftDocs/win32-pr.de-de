---
description: 'D3DXSHDot-Funktion (D3DX10.h): Berechnet das Punktprodukt von zwei Sphärischen Vektoren (SH).'
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: D3DXSHDot-Funktion (D3DX10.h)
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
ms.openlocfilehash: 3ea3e839ff7a5fc038cf40a6402db4a358da8b39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108628"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="ba263-103">D3DXSHDot-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="ba263-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="ba263-104">Berechnet das Punktprodukt zweier Sphärischer Zynisierungsvektoren (SH).</span><span class="sxs-lookup"><span data-stu-id="ba263-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba263-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba263-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="ba263-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba263-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ba263-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba263-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba263-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba263-109">Die Reihenfolge der SH-Auswertung (SphericalLips).</span><span class="sxs-lookup"><span data-stu-id="ba263-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="ba263-110">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="ba263-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ba263-111">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="ba263-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ba263-112">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="ba263-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ba263-113">*pA* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ba263-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba263-114">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba263-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba263-115">Zeiger auf den ersten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ba263-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="ba263-116">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ba263-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba263-117">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba263-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba263-118">Zeiger auf den zweiten SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ba263-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba263-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba263-119">Return value</span></span>

<span data-ttu-id="ba263-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba263-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba263-121">SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="ba263-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba263-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba263-122">Remarks</span></span>

<span data-ttu-id="ba263-123">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="ba263-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="ba263-124">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="ba263-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="ba263-125">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="ba263-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba263-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba263-126">Requirements</span></span>



| <span data-ttu-id="ba263-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba263-127">Requirement</span></span> | <span data-ttu-id="ba263-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ba263-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba263-129">Header</span><span class="sxs-lookup"><span data-stu-id="ba263-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ba263-130"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ba263-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba263-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba263-131">Library</span></span><br/> | <dl> <span data-ttu-id="ba263-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba263-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba263-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ba263-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba263-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ba263-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
