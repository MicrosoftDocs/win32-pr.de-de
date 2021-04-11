---
description: 'Skaliert einen kugelförmigen Vektor (SH). Anders ausgedrückt: Pout \[ i \] = PA \[ i \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: D3DXSHScale-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 1a8cc7c63880876f85969443502db3d5fb3278c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132325"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="50ff0-103">D3DXSHScale-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="50ff0-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="50ff0-104">Skaliert einen kugelförmigen Vektor (SH). Anders ausgedrückt: Pout \[ i \] = PA \[ i \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="50ff0-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ff0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50ff0-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="50ff0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50ff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50ff0-107">*Pout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50ff0-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50ff0-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="50ff0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="50ff0-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="50ff0-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="50ff0-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="50ff0-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="50ff0-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="50ff0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="50ff0-112">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50ff0-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ff0-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50ff0-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50ff0-114">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="50ff0-114">Order of the SH evaluation.</span></span> <span data-ttu-id="50ff0-115">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="50ff0-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="50ff0-116">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="50ff0-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="50ff0-117">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="50ff0-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="50ff0-118">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50ff0-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ff0-119">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="50ff0-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="50ff0-120">Zeiger auf den zu skalierbaren SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="50ff0-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="50ff0-121">*Skalieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50ff0-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ff0-122">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="50ff0-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="50ff0-123">Zeiger auf den Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="50ff0-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50ff0-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50ff0-124">Return value</span></span>

<span data-ttu-id="50ff0-125">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="50ff0-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="50ff0-126">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="50ff0-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="50ff0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50ff0-127">Remarks</span></span>

<span data-ttu-id="50ff0-128">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="50ff0-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="50ff0-129">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="50ff0-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="50ff0-130">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="50ff0-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ff0-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50ff0-131">Requirements</span></span>



| <span data-ttu-id="50ff0-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50ff0-132">Requirement</span></span> | <span data-ttu-id="50ff0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="50ff0-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50ff0-134">Header</span><span class="sxs-lookup"><span data-stu-id="50ff0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="50ff0-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ff0-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="50ff0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50ff0-136">Library</span></span><br/> | <dl> <span data-ttu-id="50ff0-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50ff0-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50ff0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50ff0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ff0-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="50ff0-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="50ff0-140">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="50ff0-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
