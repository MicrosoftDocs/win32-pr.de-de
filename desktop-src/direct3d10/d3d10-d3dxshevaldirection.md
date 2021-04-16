---
description: Wertet die sphärischen harmonischen (SH)-Basisfunktionen aus einem Eingabe Richtungsvektor aus.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: D3DXSHEvalDirection-Funktion (d3dx10. h)
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
ms.openlocfilehash: 698873f3278b37970120b03c25918096762ead34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104551487"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="10582-103">D3DXSHEvalDirection-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="10582-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="10582-104">Wertet die sphärischen harmonischen (SH)-Basisfunktionen aus einem Eingabe Richtungsvektor aus.</span><span class="sxs-lookup"><span data-stu-id="10582-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="10582-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10582-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="10582-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10582-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10582-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10582-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="10582-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="10582-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="10582-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="10582-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="10582-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="10582-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="10582-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="10582-112">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10582-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10582-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10582-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10582-114">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="10582-114">Order of the SH evaluation.</span></span> <span data-ttu-id="10582-115">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="10582-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="10582-116">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="10582-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="10582-117">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="10582-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="10582-118">*pdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10582-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10582-119">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="10582-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="10582-120">(x, y, z) Richtung Vektor, in dem die sh-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="10582-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="10582-121">Muss normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="10582-121">Must be normalized.</span></span> <span data-ttu-id="10582-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="10582-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10582-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10582-123">Return value</span></span>

<span data-ttu-id="10582-124">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="10582-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="10582-125">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="10582-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="10582-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="10582-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="10582-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10582-127">Remarks</span></span>

<span data-ttu-id="10582-128">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="10582-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="10582-129">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="10582-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="10582-130">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="10582-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="10582-131">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der rechten Hand Richtung und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="10582-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="10582-133">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="10582-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="10582-134">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="10582-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="10582-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10582-136">Requirements</span></span>



| <span data-ttu-id="10582-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10582-137">Requirement</span></span> | <span data-ttu-id="10582-138">Wert</span><span class="sxs-lookup"><span data-stu-id="10582-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10582-139">Header</span><span class="sxs-lookup"><span data-stu-id="10582-139">Header</span></span><br/>  | <dl> <span data-ttu-id="10582-140"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="10582-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="10582-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10582-141">Library</span></span><br/> | <dl> <span data-ttu-id="10582-142"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10582-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10582-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10582-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10582-144">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="10582-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
