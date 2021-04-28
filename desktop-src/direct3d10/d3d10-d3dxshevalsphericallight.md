---
description: D3DXSHEvalSphericalLight-Funktion (D3DX10.h) – Wertet ein sphärisches Licht aus und gibt shherische (Spherical)-Daten zurück.
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: D3DXSHEvalSphericalLight-Funktion (D3DX10.h)
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
ms.openlocfilehash: e1e509ea4695f143bd5399cbda004bcba53f514c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108558"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="2cd56-103">D3DXSHEvalSphericalLight-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2cd56-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="2cd56-104">Wertet ein sphärisches Licht aus und gibt sh-Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="2cd56-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cd56-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2cd56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cd56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd56-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cd56-109">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="2cd56-109">Order of the SH evaluation.</span></span> <span data-ttu-id="2cd56-110">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="2cd56-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2cd56-111">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="2cd56-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2cd56-112">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="2cd56-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-113">*pPos* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cd56-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2cd56-115">Zeiger auf die helle Position.</span><span class="sxs-lookup"><span data-stu-id="2cd56-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-116">*Radius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cd56-118">Radius der sphärischen Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="2cd56-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-119">*RIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cd56-121">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2cd56-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-122">*GIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cd56-124">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2cd56-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-125">*BIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cd56-127">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="2cd56-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-128">*pROut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cd56-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cd56-130">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="2cd56-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-131">*pGOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-132">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cd56-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cd56-133">Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="2cd56-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-134">*pBOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-135">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cd56-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cd56-136">Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="2cd56-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd56-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cd56-137">Return value</span></span>

<span data-ttu-id="2cd56-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2cd56-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2cd56-139">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2cd56-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2cd56-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="2cd56-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd56-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cd56-141">Remarks</span></span>

<span data-ttu-id="2cd56-142">Wertet ein pherisches Licht aus und gibt sh-Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="2cd56-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="2cd56-143">Es gibt keine Normalisierung der Intensität des Lichts wie bei direktionalen Licht, daher muss bei der Angabe der Intensitäten vorsichtssam vorgesamst werden.</span><span class="sxs-lookup"><span data-stu-id="2cd56-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="2cd56-144">Dadurch werden drei Beispielbeispiele berechnet. pROut wird zurückgegeben, während pGOut und pBOut zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="2cd56-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="2cd56-145">Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2cd56-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="2cd56-147">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="2cd56-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="2cd56-148">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis Pi variiert.</span><span class="sxs-lookup"><span data-stu-id="2cd56-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="2cd56-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cd56-150">Requirements</span></span>



| <span data-ttu-id="2cd56-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cd56-151">Requirement</span></span> | <span data-ttu-id="2cd56-152">Wert</span><span class="sxs-lookup"><span data-stu-id="2cd56-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd56-153">Header</span><span class="sxs-lookup"><span data-stu-id="2cd56-153">Header</span></span><br/>  | <dl> <span data-ttu-id="2cd56-154"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd56-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cd56-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cd56-155">Library</span></span><br/> | <dl> <span data-ttu-id="2cd56-156"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cd56-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd56-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2cd56-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd56-158">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2cd56-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
