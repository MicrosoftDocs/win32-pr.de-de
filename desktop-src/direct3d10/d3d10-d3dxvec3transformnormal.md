---
description: 'D3DXVec3TransformNormal-Funktion (D3DX10Math.h): Transformiert den 3D-Vektor normal durch die angegebene Matrix.'
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: D3DXVec3TransformNormal-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 0fc1456b89f3e11f2076a8e7b6b960d15e9c7083
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103058"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="07155-103">D3DXVec3TransformNormal-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="07155-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="07155-104">Transformiert den 3D-Vektor normal durch die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="07155-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="07155-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07155-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="07155-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07155-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07155-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07155-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07155-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="07155-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07155-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="07155-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07155-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="07155-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07155-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07155-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07155-112">Zeiger auf die D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="07155-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="07155-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="07155-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07155-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="07155-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="07155-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="07155-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07155-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07155-116">Return value</span></span>

<span data-ttu-id="07155-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="07155-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07155-118">Zeiger auf eine D3DXVECTOR3-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="07155-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="07155-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07155-119">Remarks</span></span>

<span data-ttu-id="07155-120">Diese Funktion transformiert den Vektor (pV->x, pV->y, pV->z, 0) durch die Matrix, auf die pM zeigt.</span><span class="sxs-lookup"><span data-stu-id="07155-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="07155-121">Wenn Sie einen normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="07155-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="07155-122">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07155-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="07155-123">Auf diese Weise kann die **D3DXVec3TransformNormal-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07155-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07155-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07155-124">Requirements</span></span>



| <span data-ttu-id="07155-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07155-125">Requirement</span></span> | <span data-ttu-id="07155-126">Wert</span><span class="sxs-lookup"><span data-stu-id="07155-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07155-127">Header</span><span class="sxs-lookup"><span data-stu-id="07155-127">Header</span></span><br/> | <dl> <span data-ttu-id="07155-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="07155-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07155-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07155-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07155-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="07155-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
