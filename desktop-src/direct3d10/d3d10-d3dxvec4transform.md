---
description: 'D3DXVec4Transform-Funktion (D3DX10Math.h): Transformiert einen 4D-Vektor durch eine bestimmte Matrix.'
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: D3DXVec4Transform-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 737e1901a514a3940790ce83c7e9bc1f6f471371
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102918"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="41f37-103">D3DXVec4Transform-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="41f37-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="41f37-104">Transformiert einen 4D-Vektor durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="41f37-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f37-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="41f37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41f37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f37-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="41f37-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41f37-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="41f37-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="41f37-109">Zeiger auf [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="41f37-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41f37-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="41f37-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f37-111">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="41f37-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="41f37-112">Zeiger auf die D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="41f37-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="41f37-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="41f37-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f37-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="41f37-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41f37-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="41f37-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f37-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41f37-116">Return value</span></span>

<span data-ttu-id="41f37-117">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="41f37-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="41f37-118">Zeiger auf eine D3DXVECTOR4-Struktur, die der transformierte 4D-Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="41f37-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f37-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41f37-119">Remarks</span></span>

<span data-ttu-id="41f37-120">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="41f37-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="41f37-121">Auf diese Weise kann die D3DXVec4Transform-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f37-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f37-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41f37-122">Requirements</span></span>



| <span data-ttu-id="41f37-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41f37-123">Requirement</span></span> | <span data-ttu-id="41f37-124">Wert</span><span class="sxs-lookup"><span data-stu-id="41f37-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41f37-125">Header</span><span class="sxs-lookup"><span data-stu-id="41f37-125">Header</span></span><br/> | <dl> <span data-ttu-id="41f37-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="41f37-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f37-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="41f37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f37-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="41f37-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
