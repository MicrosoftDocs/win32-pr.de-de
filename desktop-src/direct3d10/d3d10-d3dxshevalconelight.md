---
description: 'D3DXSHEvalConeLight-Funktion (D3DX10.h): Wertet ein Licht aus, das ein Kegel mit konstanter Intensität ist, und gibt SH-Daten (Pherical Imaging) zurück.'
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: D3DXSHEvalConeLight-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108608"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="2532d-103">D3DXSHEvalConeLight-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2532d-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="2532d-104">Wertet ein Licht aus, das ein Kegel mit konstanter Intensität ist, und gibt SH-Daten (Pherical Imaging) zurück.</span><span class="sxs-lookup"><span data-stu-id="2532d-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2532d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2532d-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="2532d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2532d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2532d-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2532d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2532d-109">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="2532d-109">Order of the SH evaluation.</span></span> <span data-ttu-id="2532d-110">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="2532d-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2532d-111">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="2532d-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2532d-112">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="2532d-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-113">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2532d-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2532d-115">Zeiger auf den Hemi-Achsenrichtungsrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="2532d-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="2532d-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2532d-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-117">*Radius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-118">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2532d-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2532d-119">Radius des Kegels im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="2532d-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-120">*RIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-121">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2532d-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2532d-122">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2532d-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-123">*GIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2532d-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2532d-125">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2532d-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-126">*BIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2532d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2532d-128">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2532d-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-129">*pROut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-130">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2532d-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2532d-131">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="2532d-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-132">*pGOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-133">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2532d-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2532d-134">Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="2532d-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="2532d-135">*pBOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2532d-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532d-136">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2532d-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2532d-137">Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="2532d-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2532d-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2532d-138">Return value</span></span>

<span data-ttu-id="2532d-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2532d-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2532d-140">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2532d-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2532d-141">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="2532d-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2532d-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2532d-142">Remarks</span></span>

<span data-ttu-id="2532d-143">Wertet ein Licht aus, das ein Kegel mit konstanter Intensität ist und sh-Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2532d-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="2532d-144">Der Ausgabevektor wird so berechnet, dass, wenn das Intensitätsverhältnis R/G/B gleich 1 ist, die Beendigungsausgabe eines Punkts direkt unter dem Licht (ausgerichtet in der Kegelrichtung bei einem diffusen Objekt mit einem Albedo von 1) 1,0 wäre.</span><span class="sxs-lookup"><span data-stu-id="2532d-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="2532d-145">Dadurch werden drei Beispielbeispiele berechnet. pROut wird zurückgegeben, während pGOut und pBOut zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="2532d-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="2532d-146">Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2532d-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="2532d-148">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="2532d-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="2532d-149">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis Pi variiert.</span><span class="sxs-lookup"><span data-stu-id="2532d-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="2532d-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2532d-151">Requirements</span></span>



| <span data-ttu-id="2532d-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2532d-152">Requirement</span></span> | <span data-ttu-id="2532d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="2532d-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2532d-154">Header</span><span class="sxs-lookup"><span data-stu-id="2532d-154">Header</span></span><br/>  | <dl> <span data-ttu-id="2532d-155"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2532d-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2532d-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2532d-156">Library</span></span><br/> | <dl> <span data-ttu-id="2532d-157"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2532d-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2532d-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2532d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2532d-159">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2532d-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
