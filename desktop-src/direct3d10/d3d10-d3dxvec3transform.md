---
description: 'D3DXVec3Transform-Funktion (D3DX10Math.h): Transformiert den Vektor (x, y, z, 1) durch eine angegebene Matrix.'
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: D3DXVec3Transform-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 9b5cd69ce603f56e4837818cac6ee18fe3ab1e53
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108138"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="01629-103">D3DXVec3Transform-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="01629-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="01629-104">Transformiert vektor (x, y, z, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="01629-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="01629-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01629-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="01629-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01629-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01629-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01629-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="01629-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="01629-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3d10-d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="01629-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="01629-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="01629-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01629-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="01629-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="01629-112">Zeiger auf die [**D3DXVECTOR3-Quelle.**](d3d10-d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="01629-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="01629-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="01629-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01629-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="01629-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="01629-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="01629-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01629-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01629-116">Return value</span></span>

<span data-ttu-id="01629-117">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="01629-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="01629-118">Zeiger auf eine D3DXVECTOR4-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="01629-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="01629-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01629-119">Remarks</span></span>

<span data-ttu-id="01629-120">Diese Funktion transformiert den Vektor pV (x, y, z, 1) durch die Matrix pM.</span><span class="sxs-lookup"><span data-stu-id="01629-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="01629-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="01629-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="01629-122">Auf diese Weise kann die D3DXVec3Transform-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01629-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="01629-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01629-123">Requirements</span></span>



| <span data-ttu-id="01629-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01629-124">Requirement</span></span> | <span data-ttu-id="01629-125">Wert</span><span class="sxs-lookup"><span data-stu-id="01629-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01629-126">Header</span><span class="sxs-lookup"><span data-stu-id="01629-126">Header</span></span><br/> | <dl> <span data-ttu-id="01629-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="01629-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01629-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01629-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01629-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="01629-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
