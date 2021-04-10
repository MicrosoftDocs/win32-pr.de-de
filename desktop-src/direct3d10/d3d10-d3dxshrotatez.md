---
description: Dreht den sphärischen harmonischen Vektor (SH) in der z-Achse um den angegebenen Winkel.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: D3DXSHRotateZ-Funktion (d3dx10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961678"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="a8cde-103">D3DXSHRotateZ-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="a8cde-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="a8cde-104">Dreht den sphärischen harmonischen Vektor (SH) in der z-Achse um den angegebenen Winkel.</span><span class="sxs-lookup"><span data-stu-id="a8cde-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8cde-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8cde-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="a8cde-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8cde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8cde-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8cde-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8cde-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8cde-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8cde-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="a8cde-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="a8cde-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a8cde-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a8cde-111">Dieser Zeiger sollte nicht mit pIn Alias sein.</span><span class="sxs-lookup"><span data-stu-id="a8cde-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="a8cde-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a8cde-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a8cde-113">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8cde-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8cde-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8cde-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8cde-115">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="a8cde-115">Order of the SH evaluation.</span></span> <span data-ttu-id="a8cde-116">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="a8cde-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a8cde-117">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a8cde-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a8cde-118">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="a8cde-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a8cde-119">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8cde-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8cde-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8cde-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8cde-121">Drehwinkel im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="a8cde-121">Rotation angle in radians.</span></span> <span data-ttu-id="a8cde-122">Die Drehung wird um die z-Achse durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8cde-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a8cde-123">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8cde-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8cde-124">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8cde-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8cde-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="a8cde-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8cde-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8cde-126">Return value</span></span>

<span data-ttu-id="a8cde-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8cde-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8cde-128">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="a8cde-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8cde-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8cde-129">Remarks</span></span>

<span data-ttu-id="a8cde-130">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="a8cde-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="a8cde-131">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="a8cde-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="a8cde-132">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="a8cde-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8cde-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8cde-133">Requirements</span></span>



| <span data-ttu-id="a8cde-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8cde-134">Requirement</span></span> | <span data-ttu-id="a8cde-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a8cde-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8cde-136">Header</span><span class="sxs-lookup"><span data-stu-id="a8cde-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a8cde-137"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8cde-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8cde-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8cde-138">Library</span></span><br/> | <dl> <span data-ttu-id="a8cde-139"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8cde-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8cde-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8cde-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8cde-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a8cde-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
