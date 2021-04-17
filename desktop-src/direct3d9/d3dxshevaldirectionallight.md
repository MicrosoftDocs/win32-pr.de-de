---
description: Wertet ein Direktionales Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: D3DXSHEvalDirectionalLight-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c78ee4059ed83b97e7ac1f392f857351df48ee7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104567885"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="cdf14-103">D3DXSHEvalDirectionalLight-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cdf14-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="cdf14-104">Wertet ein [Direktionales Licht](light-types.md) aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück</span><span class="sxs-lookup"><span data-stu-id="cdf14-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdf14-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="cdf14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdf14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf14-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdf14-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdf14-109">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="cdf14-109">Order of the SH evaluation.</span></span> <span data-ttu-id="cdf14-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="cdf14-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="cdf14-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="cdf14-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="cdf14-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="cdf14-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-113">*pdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdf14-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdf14-115">Ein Zeiger auf den Achsen Richtungsvektor (x, y, z), in dem die sh-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="cdf14-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="cdf14-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="cdf14-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-117">*Rintensität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdf14-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdf14-119">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="cdf14-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-120">*Gintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-121">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdf14-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdf14-122">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="cdf14-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-123">*Bintensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdf14-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdf14-125">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="cdf14-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-126">*Proxy* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdf14-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdf14-128">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="cdf14-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-129">*pgout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-130">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdf14-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdf14-131">Optionaler Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="cdf14-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="cdf14-132">*pbout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdf14-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf14-133">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdf14-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdf14-134">Optionaler Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="cdf14-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf14-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdf14-135">Return value</span></span>

<span data-ttu-id="cdf14-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdf14-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdf14-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdf14-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdf14-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="cdf14-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf14-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdf14-139">Remarks</span></span>

<span data-ttu-id="cdf14-140">Der Ausgabe Vektor wird berechnet, sodass die resultierende Ausgangs Glanz eines Punkts, der sich auf ein diffuses Objekt mit einem Albedo von 1 direkt unter dem Licht für ein diffuses Objekt mit dem Wert 1 ergibt, 1,0 ist, wenn das Intensität-Verhältnis von R/G/B 1 beträgt.</span><span class="sxs-lookup"><span data-stu-id="cdf14-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="cdf14-141">Dadurch werden drei Spektral Beispiele berechnet. " *Prout* " wird zurückgegeben, während " *pgout* " und " *pbout* " zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cdf14-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="cdf14-142">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der [rechten Hand Richtung](coordinate-systems.md)und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="cdf14-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="cdf14-144">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="cdf14-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="cdf14-145">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="cdf14-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="cdf14-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdf14-147">Requirements</span></span>



| <span data-ttu-id="cdf14-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdf14-148">Requirement</span></span> | <span data-ttu-id="cdf14-149">Wert</span><span class="sxs-lookup"><span data-stu-id="cdf14-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf14-150">Header</span><span class="sxs-lookup"><span data-stu-id="cdf14-150">Header</span></span><br/>  | <dl> <span data-ttu-id="cdf14-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdf14-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cdf14-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdf14-152">Library</span></span><br/> | <dl> <span data-ttu-id="cdf14-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdf14-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cdf14-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdf14-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf14-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cdf14-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="cdf14-156">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cdf14-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
