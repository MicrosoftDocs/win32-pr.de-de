---
description: 'D3DXVec2TransformNormal-Funktion (D3dx9math.h): Transformiert den 2D-Vektor normal durch die gegebene Matrix.'
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: D3DXVec2TransformNormal-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097908"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="e4551-103">D3DXVec2TransformNormal-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e4551-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="e4551-104">Transformiert den 2D-Vektor normal durch die gegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="e4551-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4551-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4551-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e4551-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4551-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4551-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4551-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4551-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4551-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="e4551-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e4551-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e4551-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4551-111">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4551-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4551-112">Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="e4551-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4551-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e4551-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4551-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4551-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4551-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="e4551-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4551-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4551-116">Return value</span></span>

<span data-ttu-id="e4551-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4551-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4551-118">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="e4551-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4551-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4551-119">Remarks</span></span>

<span data-ttu-id="e4551-120">Diese Funktion transformiert den Vektor (*pV-*>x, *pV-*>y, 0, 0) durch die Matrix, auf die *pM zeigt.*</span><span class="sxs-lookup"><span data-stu-id="e4551-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="e4551-121">Wenn Sie einen Normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="e4551-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="e4551-122">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="e4551-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e4551-123">Auf diese Weise kann die **D3DXVec2TransformNormal-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4551-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4551-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4551-124">Requirements</span></span>



| <span data-ttu-id="e4551-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4551-125">Requirement</span></span> | <span data-ttu-id="e4551-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e4551-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4551-127">Header</span><span class="sxs-lookup"><span data-stu-id="e4551-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e4551-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4551-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4551-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4551-129">Library</span></span><br/> | <dl> <span data-ttu-id="e4551-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4551-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4551-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4551-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4551-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4551-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4551-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="e4551-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="e4551-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="e4551-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




