---
description: Wertet ein kugelförmiges Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: D3DXSHEvalSphericalLight-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c658480a08360fe8489cfc86319a689e828c0a1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355586"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="2ecab-103">D3DXSHEvalSphericalLight-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="2ecab-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="2ecab-104">Wertet ein kugelförmiges Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück</span><span class="sxs-lookup"><span data-stu-id="2ecab-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ecab-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="2ecab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ecab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecab-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ecab-109">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="2ecab-109">Order of the SH evaluation.</span></span> <span data-ttu-id="2ecab-110">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="2ecab-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2ecab-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="2ecab-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2ecab-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="2ecab-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-113">*PPOs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ecab-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2ecab-115">Zeiger auf die Lichtposition.</span><span class="sxs-lookup"><span data-stu-id="2ecab-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-116">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ecab-118">Radius der kugelförmigen Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="2ecab-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-119">*Rintensität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ecab-121">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2ecab-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-122">*Gintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ecab-124">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2ecab-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-125">*Bintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ecab-127">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2ecab-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-128">*Proxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-129">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ecab-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2ecab-130">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="2ecab-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-131">*pgout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-132">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ecab-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2ecab-133">Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="2ecab-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="2ecab-134">*pbout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecab-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecab-135">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ecab-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2ecab-136">Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="2ecab-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecab-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ecab-137">Return value</span></span>

<span data-ttu-id="2ecab-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ecab-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ecab-139">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ecab-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ecab-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="2ecab-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecab-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ecab-141">Remarks</span></span>

<span data-ttu-id="2ecab-142">Wertet ein kugelförmiges Licht aus und gibt die Daten der Daten im Daten</span><span class="sxs-lookup"><span data-stu-id="2ecab-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="2ecab-143">Es gibt keine Normalisierung der Intensität des Lichts, wie es bei direktionalen Lichtern der Fall ist, daher muss beim Angeben der Intensitäten sorgfältig vorgegangen werden.</span><span class="sxs-lookup"><span data-stu-id="2ecab-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="2ecab-144">Dadurch werden drei Spektral Beispiele berechnet. "Prout" wird zurückgegeben, während "pgout" und "pbout" zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="2ecab-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="2ecab-145">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der rechten Hand Richtung und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="2ecab-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="2ecab-147">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="2ecab-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="2ecab-148">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="2ecab-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="2ecab-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ecab-150">Requirements</span></span>



| <span data-ttu-id="2ecab-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ecab-151">Requirement</span></span> | <span data-ttu-id="2ecab-152">Wert</span><span class="sxs-lookup"><span data-stu-id="2ecab-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecab-153">Header</span><span class="sxs-lookup"><span data-stu-id="2ecab-153">Header</span></span><br/>  | <dl> <span data-ttu-id="2ecab-154"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecab-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ecab-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ecab-155">Library</span></span><br/> | <dl> <span data-ttu-id="2ecab-156"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ecab-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecab-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ecab-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecab-158">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2ecab-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
