---
description: Berechnet den umgekehrten einer Matrix.
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: D3DXMatrixInverse-Funktion (D3dx9math. h)
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
ms.openlocfilehash: eac1072c0174a03482e60167180f900588a13a72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351942"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="2e4b4-103">D3DXMatrixInverse-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2e4b4-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="2e4b4-104">Berechnet den umgekehrten einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e4b4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2e4b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e4b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4b4-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e4b4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4b4-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e4b4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e4b4-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e4b4-110">*pdeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e4b4-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4b4-111">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e4b4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e4b4-112">Ein Zeiger auf einen float-Wert, der den Determinanten der Matrix enthält.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="2e4b4-113">Wenn die Determinante nicht benötigt wird, legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e4b4-114">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e4b4-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4b4-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e4b4-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e4b4-116">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4b4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e4b4-117">Return value</span></span>

<span data-ttu-id="2e4b4-118">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e4b4-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e4b4-119">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Umkehrung der Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="2e4b4-120">Wenn die Matrix Inversion fehlschlägt, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="2e4b4-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2e4b4-122">Auf diese Weise kann die **D3DXMatrixInverse** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4b4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e4b4-123">Requirements</span></span>



| <span data-ttu-id="2e4b4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e4b4-124">Requirement</span></span> | <span data-ttu-id="2e4b4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2e4b4-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4b4-126">Header</span><span class="sxs-lookup"><span data-stu-id="2e4b4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2e4b4-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e4b4-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e4b4-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e4b4-128">Library</span></span><br/> | <dl> <span data-ttu-id="2e4b4-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e4b4-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e4b4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e4b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4b4-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2e4b4-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
