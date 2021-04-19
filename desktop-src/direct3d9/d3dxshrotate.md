---
description: Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351946"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="4675c-103">D3DXSHRotate-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4675c-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="4675c-104">Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="4675c-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4675c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4675c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="4675c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4675c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4675c-107">*Pout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4675c-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4675c-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4675c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4675c-109">Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH).</span><span class="sxs-lookup"><span data-stu-id="4675c-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="4675c-110">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="4675c-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4675c-111">Dieser Zeiger sollte nicht mit *pIn* Alias sein.</span><span class="sxs-lookup"><span data-stu-id="4675c-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="4675c-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="4675c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4675c-113">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4675c-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4675c-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4675c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4675c-115">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="4675c-115">Order of the SH evaluation.</span></span> <span data-ttu-id="4675c-116">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="4675c-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="4675c-117">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="4675c-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4675c-118">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="4675c-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="4675c-119">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4675c-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4675c-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4675c-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4675c-121">Zeiger auf die Rotations Matrix.</span><span class="sxs-lookup"><span data-stu-id="4675c-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="4675c-122">Die Rotations Teil Matrix muss orthogonal und eine Maßeinheit sein.</span><span class="sxs-lookup"><span data-stu-id="4675c-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="4675c-123">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4675c-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4675c-124">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4675c-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4675c-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="4675c-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4675c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4675c-126">Return value</span></span>

<span data-ttu-id="4675c-127">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4675c-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4675c-128">Zeiger auf SH-Ausgabe Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="4675c-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="4675c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4675c-129">Remarks</span></span>

<span data-ttu-id="4675c-130">Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="4675c-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="4675c-131">l ist der Grad der Basis Funktion.</span><span class="sxs-lookup"><span data-stu-id="4675c-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="4675c-132">m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="4675c-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="4675c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4675c-133">Requirements</span></span>



| <span data-ttu-id="4675c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4675c-134">Requirement</span></span> | <span data-ttu-id="4675c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4675c-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4675c-136">Header</span><span class="sxs-lookup"><span data-stu-id="4675c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4675c-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4675c-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4675c-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4675c-138">Library</span></span><br/> | <dl> <span data-ttu-id="4675c-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4675c-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4675c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4675c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4675c-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4675c-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4675c-142">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4675c-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
