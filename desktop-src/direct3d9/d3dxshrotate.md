---
description: 'D3DXSHRotate-Funktion (D3dx9math.h): Rotiert den SH-Vektor (Spherical Vector) um die angegebene Matrix.'
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 8f888186fb6d7563a5904d4e6e3f1eabe626afd1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093868"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="d25b7-103">D3DXSHRotate-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d25b7-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="d25b7-104">Rotiert den SH-Vektor (Spherical Vector) um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="d25b7-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d25b7-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="d25b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d25b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25b7-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d25b7-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d25b7-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d25b7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d25b7-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical Veralten).</span><span class="sxs-lookup"><span data-stu-id="d25b7-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="d25b7-110">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="d25b7-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d25b7-111">Dieser Zeiger sollte keinen Alias mit *pIn* verwenden.</span><span class="sxs-lookup"><span data-stu-id="d25b7-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="d25b7-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d25b7-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d25b7-113">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d25b7-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d25b7-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d25b7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d25b7-115">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="d25b7-115">Order of the SH evaluation.</span></span> <span data-ttu-id="d25b7-116">Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="d25b7-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d25b7-117">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="d25b7-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d25b7-118">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="d25b7-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d25b7-119">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d25b7-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d25b7-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d25b7-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d25b7-121">Zeiger auf die Rotationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="d25b7-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="d25b7-122">Die Rotationsuntermatrix muss orthogonal sein, mit einer Determinante der Einheit.</span><span class="sxs-lookup"><span data-stu-id="d25b7-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="d25b7-123">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d25b7-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d25b7-124">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d25b7-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d25b7-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="d25b7-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25b7-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d25b7-126">Return value</span></span>

<span data-ttu-id="d25b7-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d25b7-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d25b7-128">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="d25b7-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="d25b7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d25b7-129">Remarks</span></span>

<span data-ttu-id="d25b7-130">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="d25b7-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="d25b7-131">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="d25b7-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="d25b7-132">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="d25b7-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="d25b7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d25b7-133">Requirements</span></span>



| <span data-ttu-id="d25b7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d25b7-134">Requirement</span></span> | <span data-ttu-id="d25b7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d25b7-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d25b7-136">Header</span><span class="sxs-lookup"><span data-stu-id="d25b7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d25b7-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d25b7-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d25b7-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d25b7-138">Library</span></span><br/> | <dl> <span data-ttu-id="d25b7-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d25b7-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d25b7-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d25b7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25b7-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d25b7-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d25b7-142">Vorausberechnungsübertragung der Radiance (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d25b7-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
