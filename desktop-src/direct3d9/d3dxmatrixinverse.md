---
description: 'D3DXMatrixInverse-Funktion (D3dx9math.h): Berechnet die Umkehrung einer Matrix.'
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: D3DXMatrixInverse-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098148"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="286ab-103">D3DXMatrixInverse-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="286ab-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="286ab-104">Berechnet die Umkehrung einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="286ab-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="286ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="286ab-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="286ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="286ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="286ab-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="286ab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="286ab-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="286ab-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="286ab-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="286ab-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="286ab-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="286ab-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="286ab-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="286ab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="286ab-112">Zeiger auf einen FLOAT-Wert, der die Determinante der Matrix enthält.</span><span class="sxs-lookup"><span data-stu-id="286ab-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="286ab-113">Wenn die Determinante nicht benötigt wird, legen Sie diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="286ab-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="286ab-114">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="286ab-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="286ab-115">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="286ab-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="286ab-116">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="286ab-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="286ab-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="286ab-117">Return value</span></span>

<span data-ttu-id="286ab-118">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="286ab-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="286ab-119">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Umkehrung der Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="286ab-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="286ab-120">Wenn die Matrixumkehr fehlschlägt, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="286ab-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="286ab-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="286ab-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="286ab-122">Auf diese Weise kann die **D3DXMatrixInverse-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="286ab-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="286ab-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="286ab-123">Requirements</span></span>



| <span data-ttu-id="286ab-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="286ab-124">Requirement</span></span> | <span data-ttu-id="286ab-125">Wert</span><span class="sxs-lookup"><span data-stu-id="286ab-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="286ab-126">Header</span><span class="sxs-lookup"><span data-stu-id="286ab-126">Header</span></span><br/>  | <dl> <span data-ttu-id="286ab-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="286ab-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="286ab-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="286ab-128">Library</span></span><br/> | <dl> <span data-ttu-id="286ab-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="286ab-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="286ab-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="286ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="286ab-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="286ab-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
