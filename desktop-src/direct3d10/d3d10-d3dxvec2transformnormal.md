---
description: Transformiert den 2D-Vektor normal um die angegebene Matrix.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: D3DXVec2TransformNormal-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961618"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="a373d-103">D3DXVec2TransformNormal-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a373d-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="a373d-104">Transformiert den 2D-Vektor normal um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="a373d-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a373d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a373d-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a373d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a373d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a373d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a373d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a373d-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a373d-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a373d-109">Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a373d-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a373d-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a373d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a373d-111">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a373d-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a373d-112">Ein Zeiger auf die Quell-D3DXVECTOR2-Struktur.</span><span class="sxs-lookup"><span data-stu-id="a373d-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a373d-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a373d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a373d-114">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a373d-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a373d-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a373d-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a373d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a373d-116">Return value</span></span>

<span data-ttu-id="a373d-117">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a373d-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a373d-118">Zeiger auf eine D3DXVECTOR2-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="a373d-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a373d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a373d-119">Remarks</span></span>

<span data-ttu-id="a373d-120">Diese Funktion transformiert den Vektor (PV->x, PV->y, 0, 0) durch die Matrix, auf die von pm gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a373d-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="a373d-121">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a373d-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="a373d-122">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a373d-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a373d-123">Auf diese Weise kann die **D3DXVec2TransformNormal** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a373d-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a373d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a373d-124">Requirements</span></span>



| <span data-ttu-id="a373d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a373d-125">Requirement</span></span> | <span data-ttu-id="a373d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a373d-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a373d-127">Header</span><span class="sxs-lookup"><span data-stu-id="a373d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a373d-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a373d-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a373d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a373d-129">Library</span></span><br/> | <dl> <span data-ttu-id="a373d-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a373d-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a373d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a373d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a373d-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a373d-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
