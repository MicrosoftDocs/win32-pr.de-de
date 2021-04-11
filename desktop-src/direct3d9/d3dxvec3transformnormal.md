---
description: Wandelt den 3D-Vektor normal um die angegebene Matrix um.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: D3DXVec3TransformNormal-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219661"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="620d0-103">D3DXVec3TransformNormal-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="620d0-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="620d0-104">Wandelt den 3D-Vektor normal um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="620d0-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="620d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="620d0-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="620d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="620d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="620d0-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="620d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="620d0-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="620d0-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620d0-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="620d0-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="620d0-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="620d0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620d0-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="620d0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620d0-112">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="620d0-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="620d0-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="620d0-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620d0-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="620d0-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="620d0-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="620d0-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="620d0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="620d0-116">Return value</span></span>

<span data-ttu-id="620d0-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="620d0-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620d0-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="620d0-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="620d0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="620d0-119">Remarks</span></span>

<span data-ttu-id="620d0-120">Diese Funktion transformiert den Vektor (*PV*->x, *PV*->y, *PV*->z, 0) durch die Matrix, auf die von *pm* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="620d0-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="620d0-121">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="620d0-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="620d0-122">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="620d0-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="620d0-123">Auf diese Weise kann die **D3DXVec3TransformNormal** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="620d0-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="620d0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="620d0-124">Requirements</span></span>



| <span data-ttu-id="620d0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="620d0-125">Requirement</span></span> | <span data-ttu-id="620d0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="620d0-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="620d0-127">Header</span><span class="sxs-lookup"><span data-stu-id="620d0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="620d0-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="620d0-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="620d0-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="620d0-129">Library</span></span><br/> | <dl> <span data-ttu-id="620d0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="620d0-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="620d0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="620d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620d0-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="620d0-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




