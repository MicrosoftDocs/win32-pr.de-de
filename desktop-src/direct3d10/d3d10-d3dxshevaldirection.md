---
description: D3DXSHEvalDirection-Funktion (D3DX10.h) – Wertet die SH-Basisfunktionen (SphericalIcals) aus einem Eingaberichtungsvektor aus.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: D3DXSHEvalDirection-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7fa1f94d65ca8096a0398d71ca2f562b643d47a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108588"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="77d0d-103">D3DXSHEvalDirection-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="77d0d-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="77d0d-104">Wertet die SH-Basisfunktionen (PhericalIcal) aus einem Eingaberichtungsvektor aus.</span><span class="sxs-lookup"><span data-stu-id="77d0d-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d0d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="77d0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d0d-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="77d0d-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d0d-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="77d0d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="77d0d-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical- oder Pherical-Rumpf).</span><span class="sxs-lookup"><span data-stu-id="77d0d-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="77d0d-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="77d0d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="77d0d-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="77d0d-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="77d0d-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="77d0d-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d0d-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77d0d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77d0d-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="77d0d-114">Order of the SH evaluation.</span></span> <span data-ttu-id="77d0d-115">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="77d0d-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="77d0d-116">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="77d0d-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="77d0d-117">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="77d0d-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="77d0d-118">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="77d0d-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d0d-119">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="77d0d-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="77d0d-120">(x, y, z) Richtungsvektor, in dem die SH-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="77d0d-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="77d0d-121">Muss normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="77d0d-121">Must be normalized.</span></span> <span data-ttu-id="77d0d-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="77d0d-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d0d-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77d0d-123">Return value</span></span>

<span data-ttu-id="77d0d-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="77d0d-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="77d0d-125">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="77d0d-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="77d0d-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="77d0d-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d0d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77d0d-127">Remarks</span></span>

<span data-ttu-id="77d0d-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="77d0d-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="77d0d-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="77d0d-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="77d0d-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="77d0d-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="77d0d-131">Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77d0d-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="77d0d-133">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="77d0d-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="77d0d-134">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis Pi variiert.</span><span class="sxs-lookup"><span data-stu-id="77d0d-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="77d0d-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77d0d-136">Requirements</span></span>



| <span data-ttu-id="77d0d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77d0d-137">Requirement</span></span> | <span data-ttu-id="77d0d-138">Wert</span><span class="sxs-lookup"><span data-stu-id="77d0d-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77d0d-139">Header</span><span class="sxs-lookup"><span data-stu-id="77d0d-139">Header</span></span><br/>  | <dl> <span data-ttu-id="77d0d-140"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="77d0d-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="77d0d-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77d0d-141">Library</span></span><br/> | <dl> <span data-ttu-id="77d0d-142"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="77d0d-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d0d-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="77d0d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d0d-144">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="77d0d-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
