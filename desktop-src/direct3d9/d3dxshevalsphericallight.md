---
description: Wertet ein kugelförmiges Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: D3DXSHEvalSphericalLight-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8581b4284e270b6df587be1a71fcf11f29c843d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354617"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="390a8-103">D3DXSHEvalSphericalLight-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="390a8-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="390a8-104">Wertet ein kugelförmiges Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück</span><span class="sxs-lookup"><span data-stu-id="390a8-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="390a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="390a8-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="390a8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="390a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390a8-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="390a8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="390a8-109">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="390a8-109">Order of the SH evaluation.</span></span> <span data-ttu-id="390a8-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="390a8-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="390a8-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="390a8-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="390a8-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="390a8-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-113">*PPOs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="390a8-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="390a8-115">Zeiger auf die Lichtposition.</span><span class="sxs-lookup"><span data-stu-id="390a8-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-116">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="390a8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="390a8-118">Radius der kugelförmigen Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="390a8-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-119">*Rintensität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="390a8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="390a8-121">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="390a8-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-122">*Gintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="390a8-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="390a8-124">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="390a8-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-125">*Bintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="390a8-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="390a8-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="390a8-127">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="390a8-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-128">*Proxy* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="390a8-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-129">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="390a8-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="390a8-130">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="390a8-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-131">*pgout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="390a8-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-132">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="390a8-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="390a8-133">Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="390a8-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="390a8-134">*pbout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="390a8-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390a8-135">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="390a8-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="390a8-136">Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="390a8-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390a8-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="390a8-137">Return value</span></span>

<span data-ttu-id="390a8-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="390a8-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="390a8-139">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="390a8-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="390a8-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="390a8-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="390a8-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="390a8-141">Remarks</span></span>

<span data-ttu-id="390a8-142">Wertet ein kugelförmiges Licht aus und gibt die Daten der Daten im Daten</span><span class="sxs-lookup"><span data-stu-id="390a8-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="390a8-143">Es gibt keine Normalisierung der Intensität des Lichts, wie es bei [direktionalen Lichtern](light-types.md)der Fall ist, daher muss beim Angeben der Intensitäten sorgfältig vorgegangen werden.</span><span class="sxs-lookup"><span data-stu-id="390a8-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="390a8-144">Dadurch werden drei Spektral Beispiele berechnet. " *Prout* " wird zurückgegeben, während " *pgout* " und " *pbout* " zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="390a8-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="390a8-145">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der [rechten Hand Richtung](coordinate-systems.md)und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="390a8-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="390a8-147">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="390a8-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="390a8-148">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="390a8-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="390a8-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="390a8-150">Requirements</span></span>



| <span data-ttu-id="390a8-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="390a8-151">Requirement</span></span> | <span data-ttu-id="390a8-152">Wert</span><span class="sxs-lookup"><span data-stu-id="390a8-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="390a8-153">Header</span><span class="sxs-lookup"><span data-stu-id="390a8-153">Header</span></span><br/>  | <dl> <span data-ttu-id="390a8-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="390a8-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="390a8-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="390a8-155">Library</span></span><br/> | <dl> <span data-ttu-id="390a8-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="390a8-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="390a8-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="390a8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390a8-158">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="390a8-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="390a8-159">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="390a8-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
