---
description: 'D3DXPlaneIntersectLine-Funktion (D3DX10Math.h): Sucht die Schnittmenge zwischen einer Ebene und einer Linie.'
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: D3DXPlaneIntersectLine-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108808"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="37946-103">D3DXPlaneIntersectLine-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="37946-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="37946-104">Sucht die Schnittmenge zwischen einer Ebene und einer Linie.</span><span class="sxs-lookup"><span data-stu-id="37946-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="37946-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37946-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="37946-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37946-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37946-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37946-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37946-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37946-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37946-109">Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der die Schnittmenge zwischen der angegebenen Ebene und Linie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37946-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="37946-110">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37946-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37946-111">Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="37946-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="37946-112">Zeiger auf die [**D3DXPLANE-Quelldatei.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="37946-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="37946-113">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37946-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37946-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37946-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37946-115">Zeiger auf eine D3DXVECTOR3-Quellstruktur, die einen Zeilenstartpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="37946-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="37946-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37946-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37946-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37946-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37946-118">Zeiger auf eine D3DXVECTOR3-Quellstruktur, die einen Zeilenendpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="37946-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37946-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37946-119">Return value</span></span>

<span data-ttu-id="37946-120">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37946-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37946-121">Zeiger auf eine D3DXVECTOR3-Struktur, die die Schnittmenge zwischen der angegebenen Ebene und Linie ist.</span><span class="sxs-lookup"><span data-stu-id="37946-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="37946-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37946-122">Remarks</span></span>

<span data-ttu-id="37946-123">Wenn die Linie parallel zur Ebene ist, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37946-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="37946-124">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37946-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="37946-125">Auf diese Weise kann die D3DXPlaneIntersectLine-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37946-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37946-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37946-126">Requirements</span></span>



| <span data-ttu-id="37946-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37946-127">Requirement</span></span> | <span data-ttu-id="37946-128">Wert</span><span class="sxs-lookup"><span data-stu-id="37946-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37946-129">Header</span><span class="sxs-lookup"><span data-stu-id="37946-129">Header</span></span><br/>  | <dl> <span data-ttu-id="37946-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37946-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="37946-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37946-131">Library</span></span><br/> | <dl> <span data-ttu-id="37946-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="37946-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37946-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37946-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37946-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="37946-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
