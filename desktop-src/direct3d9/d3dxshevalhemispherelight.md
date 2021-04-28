---
description: 'D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h): Wertet ein Licht aus, das eine lineare Interpolation zwischen zwei Farben über der Kugel ist.'
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093965"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="fdb47-103">D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fdb47-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="fdb47-104">Wertet ein Licht aus, das eine lineare Interpolation zwischen zwei Farben über der Kugel ist.</span><span class="sxs-lookup"><span data-stu-id="fdb47-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdb47-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="fdb47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdb47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb47-107">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb47-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb47-109">Die Reihenfolge der SH-Auswertung (SphericalLips).</span><span class="sxs-lookup"><span data-stu-id="fdb47-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="fdb47-110">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="fdb47-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fdb47-111">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="fdb47-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fdb47-112">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="fdb47-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-113">*pDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdb47-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fdb47-115">Zeiger auf den Hemisphärenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fdb47-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="fdb47-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fdb47-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-117">*Top* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-118">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb47-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="fdb47-119">Die Sky-Farbe.</span><span class="sxs-lookup"><span data-stu-id="fdb47-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-120">*Unten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb47-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="fdb47-122">Die Bodenfarbe.</span><span class="sxs-lookup"><span data-stu-id="fdb47-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-123">*pROut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb47-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb47-125">Zeiger auf den SH-Ausgabevektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="fdb47-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-126">*pGOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb47-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb47-128">Zeiger auf den SH-Ausgabevektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="fdb47-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="fdb47-129">*pBOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fdb47-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb47-130">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb47-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb47-131">Zeiger auf den SH-Ausgabevektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="fdb47-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb47-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdb47-132">Return value</span></span>

<span data-ttu-id="fdb47-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fdb47-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fdb47-134">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fdb47-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fdb47-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="fdb47-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb47-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdb47-136">Remarks</span></span>

<span data-ttu-id="fdb47-137">Die Interpolation erfolgt linear zwischen den beiden Punkten, nicht über der Oberfläche der Kugel (d. h., wenn die Achse (0,0,1) war, ist sie linear in Z, nicht im winkelförmigen Winkel.</span><span class="sxs-lookup"><span data-stu-id="fdb47-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="fdb47-138">Die resultierende pherische Beleuchtungsfunktion wird normalisiert, sodass ein Punkt auf einer perfekt diffusen Oberfläche ohne Schatten und ein normaler Punkt, der in die Richtung *pDir* zeigt, zu einer Beendigungsfläche mit dem Wert 1 führen würde (wenn die obere Farbe weiß und die untere Farbe schwarz ist).</span><span class="sxs-lookup"><span data-stu-id="fdb47-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="fdb47-139">Dies ist ein sehr einfaches Modell, bei dem *Top* die Intensität des "Sky" und *Bottom* die Intensität des "Bodens" darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdb47-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="fdb47-140">Auf der Kugel mit Einheitenradius, wie in der folgenden Abbildung dargestellt, kann die Richtung einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben [werden.](coordinate-systems.md)</span><span class="sxs-lookup"><span data-stu-id="fdb47-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

<span data-ttu-id="fdb47-142">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und pherischen Koordinaten (Theta, phi) auf der Einheitenkugel.</span><span class="sxs-lookup"><span data-stu-id="fdb47-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="fdb47-143">Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.</span><span class="sxs-lookup"><span data-stu-id="fdb47-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und pherischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="fdb47-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdb47-145">Requirements</span></span>



| <span data-ttu-id="fdb47-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdb47-146">Requirement</span></span> | <span data-ttu-id="fdb47-147">Wert</span><span class="sxs-lookup"><span data-stu-id="fdb47-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb47-148">Header</span><span class="sxs-lookup"><span data-stu-id="fdb47-148">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb47-149"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb47-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb47-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fdb47-150">Library</span></span><br/> | <dl> <span data-ttu-id="fdb47-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb47-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdb47-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fdb47-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb47-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="fdb47-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fdb47-154">Vorausberechnen der Übertragungsstärke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fdb47-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
