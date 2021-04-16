---
description: Dreht den sphärischen harmonischen Vektor (SH) in der z-Achse um den angegebenen Winkel.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: D3DXSHRotateZ-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394117"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="96737-103">D3DXSHRotateZ-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="96737-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="96737-104">Dreht den sphärischen harmonischen Vektor (SH) in der z-Achse um den angegebenen Winkel.</span><span class="sxs-lookup"><span data-stu-id="96737-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="96737-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96737-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="96737-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96737-107">*Pout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="96737-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96737-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="96737-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96737-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="96737-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="96737-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="96737-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="96737-111">Dieser Zeiger sollte nicht mit *pIn* Alias sein.</span><span class="sxs-lookup"><span data-stu-id="96737-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="96737-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="96737-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="96737-113">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96737-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96737-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96737-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96737-115">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="96737-115">Order of the SH evaluation.</span></span> <span data-ttu-id="96737-116">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="96737-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="96737-117">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="96737-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="96737-118">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="96737-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="96737-119">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96737-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96737-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96737-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96737-121">Drehwinkel im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="96737-121">Rotation angle in radians.</span></span> <span data-ttu-id="96737-122">Die Drehung wird um die z-Achse durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="96737-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="96737-123">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96737-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96737-124">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96737-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96737-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="96737-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96737-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96737-126">Return value</span></span>

<span data-ttu-id="96737-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="96737-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96737-128">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="96737-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="96737-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96737-129">Remarks</span></span>

<span data-ttu-id="96737-130">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="96737-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="96737-131">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="96737-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="96737-132">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="96737-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="96737-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96737-133">Requirements</span></span>



| <span data-ttu-id="96737-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96737-134">Requirement</span></span> | <span data-ttu-id="96737-135">Wert</span><span class="sxs-lookup"><span data-stu-id="96737-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96737-136">Header</span><span class="sxs-lookup"><span data-stu-id="96737-136">Header</span></span><br/>  | <dl> <span data-ttu-id="96737-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="96737-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="96737-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96737-138">Library</span></span><br/> | <dl> <span data-ttu-id="96737-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96737-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96737-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96737-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96737-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="96737-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="96737-142">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="96737-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
