---
description: 'D3DXVec3TransformNormal-Funktion (D3dx9math.h): Transformiert den 3D-Vektor normal durch die gegebene Matrix.'
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: D3DXVec3TransformNormal-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115618"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="c046d-103">D3DXVec3TransformNormal-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c046d-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="c046d-104">Transformiert den 3D-Vektor normal durch die gegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="c046d-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c046d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c046d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c046d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c046d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c046d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c046d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c046d-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c046d-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c046d-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c046d-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c046d-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c046d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c046d-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c046d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c046d-112">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="c046d-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c046d-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c046d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c046d-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c046d-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c046d-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="c046d-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c046d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c046d-116">Return value</span></span>

<span data-ttu-id="c046d-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c046d-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c046d-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="c046d-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c046d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c046d-119">Remarks</span></span>

<span data-ttu-id="c046d-120">Diese Funktion transformiert den Vektor (*pV*->x, *pV*->y, *pV*->z, 0) durch die Matrix, auf die *pM* zeigt.</span><span class="sxs-lookup"><span data-stu-id="c046d-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="c046d-121">Wenn Sie einen Normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="c046d-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="c046d-122">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="c046d-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c046d-123">Auf diese Weise kann die **D3DXVec3TransformNormal-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c046d-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c046d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c046d-124">Requirements</span></span>



| <span data-ttu-id="c046d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c046d-125">Requirement</span></span> | <span data-ttu-id="c046d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c046d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c046d-127">Header</span><span class="sxs-lookup"><span data-stu-id="c046d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c046d-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c046d-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c046d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c046d-129">Library</span></span><br/> | <dl> <span data-ttu-id="c046d-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c046d-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c046d-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c046d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c046d-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c046d-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




