---
description: 'D3DXSHRotate-Funktion (D3DX10.h): Rotiert den SH-Vektor (Spherical Vector) um die angegebene Matrix.'
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: D3DXSHRotate-Funktion (D3DX10.h)
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
ms.openlocfilehash: 2f2af3fe59c57ba32bc03bb59233bec72722bbb5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108538"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="cdd00-103">D3DXSHRotate-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="cdd00-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="cdd00-104">Rotiert den SH-Vektor (Spherical Vector) um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="cdd00-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd00-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="cdd00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd00-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdd00-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd00-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd00-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd00-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical Veralten).</span><span class="sxs-lookup"><span data-stu-id="cdd00-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="cdd00-110">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="cdd00-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="cdd00-111">Dieser Zeiger sollte keinen Alias mit pIn verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdd00-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="cdd00-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="cdd00-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cdd00-113">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdd00-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd00-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd00-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd00-115">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="cdd00-115">Order of the SH evaluation.</span></span> <span data-ttu-id="cdd00-116">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="cdd00-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="cdd00-117">Die Auswertung generiert Order²-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="cdd00-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="cdd00-118">Der Grad der Auswertung ist "Order - 1".</span><span class="sxs-lookup"><span data-stu-id="cdd00-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="cdd00-119">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdd00-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd00-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdd00-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cdd00-121">Zeiger auf die Rotationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="cdd00-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="cdd00-122">Die Rotationsuntermatrix muss orthogonal sein, mit einer Determinante der Einheit.</span><span class="sxs-lookup"><span data-stu-id="cdd00-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="cdd00-123">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdd00-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd00-124">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdd00-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd00-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="cdd00-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd00-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdd00-126">Return value</span></span>

<span data-ttu-id="cdd00-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd00-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd00-128">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="cdd00-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd00-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdd00-129">Remarks</span></span>

<span data-ttu-id="cdd00-130">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:</span><span class="sxs-lookup"><span data-stu-id="cdd00-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="cdd00-131">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="cdd00-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="cdd00-132">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.</span><span class="sxs-lookup"><span data-stu-id="cdd00-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd00-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd00-133">Requirements</span></span>



| <span data-ttu-id="cdd00-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd00-134">Requirement</span></span> | <span data-ttu-id="cdd00-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cdd00-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd00-136">Header</span><span class="sxs-lookup"><span data-stu-id="cdd00-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cdd00-137"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd00-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdd00-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdd00-138">Library</span></span><br/> | <dl> <span data-ttu-id="cdd00-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdd00-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd00-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdd00-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd00-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cdd00-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
