---
description: Wertet ein Licht aus, das eine lineare interpolung zwischen zwei Farben über der Kugel ist.
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: D3DXSHEvalHemisphereLight-Funktion (D3dx9math. h)
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
ms.openlocfilehash: bdb94fc10ddadc7048f7bb911df089d6f84b0829
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104560426"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="eebd9-103">D3DXSHEvalHemisphereLight-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eebd9-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="eebd9-104">Wertet ein Licht aus, das eine lineare interpolung zwischen zwei Farben über der Kugel ist.</span><span class="sxs-lookup"><span data-stu-id="eebd9-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebd9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebd9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="eebd9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eebd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebd9-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eebd9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eebd9-109">Reihenfolge der Auswertung der sphärischen Harmonika (SH).</span><span class="sxs-lookup"><span data-stu-id="eebd9-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="eebd9-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="eebd9-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="eebd9-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="eebd9-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="eebd9-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="eebd9-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-113">*pdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eebd9-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eebd9-115">Ein Zeiger auf den Achsen Richtungsvektor (x, y, z), in dem die sh-Basisfunktionen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="eebd9-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="eebd9-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="eebd9-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-117">Nach *oben* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-118">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="eebd9-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="eebd9-119">Die Farbe des Himmels.</span><span class="sxs-lookup"><span data-stu-id="eebd9-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-120">*Unten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="eebd9-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="eebd9-122">Die Grundfarbe.</span><span class="sxs-lookup"><span data-stu-id="eebd9-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-123">*Proxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-124">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eebd9-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eebd9-125">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="eebd9-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-126">*pgout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eebd9-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eebd9-128">Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="eebd9-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="eebd9-129">*pbout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eebd9-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd9-130">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eebd9-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eebd9-131">Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="eebd9-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebd9-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eebd9-132">Return value</span></span>

<span data-ttu-id="eebd9-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eebd9-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eebd9-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eebd9-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eebd9-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="eebd9-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebd9-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eebd9-136">Remarks</span></span>

<span data-ttu-id="eebd9-137">Die interpolung erfolgt linear zwischen den beiden Punkten, nicht über der Oberfläche der Kugel (d. h., wenn die Achse (0, 0, 1) ist, ist sie linear in Z, nicht im azimutalwinkel).</span><span class="sxs-lookup"><span data-stu-id="eebd9-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="eebd9-138">Die sich ergebende kugelförmige Beleuchtungsfunktion wird normalisiert, sodass ein Punkt auf einer perfekt diffusen Oberfläche ohne shadowingund eine normale, in der Richtung " *pdir* " gezeigt wird, zu einem Ausgangs Glanz mit einem Wert von "1" führt (wenn die obere Farbe weiß und die untere Farbe schwarz war).</span><span class="sxs-lookup"><span data-stu-id="eebd9-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="eebd9-139">Dabei handelt es sich um ein sehr einfaches Modell, bei dem *Top* die Intensität des "Himmels" darstellt und " *Bottom* " die Intensität des "Boden" darstellt.</span><span class="sxs-lookup"><span data-stu-id="eebd9-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="eebd9-140">In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der [rechten Hand Richtung](coordinate-systems.md)und dem Phi, dem Winkel von z.</span><span class="sxs-lookup"><span data-stu-id="eebd9-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

<span data-ttu-id="eebd9-142">Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="eebd9-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="eebd9-143">Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="eebd9-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="eebd9-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eebd9-145">Requirements</span></span>



| <span data-ttu-id="eebd9-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eebd9-146">Requirement</span></span> | <span data-ttu-id="eebd9-147">Wert</span><span class="sxs-lookup"><span data-stu-id="eebd9-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eebd9-148">Header</span><span class="sxs-lookup"><span data-stu-id="eebd9-148">Header</span></span><br/>  | <dl> <span data-ttu-id="eebd9-149"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eebd9-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eebd9-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eebd9-150">Library</span></span><br/> | <dl> <span data-ttu-id="eebd9-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eebd9-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eebd9-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eebd9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebd9-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="eebd9-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eebd9-154">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="eebd9-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
