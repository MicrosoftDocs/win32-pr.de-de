---
description: 'D3DXMatrixInverse-Funktion (D3DX10Math.h): Berechnet die Umkehrung einer Matrix.'
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: D3DXMatrixInverse-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6b42cf0ae3f9ee1154d385600b00a2dcb10c4fd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113198"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="5e8ce-103">D3DXMatrixInverse-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="5e8ce-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="5e8ce-104">Berechnet die Umkehrung einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e8ce-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5e8ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e8ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8ce-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5e8ce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8ce-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e8ce-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5e8ce-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e8ce-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5e8ce-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8ce-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e8ce-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e8ce-112">Zeiger auf einen FLOAT-Wert, der die Determinante der Matrix enthält.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="5e8ce-113">Wenn die Determinante nicht benötigt wird, legen Sie diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="5e8ce-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5e8ce-114">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5e8ce-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8ce-115">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e8ce-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5e8ce-116">Zeiger auf die D3DXMATRIX-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8ce-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e8ce-117">Return value</span></span>

<span data-ttu-id="5e8ce-118">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e8ce-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5e8ce-119">Zeiger auf eine D3DXMATRIX-Struktur, die die Umkehrung der Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="5e8ce-120">Wenn die Matrixinversion fehlschlägt, **wird NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="5e8ce-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5e8ce-122">Auf diese Weise kann die D3DXMatrixInverse-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e8ce-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8ce-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e8ce-123">Requirements</span></span>



| <span data-ttu-id="5e8ce-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e8ce-124">Requirement</span></span> | <span data-ttu-id="5e8ce-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5e8ce-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8ce-126">Header</span><span class="sxs-lookup"><span data-stu-id="5e8ce-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5e8ce-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ce-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5e8ce-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e8ce-128">Library</span></span><br/> | <dl> <span data-ttu-id="5e8ce-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ce-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e8ce-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e8ce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8ce-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5e8ce-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
