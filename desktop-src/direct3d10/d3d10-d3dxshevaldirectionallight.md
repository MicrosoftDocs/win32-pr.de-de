---
description: 'D3DXSHEvalDirectionalLight-Funktion (D3DX10.h): Wertet ein direktionales Licht aus und gibt SH-Daten zurück.'
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: D3DXSHEvalDirectionalLight-Funktion (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 551dad8081af2b0138be4758682d5a660f621141
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108598"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="5ca0f-103">D3DXSHEvalDirectionalLight-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="5ca0f-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="5ca0f-104">Wertet ein gerichtetes Licht aus und gibt sh-Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca0f-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5ca0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ca0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca0f-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ca0f-109">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-109">Order of the SH evaluation.</span></span> <span data-ttu-id="5ca0f-110">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5ca0f-111">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5ca0f-112">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="5ca0f-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-113">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ca0f-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ca0f-115">Zeiger auf den Achsenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="5ca0f-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-117">*RIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-118">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0f-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ca0f-119">Die rote Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-120">*GIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-121">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0f-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ca0f-122">Die grüne Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-123">*BIntensity* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ca0f-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ca0f-125">Die blaue Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-126">*pROut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ca0f-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5ca0f-128">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-129">*pGOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-130">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ca0f-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5ca0f-131">Optionaler Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="5ca0f-132">*pBOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ca0f-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca0f-133">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ca0f-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5ca0f-134">Optionaler Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca0f-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ca0f-135">Return value</span></span>

<span data-ttu-id="5ca0f-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ca0f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ca0f-137">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ca0f-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca0f-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ca0f-139">Remarks</span></span>

<span data-ttu-id="5ca0f-140">Der Ausgabevektor wird so berechnet, dass bei einem Intensitätsverhältnis von R/G/B gleich 1 die resultierende Beendigungsausgabe eines Punkts direkt unter dem Licht eines diffusen Objekts mit einem Albedo von 1 1,0 wäre.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="5ca0f-141">Dadurch werden drei Beispielbeispiele berechnet. pROut wird zurückgegeben, während pGOut und pBOut zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="5ca0f-142">Auf der Kugel mit Einheitenradius, wie in der folgenden Abbildung dargestellt, kann die Richtung einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und dem Winkel von z angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="5ca0f-144">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und pherischen Koordinaten (Theta, phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="5ca0f-145">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.</span><span class="sxs-lookup"><span data-stu-id="5ca0f-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="5ca0f-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ca0f-147">Requirements</span></span>



| <span data-ttu-id="5ca0f-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ca0f-148">Requirement</span></span> | <span data-ttu-id="5ca0f-149">Wert</span><span class="sxs-lookup"><span data-stu-id="5ca0f-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca0f-150">Header</span><span class="sxs-lookup"><span data-stu-id="5ca0f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="5ca0f-151"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca0f-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ca0f-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ca0f-152">Library</span></span><br/> | <dl> <span data-ttu-id="5ca0f-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ca0f-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca0f-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ca0f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca0f-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ca0f-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
