---
description: Wandelt den 3D-Vektor normal um die angegebene Matrix um.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: D3DXVec3TransformNormal-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355297"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="3fd77-103">D3DXVec3TransformNormal-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3fd77-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="3fd77-104">Wandelt den 3D-Vektor normal um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="3fd77-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd77-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="3fd77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd77-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3fd77-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd77-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fd77-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3fd77-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3fd77-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3fd77-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd77-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd77-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fd77-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3fd77-112">Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3fd77-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="3fd77-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd77-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd77-114">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fd77-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3fd77-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3fd77-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd77-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fd77-116">Return value</span></span>

<span data-ttu-id="3fd77-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fd77-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3fd77-118">Zeiger auf eine D3DXVECTOR3-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="3fd77-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd77-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd77-119">Remarks</span></span>

<span data-ttu-id="3fd77-120">Diese Funktion transformiert den Vektor (PV->x, PV->y, PV->z, 0) durch die Matrix, auf die von pm gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3fd77-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="3fd77-121">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fd77-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="3fd77-122">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3fd77-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3fd77-123">Auf diese Weise kann die **D3DXVec3TransformNormal** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fd77-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd77-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fd77-124">Requirements</span></span>



| <span data-ttu-id="3fd77-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fd77-125">Requirement</span></span> | <span data-ttu-id="3fd77-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd77-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd77-127">Header</span><span class="sxs-lookup"><span data-stu-id="3fd77-127">Header</span></span><br/> | <dl> <span data-ttu-id="3fd77-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd77-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd77-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd77-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3fd77-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
