---
description: 'D3DXSHEvalDirection-Funktion (D3dx9math.h): Wertet die SH-Basisfunktionen (Spherical Vector) aus einem Eingaberichtungsvektor aus.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: D3DXSHEvalDirection-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093961"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="e3e61-103">D3DXSHEvalDirection-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e3e61-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="e3e61-104">Wertet die SH-Basisfunktionen (Spherical Vector) aus einem Eingaberichtungsvektor aus.</span><span class="sxs-lookup"><span data-stu-id="e3e61-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3e61-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="e3e61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3e61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e61-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3e61-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e61-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3e61-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e3e61-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical veralten).</span><span class="sxs-lookup"><span data-stu-id="e3e61-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="e3e61-110">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e3e61-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e3e61-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e3e61-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e3e61-112">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e3e61-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e61-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3e61-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3e61-114">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="e3e61-114">Order of the SH evaluation.</span></span> <span data-ttu-id="e3e61-115">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="e3e61-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e3e61-116">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e3e61-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e3e61-117">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="e3e61-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e3e61-118">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e3e61-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e61-119">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3e61-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e3e61-120">(x, y, z) Richtungsvektor, in dem die SH-Basisfunktionen ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3e61-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="e3e61-121">Muss normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3e61-121">Must be normalized.</span></span> <span data-ttu-id="e3e61-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e3e61-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e61-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3e61-123">Return value</span></span>

<span data-ttu-id="e3e61-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3e61-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e3e61-125">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e3e61-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="e3e61-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e3e61-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3e61-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3e61-127">Remarks</span></span>

<span data-ttu-id="e3e61-128">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="e3e61-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e3e61-129">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="e3e61-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e3e61-130">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="e3e61-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="e3e61-131">Auf der Kugel mit Einheitenradius, wie in der folgenden Abbildung dargestellt, kann die Richtung einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben [werden.](coordinate-systems.md)</span><span class="sxs-lookup"><span data-stu-id="e3e61-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="e3e61-133">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und pherischen Koordinaten (Theta, phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="e3e61-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="e3e61-134">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.</span><span class="sxs-lookup"><span data-stu-id="e3e61-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und pherischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="e3e61-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3e61-136">Requirements</span></span>



| <span data-ttu-id="e3e61-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3e61-137">Requirement</span></span> | <span data-ttu-id="e3e61-138">Wert</span><span class="sxs-lookup"><span data-stu-id="e3e61-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e61-139">Header</span><span class="sxs-lookup"><span data-stu-id="e3e61-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e3e61-140"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e61-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3e61-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3e61-141">Library</span></span><br/> | <dl> <span data-ttu-id="e3e61-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3e61-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3e61-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e3e61-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e61-144">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e3e61-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e3e61-145">Vorausberechnungsübertragung der Radiance (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e3e61-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
