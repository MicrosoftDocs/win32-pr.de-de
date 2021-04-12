---
description: Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt.
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: D3DXSHEvalConeLight-Funktion (d3dx10. h)
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
ms.openlocfilehash: 97bd700d1c38441db6c5e68554cf038d9081efaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219650"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="3ec83-103">D3DXSHEvalConeLight-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="3ec83-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="3ec83-104">Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt.</span><span class="sxs-lookup"><span data-stu-id="3ec83-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ec83-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3ec83-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ec83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec83-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ec83-109">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="3ec83-109">Order of the SH evaluation.</span></span> <span data-ttu-id="3ec83-110">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="3ec83-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3ec83-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="3ec83-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3ec83-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="3ec83-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-113">*pdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3ec83-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3ec83-115">Ein Zeiger auf den Achsen Richtungsvektor (x, y, z), in dem die sh-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="3ec83-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="3ec83-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3ec83-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-117">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ec83-119">Der Radius des Kegel im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="3ec83-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-120">*Rintensität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-121">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ec83-122">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="3ec83-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-123">*Gintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ec83-125">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="3ec83-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-126">*Bintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-127">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ec83-128">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="3ec83-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-129">*Proxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-130">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ec83-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ec83-131">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="3ec83-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-132">*pgout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-133">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ec83-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ec83-134">Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="3ec83-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="3ec83-135">*pbout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec83-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec83-136">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ec83-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ec83-137">Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="3ec83-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec83-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ec83-138">Return value</span></span>

<span data-ttu-id="3ec83-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ec83-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ec83-140">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ec83-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ec83-141">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="3ec83-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ec83-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ec83-142">Remarks</span></span>

<span data-ttu-id="3ec83-143">Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt</span><span class="sxs-lookup"><span data-stu-id="3ec83-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="3ec83-144">Der Ausgabe Vektor wird berechnet, sodass die Ausgangs Kraft eines Punkts, der sich direkt unterhalb des Lichts (in der Kegel Richtung eines diffuses Objekts mit einem Albedo-Wert von 1) befindet, 1,0 ist, wenn das Intensität-Verhältnis von R/G/B gleich 1 ist.</span><span class="sxs-lookup"><span data-stu-id="3ec83-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="3ec83-145">Dadurch werden drei Spektral Beispiele berechnet. "Prout" wird zurückgegeben, während "pgout" und "pbout" zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3ec83-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="3ec83-146">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der rechten Hand Richtung und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="3ec83-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="3ec83-148">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="3ec83-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="3ec83-149">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="3ec83-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="3ec83-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ec83-151">Requirements</span></span>



| <span data-ttu-id="3ec83-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ec83-152">Requirement</span></span> | <span data-ttu-id="3ec83-153">Wert</span><span class="sxs-lookup"><span data-stu-id="3ec83-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec83-154">Header</span><span class="sxs-lookup"><span data-stu-id="3ec83-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3ec83-155"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec83-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ec83-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ec83-156">Library</span></span><br/> | <dl> <span data-ttu-id="3ec83-157"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ec83-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec83-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec83-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec83-159">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3ec83-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
