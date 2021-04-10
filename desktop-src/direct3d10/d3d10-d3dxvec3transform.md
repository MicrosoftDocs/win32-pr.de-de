---
description: Transformiert den Vektor (x, y, z, 1) durch eine angegebene Matrix.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: D3DXVec3Transform-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 6db2e2ad4279863ba68f709f02f86796552e0463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961691"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="d34ca-103">D3DXVec3Transform-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d34ca-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="d34ca-104">Transformiert den Vektor (x, y, z, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="d34ca-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d34ca-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d34ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34ca-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d34ca-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ca-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d34ca-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d34ca-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3d10-d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d34ca-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d34ca-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34ca-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ca-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d34ca-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d34ca-112">Zeiger auf den Quell- [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="d34ca-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="d34ca-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34ca-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ca-114">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d34ca-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d34ca-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d34ca-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34ca-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d34ca-116">Return value</span></span>

<span data-ttu-id="d34ca-117">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d34ca-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d34ca-118">Zeiger auf eine D3DXVECTOR4-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="d34ca-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34ca-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d34ca-119">Remarks</span></span>

<span data-ttu-id="d34ca-120">Diese Funktion wandelt den Vektor, PV (x, y, z, 1), durch die Matrix pm um.</span><span class="sxs-lookup"><span data-stu-id="d34ca-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="d34ca-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d34ca-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d34ca-122">Auf diese Weise kann die D3DXVec3Transform-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d34ca-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34ca-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d34ca-123">Requirements</span></span>



| <span data-ttu-id="d34ca-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d34ca-124">Requirement</span></span> | <span data-ttu-id="d34ca-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d34ca-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ca-126">Header</span><span class="sxs-lookup"><span data-stu-id="d34ca-126">Header</span></span><br/> | <dl> <span data-ttu-id="d34ca-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34ca-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34ca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d34ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34ca-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d34ca-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
