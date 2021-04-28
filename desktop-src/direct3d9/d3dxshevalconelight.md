---
description: 'D3DXSHEvalConeLight-Funktion (D3dx9math.h): Wertet ein Licht aus, das ein Kegel konstanter Intensität ist, und gibt shherische (Spherical Sply)-Daten zurück.'
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: D3DXSHEvalConeLight-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31c90e705a0bb4e82813fff42673e143c5acf171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117948"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a><span data-ttu-id="fe018-103">D3DXSHEvalConeLight-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fe018-103">D3DXSHEvalConeLight function (D3dx9math.h)</span></span>

<span data-ttu-id="fe018-104">Wertet ein Licht aus, das ein Kegel konstanter Intensität ist, und gibt SH-Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="fe018-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe018-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe018-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="fe018-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe018-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe018-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe018-109">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="fe018-109">Order of the SH evaluation.</span></span> <span data-ttu-id="fe018-110">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="fe018-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fe018-111">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="fe018-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fe018-112">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="fe018-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-113">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe018-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe018-115">Zeiger auf den Achsenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe018-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="fe018-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fe018-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-117">*Radius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-118">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe018-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe018-119">Kegelradius im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="fe018-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-120">*RIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-121">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe018-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe018-122">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="fe018-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-123">*GIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe018-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe018-125">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="fe018-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-126">*BIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe018-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe018-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe018-128">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="fe018-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-129">*pROut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe018-129">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-130">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe018-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fe018-131">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="fe018-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-132">*pGOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe018-132">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-133">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe018-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fe018-134">Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="fe018-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="fe018-135">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe018-135">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe018-136">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe018-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fe018-137">Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="fe018-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe018-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe018-138">Return value</span></span>

<span data-ttu-id="fe018-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe018-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe018-140">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe018-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe018-141">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="fe018-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe018-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe018-142">Remarks</span></span>

<span data-ttu-id="fe018-143">Wertet ein Licht aus, das ein Kegel mit konstanter Intensität ist und sh-Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe018-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="fe018-144">Der Ausgabevektor wird so berechnet, dass, wenn das Intensitätsverhältnis R/G/B gleich 1 ist, die Beendigungsausgabe eines Punkts direkt unter dem Licht (ausgerichtet in der Kegelrichtung bei einem diffusen Objekt mit einem Albedo von 1) 1,0 wäre.</span><span class="sxs-lookup"><span data-stu-id="fe018-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="fe018-145">Dadurch werden drei Beispielbeispiele berechnet: *pROut* wird zurückgegeben, während *pGOut* und *pBOut* zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="fe018-145">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="fe018-146">Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die [Z-Achse in rechtshändiger Richtung](coordinate-systems.md)und phi, dem Winkel von z, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fe018-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="fe018-148">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="fe018-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="fe018-149">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis Pi variiert.</span><span class="sxs-lookup"><span data-stu-id="fe018-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="fe018-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe018-151">Requirements</span></span>



| <span data-ttu-id="fe018-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe018-152">Requirement</span></span> | <span data-ttu-id="fe018-153">Wert</span><span class="sxs-lookup"><span data-stu-id="fe018-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe018-154">Header</span><span class="sxs-lookup"><span data-stu-id="fe018-154">Header</span></span><br/>  | <dl> <span data-ttu-id="fe018-155"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe018-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe018-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe018-156">Library</span></span><br/> | <dl> <span data-ttu-id="fe018-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe018-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe018-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe018-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe018-159">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe018-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fe018-160">Vorausberechnen der Übertragungsstärke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fe018-160">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
