---
description: 'D3DXSHRotateZ-Funktion (D3dx9math.h): Rotiert den SH-Vektor (Pherical Rotation) in der Z-Achse um den angegebenen Winkel.'
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: D3DXSHRotateZ-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117848"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="e4a01-103">D3DXSHRotateZ-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e4a01-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="e4a01-104">Dreht den SH-Vektor (Pherical Rotation) in der Z-Achse um den angegebenen Winkel.</span><span class="sxs-lookup"><span data-stu-id="e4a01-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a01-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="e4a01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4a01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a01-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4a01-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a01-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4a01-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4a01-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical- oder Pherical-Rumpf).</span><span class="sxs-lookup"><span data-stu-id="e4a01-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="e4a01-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4a01-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e4a01-111">Dieser Zeiger sollte keinen Alias mit *pIn verwenden.*</span><span class="sxs-lookup"><span data-stu-id="e4a01-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="e4a01-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4a01-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e4a01-113">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e4a01-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a01-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a01-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4a01-115">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="e4a01-115">Order of the SH evaluation.</span></span> <span data-ttu-id="e4a01-116">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="e4a01-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e4a01-117">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4a01-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e4a01-118">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="e4a01-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e4a01-119">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e4a01-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a01-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a01-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4a01-121">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="e4a01-121">Rotation angle in radians.</span></span> <span data-ttu-id="e4a01-122">Die Drehung erfolgt um die Z-Achse.</span><span class="sxs-lookup"><span data-stu-id="e4a01-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e4a01-123">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e4a01-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a01-124">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4a01-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4a01-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4a01-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a01-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4a01-126">Return value</span></span>

<span data-ttu-id="e4a01-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4a01-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4a01-128">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4a01-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a01-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4a01-129">Remarks</span></span>

<span data-ttu-id="e4a01-130">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="e4a01-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e4a01-131">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="e4a01-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e4a01-132">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="e4a01-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a01-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a01-133">Requirements</span></span>



| <span data-ttu-id="e4a01-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a01-134">Requirement</span></span> | <span data-ttu-id="e4a01-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e4a01-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a01-136">Header</span><span class="sxs-lookup"><span data-stu-id="e4a01-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e4a01-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a01-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4a01-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4a01-138">Library</span></span><br/> | <dl> <span data-ttu-id="e4a01-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4a01-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4a01-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4a01-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a01-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4a01-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4a01-142">Vorausberechnungsübertragung der Radiance (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e4a01-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
