---
description: 'D3DXVec3TransformCoord-Funktion (D3DX10Math.h): Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projiziert das Ergebnis zurück in w = 1.'
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: D3DXVec3TransformCoord-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5b3e763d87503f9ca71911ad40ccf3c6ae9ca722
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108098"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="835a7-103">D3DXVec3TransformCoord-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="835a7-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="835a7-104">Transformiert einen 3D-Vektor durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="835a7-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="835a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="835a7-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="835a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="835a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835a7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="835a7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="835a7-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="835a7-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="835a7-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="835a7-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="835a7-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="835a7-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835a7-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="835a7-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="835a7-112">Zeiger auf die D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="835a7-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="835a7-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="835a7-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835a7-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="835a7-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="835a7-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="835a7-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835a7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="835a7-116">Return value</span></span>

<span data-ttu-id="835a7-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="835a7-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="835a7-118">Zeiger auf eine D3DXVECTOR3-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="835a7-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="835a7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="835a7-119">Remarks</span></span>

<span data-ttu-id="835a7-120">Diese Funktion transformiert den Vektor pV (x, y, z, 1) durch die Matrix pM und projiziert das Ergebnis zurück in w=1.</span><span class="sxs-lookup"><span data-stu-id="835a7-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="835a7-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="835a7-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="835a7-122">Auf diese Weise kann die D3DXVec3TransformCoord-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="835a7-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="835a7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="835a7-123">Requirements</span></span>



| <span data-ttu-id="835a7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="835a7-124">Requirement</span></span> | <span data-ttu-id="835a7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="835a7-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="835a7-126">Header</span><span class="sxs-lookup"><span data-stu-id="835a7-126">Header</span></span><br/> | <dl> <span data-ttu-id="835a7-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="835a7-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835a7-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="835a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835a7-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="835a7-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
