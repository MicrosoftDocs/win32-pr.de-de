---
description: D3DXSHEvalSphericalLight-Funktion (D3dx9math.h) – Wertet ein pherisches Licht aus und gibt SH-Daten (Pherical Imaging) zurück.
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: D3DXSHEvalSphericalLight-Funktion (D3dx9math.h)
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
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117888"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="25f77-103">D3DXSHEvalSphericalLight-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="25f77-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="25f77-104">Wertet ein pherisches Licht aus und gibt SH-Daten (PhericalIcalIcals) zurück.</span><span class="sxs-lookup"><span data-stu-id="25f77-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25f77-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="25f77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f77-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25f77-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25f77-109">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="25f77-109">Order of the SH evaluation.</span></span> <span data-ttu-id="25f77-110">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="25f77-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="25f77-111">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="25f77-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="25f77-112">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="25f77-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-113">*pPos* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="25f77-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="25f77-115">Zeiger auf die Lichtposition.</span><span class="sxs-lookup"><span data-stu-id="25f77-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-116">*Radius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25f77-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25f77-118">Radius der pherischen Glühbirnenquelle.</span><span class="sxs-lookup"><span data-stu-id="25f77-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-119">*RIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25f77-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25f77-121">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="25f77-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-122">*GIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25f77-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25f77-124">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="25f77-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-125">*BIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25f77-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25f77-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25f77-127">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="25f77-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-128">*pROut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25f77-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25f77-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25f77-130">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="25f77-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-131">*pGOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25f77-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-132">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25f77-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25f77-133">Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="25f77-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="25f77-134">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25f77-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25f77-135">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25f77-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25f77-136">Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="25f77-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f77-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25f77-137">Return value</span></span>

<span data-ttu-id="25f77-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25f77-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25f77-139">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25f77-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25f77-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="25f77-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f77-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25f77-141">Remarks</span></span>

<span data-ttu-id="25f77-142">Wertet ein sphärisches Licht aus und gibt unerklärliche SH-Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="25f77-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="25f77-143">Es gibt keine Normalisierung der Intensität des Lichts, wie es für [gerichtete Beleuchtungen](light-types.md)gibt. Daher muss beim Angeben der Intensitäten sorgfältig vorgegangen werden.</span><span class="sxs-lookup"><span data-stu-id="25f77-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="25f77-144">Dadurch werden drei Testbeispiele berechnet: *pROut* wird zurückgegeben, während *pGOut* und *pBOut* zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="25f77-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="25f77-145">Auf der Kugel mit Einheitenradius, wie in der folgenden Abbildung dargestellt, kann die Richtung einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben [werden.](coordinate-systems.md)</span><span class="sxs-lookup"><span data-stu-id="25f77-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="25f77-147">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und pherischen Koordinaten (Theta, phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="25f77-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="25f77-148">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.</span><span class="sxs-lookup"><span data-stu-id="25f77-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und pherischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="25f77-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f77-150">Requirements</span></span>



| <span data-ttu-id="25f77-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f77-151">Requirement</span></span> | <span data-ttu-id="25f77-152">Wert</span><span class="sxs-lookup"><span data-stu-id="25f77-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f77-153">Header</span><span class="sxs-lookup"><span data-stu-id="25f77-153">Header</span></span><br/>  | <dl> <span data-ttu-id="25f77-154"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="25f77-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="25f77-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25f77-155">Library</span></span><br/> | <dl> <span data-ttu-id="25f77-156"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="25f77-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25f77-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25f77-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f77-158">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="25f77-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="25f77-159">Vorausberechnungsübertragung der Radiance (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25f77-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
