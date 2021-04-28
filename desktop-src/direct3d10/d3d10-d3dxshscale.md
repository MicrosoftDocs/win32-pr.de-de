---
description: 'D3DXSHScale-Funktion (D3DX10.h): Skaliert einen pherischen Vektor (SH) anders ausgedrückt: pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: D3DXSHScale-Funktion (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108498"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="3e465-103">D3DXSHScale-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="3e465-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="3e465-104">Skaliert einen Sh-Vektor (PhericalIcal). anders ausgedrückt: pOut \[ i \] = pA i \[ \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="3e465-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e465-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e465-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="3e465-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e465-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e465-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e465-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e465-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3e465-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical- und Pherical-Rumpf).</span><span class="sxs-lookup"><span data-stu-id="3e465-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="3e465-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3e465-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3e465-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3e465-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e465-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e465-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e465-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e465-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e465-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="3e465-114">Order of the SH evaluation.</span></span> <span data-ttu-id="3e465-115">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="3e465-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3e465-116">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3e465-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3e465-117">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="3e465-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3e465-118">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e465-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e465-119">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e465-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3e465-120">Zeiger auf den zu skalierenden SH-Vektor.</span><span class="sxs-lookup"><span data-stu-id="3e465-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="3e465-121">*Skalieren* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e465-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e465-122">Typ: **const [**FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e465-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e465-123">Zeiger auf den Skalierungswert.</span><span class="sxs-lookup"><span data-stu-id="3e465-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e465-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e465-124">Return value</span></span>

<span data-ttu-id="3e465-125">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e465-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3e465-126">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3e465-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e465-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e465-127">Remarks</span></span>

<span data-ttu-id="3e465-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="3e465-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="3e465-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="3e465-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="3e465-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="3e465-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e465-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e465-131">Requirements</span></span>



| <span data-ttu-id="3e465-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e465-132">Requirement</span></span> | <span data-ttu-id="3e465-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3e465-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e465-134">Header</span><span class="sxs-lookup"><span data-stu-id="3e465-134">Header</span></span><br/>  | <dl> <span data-ttu-id="3e465-135"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e465-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e465-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e465-136">Library</span></span><br/> | <dl> <span data-ttu-id="3e465-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e465-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e465-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e465-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e465-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3e465-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
