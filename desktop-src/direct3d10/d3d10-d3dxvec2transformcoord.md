---
description: 'D3DXVec2TransformCoord-Funktion (D3DX10Math.h): Transformiert einen 2D-Vektor durch eine bestimmte Matrix und pro projectiert das Ergebnis zurück in w = 1.'
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: D3DXVec2TransformCoord-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108338"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="0418c-103">D3DXVec2TransformCoord-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="0418c-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="0418c-104">Transformiert einen 2D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="0418c-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="0418c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0418c-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0418c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0418c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0418c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0418c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0418c-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="0418c-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0418c-109">Zeiger auf den [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) der das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0418c-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0418c-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0418c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0418c-111">Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="0418c-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0418c-112">Zeiger auf die D3DXVECTOR2-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="0418c-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="0418c-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0418c-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0418c-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0418c-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0418c-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="0418c-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0418c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0418c-116">Return value</span></span>

<span data-ttu-id="0418c-117">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="0418c-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0418c-118">Zeiger auf eine D3DXVECTOR2-Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="0418c-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="0418c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0418c-119">Remarks</span></span>

<span data-ttu-id="0418c-120">Diese Funktion transformiert den Vektor pV (x, y, 0, 1) durch die Matrix, pM, und pro projectiert das Ergebnis zurück in w=1.</span><span class="sxs-lookup"><span data-stu-id="0418c-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="0418c-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0418c-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0418c-122">Auf diese Weise kann die D3DXVec2TransformCoord-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0418c-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0418c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0418c-123">Requirements</span></span>



| <span data-ttu-id="0418c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0418c-124">Requirement</span></span> | <span data-ttu-id="0418c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0418c-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0418c-126">Header</span><span class="sxs-lookup"><span data-stu-id="0418c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0418c-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0418c-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0418c-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0418c-128">Library</span></span><br/> | <dl> <span data-ttu-id="0418c-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0418c-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0418c-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0418c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0418c-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0418c-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
