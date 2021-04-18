---
description: Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: D3DXSHRotate-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1cdff4a74cb92943db2bd6dc9f207dbac2208afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355044"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="2bce7-103">D3DXSHRotate-Funktion (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="2bce7-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="2bce7-104">Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="2bce7-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bce7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bce7-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="2bce7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bce7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bce7-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bce7-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bce7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bce7-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="2bce7-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="2bce7-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="2bce7-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bce7-111">Dieser Zeiger sollte nicht mit pIn Alias sein.</span><span class="sxs-lookup"><span data-stu-id="2bce7-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="2bce7-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2bce7-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2bce7-113">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bce7-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bce7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bce7-115">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="2bce7-115">Order of the SH evaluation.</span></span> <span data-ttu-id="2bce7-116">Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="2bce7-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2bce7-117">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="2bce7-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bce7-118">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="2bce7-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2bce7-119">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bce7-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bce7-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2bce7-121">Zeiger auf die Rotations Matrix.</span><span class="sxs-lookup"><span data-stu-id="2bce7-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="2bce7-122">Die Rotations Teil Matrix muss orthogonal und eine Maßeinheit sein.</span><span class="sxs-lookup"><span data-stu-id="2bce7-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="2bce7-123">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bce7-124">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bce7-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bce7-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="2bce7-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bce7-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bce7-126">Return value</span></span>

<span data-ttu-id="2bce7-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bce7-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bce7-128">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="2bce7-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bce7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bce7-129">Remarks</span></span>

<span data-ttu-id="2bce7-130">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="2bce7-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2bce7-131">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="2bce7-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2bce7-132">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="2bce7-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bce7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bce7-133">Requirements</span></span>



| <span data-ttu-id="2bce7-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bce7-134">Requirement</span></span> | <span data-ttu-id="2bce7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2bce7-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bce7-136">Header</span><span class="sxs-lookup"><span data-stu-id="2bce7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2bce7-137"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bce7-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bce7-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2bce7-138">Library</span></span><br/> | <dl> <span data-ttu-id="2bce7-139"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bce7-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bce7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bce7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bce7-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2bce7-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
