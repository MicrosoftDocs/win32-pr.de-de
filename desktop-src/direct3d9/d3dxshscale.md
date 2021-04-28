---
description: 'D3DXSHScale-Funktion (D3dx9math.h) – Skaliert einen SH-Vektor (Spherical Vector; Sphärische Entführung). mit anderen Worten: pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: D3DXSHScale-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093858"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="5d907-103">D3DXSHScale-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5d907-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="5d907-104">Skaliert einen Sphärischen Vektor (SH). mit anderen Worten: pOut \[ i \] = pA i \[ \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="5d907-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d907-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d907-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="5d907-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d907-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d907-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5d907-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d907-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d907-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d907-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical veralten).</span><span class="sxs-lookup"><span data-stu-id="5d907-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="5d907-110">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="5d907-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5d907-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5d907-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5d907-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5d907-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d907-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d907-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d907-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="5d907-114">Order of the SH evaluation.</span></span> <span data-ttu-id="5d907-115">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="5d907-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5d907-116">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="5d907-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5d907-117">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="5d907-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5d907-118">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5d907-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d907-119">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d907-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d907-120">Zeiger auf den sh-Vektor, der skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d907-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="5d907-121">*Skalieren* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5d907-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d907-122">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d907-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d907-123">Zeiger auf den Skalierungswert.</span><span class="sxs-lookup"><span data-stu-id="5d907-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d907-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d907-124">Return value</span></span>

<span data-ttu-id="5d907-125">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d907-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d907-126">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="5d907-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d907-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d907-127">Remarks</span></span>

<span data-ttu-id="5d907-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="5d907-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="5d907-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="5d907-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="5d907-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="5d907-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d907-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d907-131">Requirements</span></span>



| <span data-ttu-id="5d907-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d907-132">Requirement</span></span> | <span data-ttu-id="5d907-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5d907-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d907-134">Header</span><span class="sxs-lookup"><span data-stu-id="5d907-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5d907-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5d907-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5d907-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d907-136">Library</span></span><br/> | <dl> <span data-ttu-id="5d907-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d907-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d907-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d907-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d907-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d907-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5d907-140">Vorausberechnungsübertragung der Radiance (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5d907-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
